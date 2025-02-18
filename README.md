<!DOCTYPE html>
<html>
    <head>
        <title>CONTACT-FORM-MAIN</title>
        <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
        <style>
            body{
                background-color: hsl(148, 38%, 91%);
                width: 1440px;
                height: 100vh;
            }
            form{
                padding-left: 50%;
                background-color: white;
                margin-left: 35%;
                width: 450px;
                height: 700px;
                padding-left: 50px;
                padding-right: 50px;
                margin-top: 50px;
                border-radius: 10px;
            }
            h1{
                font-size: 40px;
                font-weight: bolder;
            }
            .form-group{
                display: flex;
                flex-direction: row;
                justify-content: space-between;
                font-size: 20px;
                color: hsl(187, 24%, 22%); 
                
            }
            .form-group label{
                font-weight: bold;
                display: block;
                margin-bottom: 5px;
            }
            .form-group input{
                width: 100%;
                padding: 10px;
                border: 1px solid #ccc;
                border-radius: 4px;
                cursor: pointer;
            }
            .two{
                margin-bottom: 0px;
                
            }
            .two label{
                font-size: 20px;
                font-weight: bold;
                display: block;
                margin-bottom: 0px;
                color:  hsl(187, 24%, 22%);
            }
            .two input{
                width: 100%;
                padding: 10px;
                border: 1px solid #ccc;
                border-radius: 4px;
                cursor: pointer;
            }
            .one{
                display: flex;
                flex-direction: row;
                justify-content: space-evenly;
                color:  hsl(187, 24%, 22%);;
            }
            .one input{
                font-size: 15px;
                font-weight: bold;
                width: 80%;
                padding: 10px;
                border: 1px solid #ccc;
                border-radius: 4px;  
                cursor: pointer;
            }
            .three{
                font-size: 20px;
                font-weight: bold;
                padding-bottom: 0px;
                color:  hsl(187, 24%, 22%);
            }
            
            .form-text{
                font-size: 20px;
                font-weight: bold;
                color:  hsl(187, 24%, 22%);
            }
            textarea{
                width: 100%;
                padding: 10px;
               border-radius: 4px;
               border: 1px solid #ccc;
                
            }
            .four{
                margin-bottom: 15px;
                font-size: 25px;
                color:  hsl(187, 24%, 22%);;
            }
            .four input{
                width: 100%;
                padding: 5px;
                border: 1px solid #ccc;
                border-radius: 4px;
                background-color: hsl(169, 82%, 27%);
                color: white;
                font-size: 25px;
                margin-top: 0px;
                cursor: pointer;
                border: none;
            }
            .four input:hover {
                background-color: hsl(169, 72%, 37%);
            }
                #successMessage{
                display: none;
                color:green;
                margin-top: 20px;
            }
            .one i {
            font-size: 20px;
            color: gray;
        }
        .selected i {
            color: green;
        }
        .one div {
            display: flex;
            align-items: center;
            cursor: pointer;
        }
        </style>
    </head>
<body>
    <form id="myForm">
        <br>
        <h1>Contact Us</h1>
      <div class="form-group">
        <div class="five">
      <div>
         <label for="First Name">First Name</label>
      </div>
      <div>
         <input type=""  id="First name" name="First name">
      </div>
      </div>
      <div class="six">
        <div>
          <label for="Last Name">Last Name</label>
        </div>
        <div>
          <input type=""  id="Last name" name="Last name">
       </div>
    </div>
      </div>
      <br>
      <div class="two">
        <div>
         <label for="Email Address">Email Address</label>
        </div>
        <div>
         <input type=""  id="Email Address" name="Email Address">
        </div>
      </div>
      <br>
       <div class="three">
         <label for="Query Type">Query Type</label>
       </div>
         <div class="one">
            <div id="option1">
                <i class="fa fa-circle-o"></i>
                <input type="text" value="General Enquiry" readonly>
            </div>
            <br>
            <div id="option1">
                <i class="fa fa-circle-o"></i>
                <input type="text" value="Support Request" readonly>
            </div>
         </div>
       </div>
      <br>
      <div class="form-text">
        <div>
        <label for="Messages">Messages</label>
        </div>
        <div>
         <textarea id="Messages" name="Messages" rows="10"></textarea>
        </div>
        <p>
            <i id="consentIcon" class="fa fa-circle-o"></i>  i consent to being contacted by the team.
        </p>
        <div class="four">
         <input type="Submit" id="submitBtn" value="Submit">
        </div>
     </div>
     </form>
    
     <div id="successMessage">your message is saved</div>
     <script>
        document.getElementById("option1").addEventListener("click", function() {
            document.querySelector("#option1 i").classList.replace("fa-circle-o", "fa-check-circle");
            document.querySelector("#option1 i").style.color = "green";

            document.querySelector("#option2 i").classList.replace("fa-check-circle", "fa-circle-o");
            document.querySelector("#option2 i").style.color = "gray";
        });

        document.getElementById("option2").addEventListener("click", function() {
            document.querySelector("#option2 i").classList.replace("fa-circle-o", "fa-check-circle");
            document.querySelector("#option2 i").style.color = "green";

            document.querySelector("#option1 i").classList.replace("fa-check-circle", "fa-circle-o");
            document.querySelector("#option1 i").style.color = "gray";
        });

        
        document.getElementById("consentIcon").addEventListener("click", function() {
            this.classList.toggle("fa-circle-o");
            this.classList.toggle("fa-check-circle");
            this.style.color = this.classList.contains("fa-check-circle") ? "green" : "gray";
        });

    
        document.getElementById("myForm").addEventListener("submit", function(event) {
            event.preventDefault(); 

            
            document.getElementById("successMessage").style.display = "block";
        });
     </script>
</body>
</html>
