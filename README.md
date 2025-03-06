# Simple Registration Form In CodeIgniter With Database

A **Simple Registration Form in CodeIgniter with Databas**e is a list of fields where a person can enter information and send it to a company or person.

You might want someone to fill out a registration form for many different reasons. Companies use registration forms to get customers to sign up for subscriptions, services, or other programs or plans.

## About the Project

This **Simple Registration Form in CodeIgniter** is  developed using **CodeIgniter and MySQL Database as Back-End**.

In this article, we’ll learn how to use CodeIgniter to develop a simple registration form.

The information will be stored in the database. To save data, we’ll utilize a user table.

In this **Registration Form CodeIgniter** you can learn how to create a registration form in CodeIgniter, this Project has functionality in which the user can register the account, store it in the MySQL Database, and display the data in the table.

## What is CodeIgniter?

CodeIgniter is an Application Development Framework – a toolset – for PHP website developers.

Its purpose is to let you construct projects much faster than if you were programming code from the start by providing a rich set of libraries for common activities, as well as a simple interface and logical structure to access these libraries.

By reducing the amount of code required for a given operation, CodeIgniter allows you to focus more creatively on your project.

In this Registration Form in CodeIgniter With Validation also includes a downloadable CodeIgniter Project With Source Code for free, just find the downloadable source code below and click to start downloading.

To start executing this Simple Registration Form In CodeIgniter With Database, make sure that you have sublime or any platform of PHP and MySQL installed on your computer.

## How to Run the Simple Registration Form in CodeIgniter With Database?

These are the steps on how to run the Simple Registration Form in CodeIgniter With Database.

1. **Download Source Code**

2. **Extract File**

Next, after finishing downloading the file, go to the file location, right-click the file, and click “Extract Here.”

![image](https://github.com/user-attachments/assets/fc2fd26a-3623-4de2-ba6d-a47d22854468)

3. **Copy Project Folder**

Next, copy the project folder and paste it to C:\xampp\htdocs.

4. Open Xampp

Next, open xampp and start the Apache and mysql.

![image](https://github.com/user-attachments/assets/2d679b95-e527-4045-a404-eaf66a170f25)

5. **Create Database**

Next, click any browser type the URL localhost/phpmyadmin, and create a database.

![image](https://github.com/user-attachments/assets/6b768969-9796-4783-b166-5b7376ae3446)

6. **Import Database**

Next, click the created database click import to the right tab click choose file, and import the sql file inside the download folder.

![image](https://github.com/user-attachments/assets/ac485a41-98ef-4be8-8a58-c4253bb0c2ad)


7. **Execute Project**

Lastly , type to the URL localhost/codeigniter_register.

## How to Create a Simple Registration Form in CodeIgniter With Database

The code given below is for the registration form module

### views: register_form.php

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<title>CodeIgniter Signup with Validation (IT SOURCECODE)</title>
	<link rel="stylesheet" type="text/css" href="<?php echo base_url(); ?>bootstrap/css/bootstrap.min.css">
	<script src="<?php echo base_url(); ?>jquery/jquery.min.js"></script>
	<script src="<?php echo base_url(); ?>bootstrap/js/bootstrap.min.js"></script>
</head>
<body class="bg-info">
<div class="container">
	<h1 class="page-header text-center">CodeIgniter Signup with Validation (IT SOURCECODE)</h1>
	<div class="row">
		<div class="col-sm-4">
			<div class="login-panel panel panel-primary">
		        <div class="panel-heading">
		            <h3 class="panel-title"><span class="glyphicon glyphicon-user"></span> Register
		            </h3>
		        </div>
		    	<div class="panel-body">
		        	<form id="regForm">
		            	<fieldset>
		                	<div class="form-group">
		                    	<input class="form-control" placeholder="Email" type="text" name="email">
		                	</div>
		                	<div class="form-group">
		                    	<input class="form-control" placeholder="Password" type="password" name="password">
		                	</div>
		                	<div class="form-group">
		                    	<input class="form-control" placeholder="Full Name" type="text" name="fname">
		                	</div>
		                	<button type="submit" class="btn btn-lg btn-primary btn-block">Sign Up</button>
		            	</fieldset>
		        	</form>
		    	</div>
		    </div>
		    <div id="responseDiv" class="alert text-center" style="margin-top:20px; display:none;">
				<button type="button" class="close" id="clearMsg"><span aria-hidden="true">&times;</span></button>
				<span id="message"></span>
			</div>
		</div>
		<div class="col-sm-8">
			<table class="table table-bordered table-striped">
				<thead>
					<tr>
						<th>ID</th>
						<th>Email</th>
						<th>Password</th>
						<th>FullName</th>
					</tr>
				</thead>
				<tbody id="tbody">
				</tbody>
			</table>
		</div>
	</div>
</div>
<script type="text/javascript">
	$(document).ready(function(){
		getTable();

		$('#regForm').submit(function(e){
			e.preventDefault();
			var url = '<?php echo base_url(); ?>';
			var reg = $('#regForm').serialize();
			$.ajax({
				type: 'POST',
				data: reg,
				dataType: 'json',
				url: url + 'index.php/user/register',
				success:function(response){
					$('#message').html(response.message);
					if(response.error){
						$('#responseDiv').removeClass('alert-success').addClass('alert-danger').show();
					}
					else{
						$('#responseDiv').removeClass('alert-danger').addClass('alert-success').show();
						$('#regForm')[0].reset();
						getTable();
					}
				}
			});
		});

		$(document).on('click', '#clearMsg', function(){
			$('#responseDiv').hide();
		});

	});
	function getTable(){
		var url = '<?php echo base_url(); ?>';
		$.ajax({
			type: 'POST',
			url: url + 'index.php/user/fetch',
			success:function(response){
				$('#tbody').html(response);
			}
		});
	}
</script>
</body>
</html>
```

## Project Output:

![image](https://github.com/user-attachments/assets/6e1dc865-ec9e-4911-9753-9eb3ed571a76)

### 📌 Here's the full documentation for the [Simple Registration Form In CodeIgniter](https://itsourcecode.com/free-projects/php-project/simple-registration-form-in-codeigniter-with-database/)


