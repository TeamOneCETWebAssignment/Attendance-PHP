# Simple Attendance System in PHP, MySQL and Bootstrap

## Installation

Here are the steps you will need to complete in order to get it working.

**Step 1: Create a MySQL database.**

* Server:   localhost
* Database: attendance
* Username: root
* Password: [blank]

Edit the db-connect.php file to change these credentials.

**Step 2: Use the following SQL to create the tables.**

	CREATE TABLE `user` (
	  `id` int NOT NULL AUTO_INCREMENT,
	  `fullname` text NOT NULL,
	  `email` text NOT NULL,
	  `role` text NOT NULL,
	  `class` text NOT NULL,
	  PRIMARY KEY (id)
	);

	CREATE TABLE `class` (
	  `id` int NOT NULL AUTO_INCREMENT,
	  `name` text NOT NULL,
		PRIMARY KEY (id),
	   UNIQUE KEY (name(255))
	);

	CREATE TABLE `attendance` (
	  `studentid` int NOT NULL,
	  `classid` int NOT NULL,
	  `session` int NOT NULL,
	  `ispresent` int NOT NULL
	);

**Step 3: Setup the website.**

The first time you try to access the website, you will be prompted to create an Administrator account. This is the only time you will be able to do this from within Attendance System.

Next:

* Register teachers.
* Register students.
