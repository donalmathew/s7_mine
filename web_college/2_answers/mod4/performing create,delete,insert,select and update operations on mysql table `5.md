![[Pasted image 20241124202233.png]]
![[Pasted image 20241124202300.png]]![[Pasted image 20241124202806.png]]![[Pasted image 20241124202822.png]]![[Pasted image 20241124202848.png]]

answers:
![[Pasted image 20241124234215.png]]

![[Pasted image 20241124234247.png]]

3. insert data into table:
```php
<?php
// SQL query to insert data
$sql = "INSERT INTO Users (name, email, age) VALUES ('John Doe', 'john@example.com', 25)";

// Execute the query
if ($conn->query($sql) === TRUE) {
    echo "New record created successfully.";
} else {
    echo "Error: " . $sql . "<br>" . $conn->error;
}
?>

```

4. **SELECT Data from the Table**
```php
<?php
// SQL query to select data
$sql = "SELECT id, name, email, age FROM Users";
$result = $conn->query($sql);

if ($result->num_rows > 0) {
    // Output data for each row
    while ($row = $result->fetch_assoc()) {
        echo "ID: " . $row["id"] . " - Name: " . $row["name"] . " - Email: " . $row["email"] . " - Age: " . $row["age"] . "<br>";
    }
} else {
    echo "No records found.";
}
?>

```

![[Pasted image 20241124234357.png]]

![[Pasted image 20241124234407.png]]

![[Pasted image 20241124234417.png]]

Full Example Script:
```php
<?php
// Database connection
$servername = "localhost";
$username = "root";
$password = "";
$dbname = "testdb";
$conn = new mysqli($servername, $username, $password, $dbname);
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}

// CREATE Table
$sql = "CREATE TABLE IF NOT EXISTS Users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    age INT
)";
$conn->query($sql);

// INSERT Data
$sql = "INSERT INTO Users (name, email, age) VALUES ('John Doe', 'john@example.com', 25)";
$conn->query($sql);

// SELECT Data
$sql = "SELECT id, name, email, age FROM Users";
$result = $conn->query($sql);
while ($row = $result->fetch_assoc()) {
    echo "ID: " . $row["id"] . " - Name: " . $row["name"] . " - Email: " . $row["email"] . " - Age: " . $row["age"] . "<br>";
}

// UPDATE Data
$sql = "UPDATE Users SET age = 30 WHERE name = 'John Doe'";
$conn->query($sql);

// DELETE Data
$sql = "DELETE FROM Users WHERE name = 'John Doe'";
$conn->query($sql);

// Close connection
$conn->close();
?>

```
![[Pasted image 20241124234428.png]]
