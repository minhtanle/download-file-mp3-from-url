# download-file-mp3-from-url
download-file-mp3-from-url

```php
<?php 
	// Use this to directly download files, rather than play/view them in the browser
	// Save this as a file in the same directory as the file to be downloaded, e.g., direct-download.php
 ?>

<?php
  //Example : https://domain-name.com/audio/audio.mp3

  $remote_url = "https://domain-name.com/audio/";
	$file = $remote_url . $_GET['filename'];
	header ("Content-type: octet/stream");
	header ("Content-disposition: attachment; filename=".$_GET['filename'].";");
	header("Content-Length: ".filesize($file));
	readfile($file);
	exit;
?>

<!-- then use this link format in your webpage to link to the download, replace filename as appropriate -->
 <a href="http://URL-to-dowbload/direct-download.php?filename=audio.mp3">Download the mp3</a>
```
