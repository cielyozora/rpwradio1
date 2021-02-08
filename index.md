<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
<meta name="viewport" content="width=device-width">
<title>RPWRADIO1 SUBMISSION SITE</title>
<link rel="stylesheet" type="text/css" href="view.css" media="all">
<script type="text/javascript" src="view.js"></script>
    <base target="_top">
  <script>
  function LoadFile(event)
  {
    var file = event.target.files[0];
    var reader = new FileReader();
    reader.onload = function(e) {
      console.log(e.target.result);
      var fileData = e.target.result.substr(e.target.result.indexOf(",")+1);
      var mimeTypeStart = e.target.result.indexOf("data:") + 5;
      var mimeTypeEnd = e.target.result.indexOf(";");
      var mimeType = e.target.result.substr(mimeTypeStart, mimeTypeEnd - mimeTypeStart);
      var fileName = file.name;
      document.getElementById("fileData").value = fileData;
      document.getElementById("mimeType").value = mimeType;
      document.getElementById("fileName").value = fileName;
    };    
    reader.readAsDataURL(file);
  }
  </script>

</head>
<body id="main_body" >
	
	<img id="top" src="banner.png" alt="">
	<div id="form_container">
	
		<h1><a>RPW RADIO1</a></h1>
		<?var url = getUrl();?>
		<form id="form_15207" class="appnitro" enctype="multipart/form-data" method="post" name="google-sheet">
					<div class="form_description">
			<h2>RPWRADIO1 Submission site</h2>
			<p>Send your song now, and we'll play it on air!</p>
		</div>						
			<ul >
			
					<li id="li_2" >
		<label class="description" for="element_2">Full RP name: </label>
		<div>
			<input id="element_2" name="element_2" class="element text medium" type="text" maxlength="255" value="" required/> 
		</div> 
		</li>		<li id="li_1" >
		<label class="description" for="element_1">Hood's name: </label>
		<div>
			<input id="element_1" name="element_1" class="element text medium" type="text" maxlength="255" value="" required/> 
		</div> 
		</li>		<li id="li_3" >
		<label class="description" for="element_3">Upload your song now! </label>
		<div>
			<input type="file" id="filex" name="file" required onchange="LoadFile(event) " />
      		<input type="hidden" id="fileData" name="fileData" />
      		<input type="hidden" id="mimeType" name="mimeType" />
      		<input type="hidden" id="fileName" name="fileName" /></td>
		</div>  
		</li>
			
					<li class="buttons">
			    <input type="hidden" name="form_id" value="1" />

			    
				<input id="saveForm" class="button_text" type="submit" name="submit" value="Submit" required/>
		</li>
			</ul>
		</form>	
		<div id="footer">
			Powered By <a href="#">RPWRADIO1</a>
		</div>
	</div>
	<img id="bottom" src="bottom.png" alt="">
	</body>
	<script>
            const scriptURL = 'https://script.google.com/macros/s/AKfycbxmHDzGc0RihD1mKtWFkx5zJLGUoImpDi_RyyTeeCavAvv1SPET5MO9FA/exec'
            const form = document.forms['google-sheet']
          
            form.addEventListener('submit', e => {
              e.preventDefault()
              fetch(scriptURL, { method: 'POST', body: new FormData(form)})
              	window.location.replace("https://facebook.com/rpwradio.official");
              //  .then(response => alert("Thanks for Contacting us..! We Will Contact You Soon..."))
              // .catch(error => console.error('Error!', error.message))
            })
          </script>
          <script>
function myFunction() {
  var x = document.getElementById("filex").required;
  document.getElementById("demo").innerHTML = x;
}
</script>

        <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.1.1/js/bootstrap.min.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
</html>
