<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PEARSONAL BIO</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 300px;
        }
        h1 {
            color: #4CAF50;
        }
        img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin: 20px 0;
        }
        p {
            font-size: 18px;
            margin: 5px 0;
        }
        button {
            background-color: #4CAF50;
            color: white;
            border: none;
            padding: 10px;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 20px;
        }
        button:hover {
            background-color: #45a049;
        }
    </style>
</head>
<body>
    <div class="container" id="bioContainer">
      <B> <h1 style="color:Tomato;">WEL-COME MY BIO</h1></B>
        <img id="profilePic" src="https://i.sstatic.net/l60Hf.png" alt="Profile Picture">
        <p id="userName">Name: Not Provided</p>
        <p id="userProfession">Profession: Not Provided</p>
        <button onclick="updateBio()">Update Bio</button>
    </div>

    <script>
        
        function updateBio() {
            
            let name = prompt("ENTER YOUR NAME:-");
            let profession = prompt("ENTER YOUR PROFESSION:");
            let profilePicUrl = prompt("ENTER A URL PROFILE PICTURE:-");

           
            if (!name || !profession || !profilePicUrl) {
                alert("All fields are required!");
                return; 
            }

            
            alert(`NAME:- ${name}\nProfession: ${profession}\nProfile Picture URL: ${profilePicUrl}`);

           
            console.log("User Bio Details:");
            console.log(`NAME:- ${name}`);
            console.log(`PROFESSION:- ${profession}`);
            console.log(`PROFILE PICTURE URL: ${profilePicUrl}`);

           
            document.getElementById("userName").textContent = `NAME: ${name}`;
            document.getElementById("userProfession").textContent = `Profession: ${profession}`;
            document.getElementById("profilePic").src = profilePicUrl;

            
            document.querySelector("button").textContent = "Update Bio Again";
        }
    </script>
</body>
</html>
