<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width" />
    <title>Create</title>
    <link href="/Content/bootstrap.css" rel="stylesheet"/>
<link href="/Content/site.css" rel="stylesheet"/>

    <script src="/Scripts/modernizr-2.6.2.js"></script>

</head>
<body>
    <div class="container body-content" id="form-group">
        


<h2>Welcome to MBEC!</h2>

  <form class="gform pure-form pure-form-stacked" method="POST" data-email="example@email.net"
  action="https://script.google.com/macros/s/AKfycbynMvuU6o0JkNte-0Z2kIDahDkWvO2nHlkxPG_-RA/exec">
        <h4>How Was You Experience?</h4>
        <hr />
        

        
        <div id="contents">
            <div id="rate">
                <label style="font-size:400%;" class="star" id="r1"  onclick="star1()">  <input data-val="true" data-val-number="The field Rating must be a number." data-val-required="The Rating field is required." id="Rating" name="Rating" type="radio" value="1" /> ☆ </label>

                <label style="font-size:400%;" class="star" id="r2" onclick="star2()"> <input id="Rating" name="Rating" type="radio" value="2" /> ☆ </label>

                <label style="font-size:400%;" class="star" id="r3" onclick="star3()"> <input id="Rating" name="Rating" type="radio" value="3" /> ☆ </label>

                <label style="font-size:400%;" class="star" id="r4" onclick="star4()"> <input id="Rating" name="Rating" type="radio" value="4" /> ☆ </label>

                <label style="font-size:400%" class="star" id="r5" onclick="star5()"> <input id="Rating" name="Rating" type="radio" value="5" /> ☆ </label>
            </div>
        

        <div id="fade2" style="display:none">
            <label>Comments</label>
            <div>
                <textarea cols="20" id="message" name="message" rows="2"> </textarea>
                <span class="field-validation-valid text-danger" data-valmsg-for="message" data-valmsg-replace="true"></span>
            </div>
        </div>

        <div class="form-group" id="fade3" style="display:none">
                <input type="submit" value="Submit Rating" onclick="myFunction()" />
        </div>
    </div>
      
      
       <!-- Customise the Thankyou Message People See when they submit the form: -->
          <div class="thankyou_message" style="display:none;">
      <h2>thank you for your submission!</h2>
        <p><a href="SurveyPage.html"> click here to return to the survey! </a></p>
    </div>

</form>
    

          <!-- Submit the Form to Google Using "AJAX" -->
  <script data-cfasync="false" type="text/javascript"
  src="form-submission-handler.js"></script>

<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>

<script>

    $(".star").click(function () {
        $("#fade1").slideDown("slow");
        $("#fade2").slideDown("slow");
        $("#fade3").slideDown("slow");
        
    });

    $("#r1,#r2,#r3,#r4,#r5").click(function () {
        $("#r1,#r2,#r3,#r4,#r5").animate({
            fontSize: "400%"
            },1000);
    });

    function myFunction() {
        document.getElementById("contents").style.display="none";
    }

    function star1() {
        var all = document.getElementById("rate").querySelectorAll(".star");
        var stars = document.getElementById("r1");
        if (stars.style.color = "black") {
            stars.style.color = "gold";
        }

        if (document.getElementById("r2").style.color = "gold") {
            document.getElementById("r2").style.color = "black";
            document.getElementById("r3").style.color = "black";
            document.getElementById("r4").style.color = "black";
            document.getElementById("r5").style.color = "black";
        }



    }

    function star2() {
        star1();
        var stars = document.getElementById("r2");
        stars.style.color = "gold";
    }

    function star3() {
        star1();
        star2();
        var stars = document.getElementById("r3");
        stars.style.color = "gold";
    }

    function star4() {
        star1();
        star2();
        star3();
        var stars = document.getElementById("r4");
        stars.style.color = "gold";
    }

    function star5() {
        star1();
        star2();
        star3();
        star4();
        var stars = document.getElementById("r5");
        stars.style.color = "gold";
    }
</script>

<style>
    #form-group{
        margin: 0 auto;
        text-align:center;
        width: 50%;
    }
    
    #rate{
        width: 100%;
    }

    label input {
        visibility: hidden;
    }

/*
    #rate, #fade3{   
        padding-left: 35%;
        
    }
    #fade1, #fade2{
        padding-left: 25%;
    }
*/

    #rate:hover {
        color: gold;
    }

    .star:hover ~ .star {
        color: black;
    }

    .star.checked {
        background-color: gold;
    }

    .rating.checked ~ label input {
        background: #ff0000;
        color: gold;
    }

    .navbar {
        //visibility:hidden;
    }

    body {
/*        background: url(http://i.imgur.com/AbmZDdM.png) no-repeat center center fixed;*/
        background-size: 100% 100%;
        background-repeat: no-repeat;
    }

    #r1{
       font-size: 500%;
    }

    #message{
        height: 150px;
        width: 300px;
    }
</style>
    <div>
        <hr />
        <footer>
            <p>&copy; Created by Tyshaun Jones-Tyrell</p>
        </footer>
    </div>


</body>
</html>
