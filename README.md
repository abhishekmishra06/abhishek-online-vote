<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=Edge">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <title>Online Voting</title>
  
  <!-- HTML -->
  

  <!-- Custom Styles -->
  <link rel="stylesheet" href="style.css" >
</head>

<body>
  <style type="text/css">
    
    body {
    font-size: 15px;
    background: olive;
    } 
    input[type="text"]{
      border-radius: 15px;
      padding: 5px;
    }
    input[type=number]{
      border-radius: 15px;
      padding: 5px;
    }
    label{
      font-size: 15px;
      font-family: sans-serif;
      color: black;
    }
    div{
 background-image: linear-gradient(red,yellow,green);
 background-size: 5px;
    }
    input[type="submit"]{
      border: 5px;
      padding: 10px;
      border-radius: 5px;
    }
    h2{
      text-align: center;
    }
    #sub{
      background: cyan;
      color: black;
      font-size: 15px;
    }
    marquee{
      font-size: 20px;
      color: black;
    }
    #profile{
        border-radius: 15px;
        padding:10px;
        animation: profile 1s infinite;
    }
    @keyframes profile{
        from{
            background-color:aqua;
        }
    }
  </style>
  
<h2>ONLINE VOTING</h2><hr>
<div>
<label>Surname:</label><br>
<input type="text" id="name" name="Sur" required/>
<br><label>Last name:</label>
<br><input type="text" class="form" id="name" required/><br>
<label>Email:</label><br>
<input type="text" class="form" name="email" required/><br>
<label>Voter Id:</label><br>
<input type="number"  id="voterid" class="form" name="voter" required/><br>
Select Party:
<select id="party" class="form">
<option value="NPP">NPP</option> 
<option value="NDC">NDC</option>
<option value="GUM">GUM</option>
<option value="CPP">CPP</option>
<option value="NDP">NDP</option>
<option value="PPP">PPP</option>
<option value=""></option>
</select><br><small>
  
<input type="radio" name="Gender" value="male">Male<br>
<input type="radio" name="Gender" value="female">Female<br></small>
<small><input type="checkbox" id="check" class="check"/>
You agree to our terms and conditions</small>
<input type="submit" id="sub" onclick="sub()">
</div><br>
<div id="dj"></div><br>
 <button id="profile">
  <a href="  https://www.sololearn.com/Profile/20084575/?ref=
             app">Follow Me</a><br>
    </button>
<marquee>Made By:💥 DARKWA JOHN💥
    😎😎
</marquee>
  <!-- Project -->
  <script src="main.js"></script>
  <script src="https://code.jquery.com/jquery-3.1.1.js"></script>
  <script>
$(function() {
$("<table class='table table-stripped'><thead> <th>Name</th><th>Voterid</th> <th>Party</th> </thead></table> ").appendTo("#dj");
        $("#check").click(function(){
           $("#sub").attr("disabled", !this.checked);
        });
        $("#sub").click(function(){
            var nm = $("#name").val();
            var vid = $("#voterid").val();
            var py = $("#party").val();
            $(" <tr><td>"+nm+"</td><td>"+vid+"</td><td>"+py+"</td></tr>").appendTo("thead");
        });

});
  </script>
</body>
</html>
