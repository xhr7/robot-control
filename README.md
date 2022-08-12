# robot-control-BY Rahaf
Connect Robot Control panel with database using php, and MySQL. 

## Requirement

* [XAMPP](https://www.apachefriends.org/download.html)
 
## Instructions Running
Create MySQL Database at the Localhost:
1. Open XAMPP start the server ```Apache``` and ```MySQL```.
2. Open your browser and go to ```localhost/phpmyadmin```
3. Put project file **Control_Panel** in folder ```htdocs``` in ```XAMPP``` folder
4. Open connection to MySQL.
```
<?php
$servername = "localhost";
$username = "admin";
$password = "";

// Create connection
$conn = new mysqli($servername, $username, $password);
// Check connection
if ($conn->connect_error) {
  die("Connection failed: " . $conn->connect_error);
} 
echo "Connected successfully";
?>
``` 

5. Create a MySQL Database
```
$sql = "CREATE DATABASE control_panel";
```

6. Create a MySQL Table
```
$create_table = $conn->query("CREATE TABLE control (
  id INT,
  forward TEXT,
  backward TEXT,
  move_right TEXT,
  move_left TEXT,
  press_stop TEXT
)");

```

7. Insert Data into table
```
$inser_data = $conn -> query("INSERT INTO `control`(`id`, `forward`, `backward`, `move_right`, `move_left`, `press_stop`) 
VALUES (1,'Forward','Backward','Right','Left','Stop'");

```![ROBOT](https://user-images.githubusercontent.com/102740867/184293885-3c6191c7-9d69-4944-ae0b-e43122ea7924.PNG)

