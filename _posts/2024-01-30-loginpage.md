---
toc: False
layout: post
hide: False
title: Login and Signup Page
courses: {compsci: {week: 20}}
permalink: /login
type: hacks
---

<style>
 #login {
    margin-top: 10px;
    padding-top: 0.75rem;
    padding-bottom: 0.75rem;
    padding-left: 1rem;
    padding-right: 1rem;
    text-align: center;
    width:100%;
}
.login-container {
  border: 3px solid #f1f1f1;
}

input[type=text], input[type=password] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  box-sizing: border-box;
}

button {
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  cursor: pointer;
  width: 50%;
  margin-left: 200px;
}

.imgcontainer {
  text-align: center;
  margin: 24px 0 12px 0;
}

img.avatar {
  width: 40%;
  border-radius: 50%;
}

.container {
  padding: 16px;
}

span.psw {
  display: flex;
  justify-items: center;
  text-align: center;
  margin-left: 325px;
  padding-top: 16px;
}

@media screen and (max-width: 300px) {
  span.psw {
    display: block;
    float: none;
  }
  .cancelbtn {
    width: 100%;
  }
}

</style>
<div class="login-container">
  </div>

<form action="javascript:login_user()">
    <label for="uid"><b>Username</b></label>
    <input type="text" id="uid" placeholder="Enter Username" name="uid" required>
    <label for="password"><b>Password</b></label>
    <input type="password" id="password" placeholder="Enter Password" name="password" required>
    <button class='button'>Log in</button>
    <div>
    <span class="psw"><a href="{{site.baseurl}}/signup"> Sign Up</a></span>
    </div>
  </div>
</form>
<script type="module">
    import { uri, options } from '{{site.baseurl}}/assets/js/api/config.js';
    function login_user(){
      var myHeaders = new Headers();
myHeaders.append("Content-Type", "application/json");
        const url = uri + '/api/users/authenticate';
        const body = {
            uid: document.getElementById("uid").value,
            password: document.getElementById("password").value,
        };
        const authOptions = { 
            ...options,
            method: 'POST', 
            cache: 'no-cache',
            body: JSON.stringify(body)
        };
        fetch(url, authOptions)
        .then(response => {
            if (!response.ok) {
                const errorMsg = 'Login error: ' + response.status;
                console.log(errorMsg);
                return;
            }
            window.location.href = "{{site.baseurl}}/";
        })
        .catch(err => {
            console.error(err);
        });
    }
    window.login_user = login_user;
</script>
