---
permalink: /terms.html
---

<html>
<head>
<script src="http://code.jquery.com/jquery-1.11.0.min.js"></script>
<script type="text/javascript">
 $(document).ready(function(){
    $('#targets').submit(function() {
        var error = 0;
        if (!($('#checkboxid').is(':checked'))) {
            error = 1
            alert("Please Tick the Agree to Terms of Use");
        }

        if (error) {
            return false;
        } else {
            return true;
        }

    });
});
</script>
</head>
<body>

                    <div class="checkbox">
                      <label for="agree">
                        <input type="checkbox" name="agree" id="agree" />
                        I have read, understood, and hereby agree to the <a href="#" target="_blank"><u>Terms and Conditions of Sale</u></a>.
                      </label>
                    </div>
                    <span class="error-agree-ocst">
                      <div class="alert alert-danger ocst-agree" role="alert">
                          Please accept the shipping disclaimer.
                      </div>
                    </span>
                    <button class="btn btn-primary btn-checkout btn-lg" type="submit">Continue</button>

<script>
  $("#ocst_form").submit(function(e){
		if($('#agree').is(':checked')) {
	        $('#ocst_form').submit();
	   } else{
	   		e.preventDefault();
	   		$('.error-agree-ocst').fadeIn('slow');
	   		$('.error-agree-ocst').fadeOut('slow');
	   }
	});
</script>
</body>
</html>