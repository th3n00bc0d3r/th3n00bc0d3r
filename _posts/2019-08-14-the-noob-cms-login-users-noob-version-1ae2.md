---
title: 'The Noob CMS: Login/Users Noob Version'
date: '2019-08-14T12:06:28.473Z'
excerpt: ''
thumb_img_path: >-
  https://res.cloudinary.com/practicaldev/image/fetch/s--FMAOU1v6--/c_imagga_scale,f_auto,fl_progressive,h_420,q_auto,w_1000/https://res.cloudinary.com/practicaldev/image/fetch/s--uvRaPyG2--/c_imagga_scale%2Cf_auto%2Cfl_progressive%2Ch_420%2Cq_auto%2Cw_1000/https://thepracticaldev.s3.amazonaws.com/i/1k95z2fbrn1ntzxulc3m.png
comments_count: 0
positive_reactions_count: 7
tags:
  - php
  - beginners
  - tutorial
canonical_url: 'https://dev.to/th3n00bc0d3r/the-noob-cms-login-users-noob-version-1ae2'
layout: post
---
Lets create an Empty Folder in your Web Server and create the following files;

__noobcms__

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/l51ez2mwxb8g9vw46kxh.png)

In PHPMyAdmin or MySQL Workbench Create the Following Database Structure and our database name is __noob_db___

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/4410m9oi1trcfow25ng6.png)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/reyzaeirp46009iwpdpm.png)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/e5n3zdfidtvpnj5qx413.png)

Our Config File Should Look like this
__config.php__
{% raw %}```
<?php
    //CREATE SESSTION
    session_start();

    //TIMEZONE
    date_default_timezone_set('Asia/Karachi');

    //SITE PATH
    define('SITE', 'http://localhost/noobcms/');
    
    //DATABASE CREDENTIALS
    define('DBHOST', 'localhost');
    define('DBUSER', 'root');
    define('DBPASS', '');
    define('DBNAME', 'noob_db');

    //CREATE CONNECTION
    $conn = mysqli_connect(DBHOST, DBUSER, DBPASS, DBNAME);
    
    //CHECK CONNECTION
    if (!$conn) {
        die("Connection failed: ".mysqli_connect_error());
    }
?>
```{% endraw %}

__admin_users.php__
{% raw %}```
<?php
    include("../includes/config.php");

    if (isset($_POST['btnCreateUser'])) {
        $email  = $_POST['email'];
        $pass   = $_POST['pass'];
        $name   = $_POST['name'];

        $sql = "SELECT * FROM users WHERE email = '$email'";
        if ($result = $conn->query($sql)) {
            if ($result->num_rows == 0) {
                //Email Address Doesnt Exists
                //Add User to Database
                $pass   = md5($pass); //We are Encrypting Password with MD5 Hash
                $addSQL = "INSERT INTO users (email, password, name) VALUES ('$email', '$pass', '$name')";
                $conn->query($addSQL);

                echo "New User Added";
            } else {
                //Email Address Already Exists
                echo "Email Address Already Exists";
            }
        }
    }
?>
    <head>
        <meta charset="UTF-8">
        <title>Admin: Users</title>
    </head>

    <body>
        <div>
            <form action="" method="POST">
                <label>Email Address</label>
                <input name="email" type="text" placeholder="Enter Email Address..." />

                <label>Password</label>
                <input name="pass" type="password" placeholder="Password..." />

                <label>Full Name</label>
                <input name="name" type="text" placeholder="Full Name..." />

                <button name="btnCreateUser">Create User</button>
            </form>
        </div>

        <div>
            <table border="1">
                <thead>
                    <tr>
                        <th>Email</th>
                        <th>Name</th>
                    </tr>
                </thead>
                <tbody>
                    <?php
                        $userResult = $conn->query('SELECT * FROM users');
                        if ($userResult->num_rows != 0) {
                            while ($row = $userResult->fetch_array()) {
                                ?>
                                <tr>
                                    <td><?php echo $row["email"];?></td>
                                    <td><?php echo $row["name"];?></td>
                                </tr>
                                <?php
                            }
                        }
                    ?>
                </tbody>
            </table>
        </div>
    </body>
```{% endraw %}

Now if you run this file in the browser

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/uvehgmwl3blbh6xzfod2.png)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/scmxf3bihyi8uae1ijvb.png)

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/so5a0kwnikk48p413s4i.png)

__login.php__
{% raw %}```
<?php
    include("includes/config.php");

    if (isset($_POST['btnLogin'])) {
        $email  = $_POST['email'];
        $pass   = md5($_POST['pass']);

        $sql = "SELECT * FROM users WHERE email = '$email' AND password = '$pass'";
        if ($result = $conn->query($sql)) {
            if ($result->num_rows == 1) {
                echo "Login Successful";
            } else {
                echo "Invalid Credentials";
            }
        }
    }
?>

    <head>
        <meta charset="UTF-8">
        <title>Login</title>
    </head>

    <body>
        <div>
            <form action="" method="POST">
                <label>Email Address</label>
                <input name="email" type="text" placeholder="Enter Email Address..." />

                <label>Password</label>
                <input name="pass" type="password" placeholder="Password..." />

                <button name="btnLogin">Login</button>
            </form>            
        </div>
    </body>

```{% endraw %}

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/z764v9deqn890n9tpzpm.png)


You can get the code from the following Git

<iframe class="liquidTag" src="https://dev.to/embed/github?args=th3n00bc0d3r%2Fnoobcms_login" style="border: 0; width: 100%;"></iframe>


[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/the-noob-cms-login-users-noob-version-1ae2)*


<script>
const parent = document.getElementsByTagName('head')[0];
const script = document.createElement('script');
script.type = 'text/javascript';
script.src = 'https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/4.1.1/iframeResizer.min.js';
script.charset = 'utf-8';
script.onload = function() {
    window.iFrameResize({}, '.liquidTag');
};
parent.appendChild(script);
</script>    
