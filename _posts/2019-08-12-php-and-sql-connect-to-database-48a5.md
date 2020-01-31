---
title: 'PHP and SQL: Connect to Database'
date: '2019-08-12T23:27:50.293Z'
excerpt: ''
thumb_img_path: null
comments_count: 5
positive_reactions_count: 9
tags: []
canonical_url: 'https://dev.to/th3n00bc0d3r/php-and-sql-connect-to-database-48a5'
layout: post
---
## What the heck is SQL?
SQL stand for structured query language. It is just a syntax created to select, update, delete and insert data into a relational database system, such as MySQL, MariaDB.

Now lets get into the game. Create a folder by the name of sql_basics in our PHP project and then Create a file by the name of insert_data.php, inside the folder.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/20y741er5y164nth98ck.png)

Now lets look at the piece of code inside the file.

![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/oyr7db50g2bb2228jbja.png)

{% raw %}```
$conn = mysqli_connect('localhost','root','','myfirstdb');
```{% endraw %}
We created a variable by the name of $conn and called a built-in function that comes with PHP known as mysqli_connect. This function does all the hardwork for us of making the conneciton. The function is given 4 values.
* Database Host
* Database User
* Database Password
* Database Name

Now once you run it, it will try to create a connection to the database.

{% raw %}```
if (!$conn) {
   die("Connection failed: ".mysqli_connect_error());
}
```{% endraw %}
Next, we will check whether a connection has been made or not. Therefore, we create an if function and if it does not return true, then that means there is something wrong. We will kill the connection and throw out the error. Now if no error is produced, the code will run forth.

**REMEMBER, IN PHP THE CODE RUNS FROM TOP TO DOWN EXECUTION, MEANING WHAT IS AT THE START OF THE FILE EXECUTES FIRST AND THEN AS IT GOES DOWN, DOES EVERYTHING ELSE EXECUTES**

**Some Fun**
I will now run the following code;
{% raw %}```
$conn = mysqli_connect('localhost','fakeuser','','myfirstdb');
```{% endraw %}
![Alt Text](https://thepracticaldev.s3.amazonaws.com/i/yiig6d9ek39gmqhwt6ob.png)

Look at that, taking Like a Champ!, Now that is how an error would look out, if you read it, it will make sense.

**INSERT AN ENTRY INTO THE DATABASE**
{% raw %}```
$sql = "INSERT INTO users (email, password) VALUES ('c@c.com', 'hello')";
```{% endraw %}
We have just created a variable by the name of $sql and in it all we have created a s string which is called a SQL. The SQL has a build in command, INSERT INTO then we specify the table name into which we want to add the entry. Now the first brackets will contain the columns in which we want to enter the data and then comes the VALUES tag and in the second brackets, we will enter values. The Frist value c@c.com is being entered into email. The second value hello will go into password column.

**ALWAYS REMEMBER THAT THE SINGLE QUOTE IS VERY IMPORTANT FOR THE QUERY TO RUN SUCCESSFUL**

{% raw %}```
$conn->query($sql);
```{% endraw %}
Now this statement simple asks PHP to pass the SQL into the SQL Language and run the query on the database.

**DELETE**
{% raw %}```
$sql = "DELETE FROM users WHERE id = '1'";
```{% endraw %}
Delete is relatively simple as it is condition based, so you are going to be deleting based on a condition.

**UPDATE**
{% raw %}```
$sql = "UPDATE users SET password = 'hello', name = 'Mr. Yes' WHERE id = '3'";
```{% endraw %}
Update is also understandable not, as you update values, based on a condition.

**SELECT**
{% raw %}```
$sql = "SELECT * FROM users WHERE id = '3'";
$result = $conn->query($sql);
$user =  $result->fetch_array();
print_r($user); 

//OUTTPUT
Array ( 
  [id] => 3, 
  [date] => 2019-08-08 14:44:58, 
  [email] => test@test1.com, 
  [password] => hello, 
  [name] => Mr. Yes 
)
```{% endraw %}
Now we have selected a user whose ID is 3, therefore we need to store the response from $conn in a $result variable and then fetch it as an array. Now when we print the array, we will get an output like this.

**SELECT FOR MORE THAN ONE**
{% raw %}```
$sql = "SELECT * FROM users";
$result = $conn->query($sql);

while ($row = $result->fetch_array()) {
   print_r($row);
}
```{% endraw %}
Now for getting more than one results, we need to encase it into a while loop, which keeps running till it runs out of results. 

### NOW EVERYTHING TOGETHAR
{% raw %}```
//Create Connection
$conn = mysqli_connect('localhost','root','','noob_cms');

//CHECK CONNECTION
if (!$conn) {
    die("Connection failed: ".mysqli_connect_error());
}

//Insert
$sql = "INSERT INTO users (email, password, name) VALUES ('test@test.com', 'test', 'Mr. Test')";

//DELETE
$sql = "DELETE FROM users WHERE id = '1'";

//UPDATE
$sql = "UPDATE users SET password = 'hello', name = 'Mr. Yes' WHERE id = '3'";

//SELECT for Multiple
$sql = "SELECT * FROM users";
$result = $conn->query($sql);
while ($row = $result->fetch_array()) {
   var_dump($row);
}

//SELECT FOR single
$sql = "SELECT * FROM users WHERE id = '3'";
$result = $conn->query($sql);
$user =  $result->fetch_array();
var_dump($user);
echo $user['name']; //Prints Name
```{% endraw %}

Please Feel Free to ask any questions.

[Noob Index](https://dev.to/th3n00bc0d3r/noob-guides-index-4mne)

*[This post is also available on DEV.](https://dev.to/th3n00bc0d3r/php-and-sql-connect-to-database-48a5)*


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
