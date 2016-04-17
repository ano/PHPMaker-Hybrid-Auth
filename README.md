# PHPMaker-Hybrid-Auth
PHPMaker Hybrid Auth Template

A PHPMaker file with the HybridAuth authentication library http://hybridauth.sourceforge.net/ 

Based on the following tutorial
https://hasin.me/2014/02/10/integrate-social-sign-on-in-your-php-apps-using-hybridauth/

#Manual Setup
1. Create a new PHPMaker Project
2. Click on a table, in the Code(Server Events, Client Scripts and Custom Templates) tab, add this to the function Page_DataRendering
```php
// Page Data Rendering event
function Page_DataRendering(&$header) {
	/* 
		Description: Adds a login button to the login screen
		Source: http://tech.yeesiang.com/social-login-button-with-font-awesome-bootstrap/
	*/
	$header = '
				<div class="row form-horizontal ewForm ewLoginForm">
				   		<div class="col-sm-offset-2 col-sm-10">
				   			<div class="btn-group">
				   				<a class="btn btn-danger disabled"><i class="fa fa-google-plus" style="width:16px; height:20px"></i></a>
				   				<a class="btn btn-danger" href="" style="width:12em; height:37px"> Sign in with Google</a>
				   			</div>
				</div>
				<div class="row form-horizontal ewForm ewLoginForm">
					<h3 class="col-sm-offset-2 col-sm-10">OR</h3>
					<hr style="width: 66%; float: left;">
				</div>
			  ';
}
 ```
 
3. Create 3 custom files in PHPMaker

 - hybrid.php
 - google.php
 - composer.json
