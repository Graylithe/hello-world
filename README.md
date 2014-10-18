hello-world
===========

My first repo
<!DOCTYPE html>
<html lang="en-US">
   <HEAD>
      <TITLE>
         A Small Hello 
      </TITLE>
   </HEAD>
<BODY>

	<?php
		//php code;
		echo "PHP code start.";
		// Create connection
		$con=mysqli_connect("localhost", "root", "", "studydatabase");

		// Check connection
		if (mysqli_connect_errno()) {
		  echo "Failed to connect to MySQL: " . mysqli_connect_error();
		}
		
		$result = mysqli_query($con, "SELECT * FROM incrementtable", MYSQLI_USE_RESULT);
		//$result = mysqli_query("SELECT * FROM 'unittable'");
		while($row = mysqli_fetch_array($result)) {
		  echo $row['primkey'] . " : " . $row['name'];
		  echo "<br>";
		}
		
	?>

	<H1>Hi</H1>
	<P title="About W3Schools">HTML code</P> 
</BODY>
</HTML>
