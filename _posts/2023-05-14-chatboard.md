<!DOCTYPE html>
<html>
<head>
  <title>Chatboard</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f7f7f7;
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      flex-direction: column;
    }
    .chatbox {
      width: 500px;
      background-color: #f7f7f7;
      border-radius: 20px;
      padding: 20px;
      box-shadow: 8px 8px 16px #d9d9d9, -8px -8px 16px #ffffff;
      margin: auto;
    }
    .message {
      margin-bottom: 10px;
      position: relative;
    }
    .user {
      color: #007bff;
      font-weight: bold;
      display: inline-block;
    }
    .user-message {
      display: inline-block;
      margin-left: 5px;
    }
    .timestamp {
      font-size: 0.8em;
      color: #888;
      position: absolute;
      right: 0;
      bottom: 0;
    }
    input[type="text"] {
      width: 95%;
      padding: 12px;
      border: none;
      border-radius: 10px;
      background-color: #f7f7f7;
      box-shadow: inset 6px 6px 12px #d9d9d9, inset -6px -6px 12px #ffffff;
    }
    button {
      padding: 12px;
      margin-top: 10px;
      background-color: #007bff;
      color: #fff;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 6px 6px 12px #d9d9d9, -6px -6px 12px #ffffff;
      width: 100%;
    }
    .username-box {
      width: 500px;
      background-color: #f7f7f7;
      border-radius: 20px;
      padding: 20px;
      box-shadow: 8px 8px 16px #d9d9d9, -8px -8px 16px #ffffff;
      margin-top: 5px;
    }
    .username-input {
      width: 70%;
      padding: 8px;
      border: none;
      border-radius: 10px;
      background-color: #fff;
      box-shadow: inset 4px 4px 8px #d9d9d9, inset -4px -4px 8px #ffffff;
      margin-right: 10px;
    }
    .submit-username {
      padding: 8px;
      background-color: #007bff;
      color: #fff;
      border: none;
      border-radius: 10px;
      cursor: pointer;
      box-shadow: 4px 4px 8px #d9d9d9, -4px -4px 8px #ffffff;
    }
  </style>
</head>
<body>
<h2>Chatboard</h2>
  <div class="username-box">
      <h4 style="text-align: center;" >Pick your Username</h4>
      <input type="text" id="username-input" placeholder="Enter your username..." />
      <button class="submit-username" onclick="submitUsername()">Submit</button>
    </div>

  <div class="chatbox">
    <div id="messages">
      <!-- Chat messages will be dynamically added here -->
    </div>
    <div>
        <input type="text" id="input-message" placeholder="Type your message..." />
        <button onclick="sendMessage()">Send</button>
      </div>
    </div>
    <script>
      function sendMessage() {
        var inputMessage = document.getElementById('input-message').value;
        document.getElementById('input-message').value = '';
  
        var messageElement = document.createElement('div');
        messageElement.classList.add('message');
  
        // Create user element
        var userElement = document.createElement('span');
        userElement.classList.add('user');
        userElement.textContent = getSelectedUsername() + ': ';
  
        // Create user message element
        var userMessageElement = document.createElement('span');
        userMessageElement.classList.add('user-message');
        userMessageElement.textContent = inputMessage;
  
        // Create timestamp element
        var timestampElement = document.createElement('span');
        timestampElement.classList.add('timestamp');
        timestampElement.textContent = getCurrentTime();
  
        // Append user, user message, and timestamp elements to the message element
        messageElement.appendChild(userElement);
        messageElement.appendChild(userMessageElement);
        messageElement.appendChild(timestampElement);
  
        // Append the message element to the messages container
        document.getElementById('messages').appendChild(messageElement);
      }
  
      function submitUsername() {
        var username = document.getElementById('username-input').value;
        localStorage.setItem('selectedUsername', username);
      }
  
      function getSelectedUsername() {
        return localStorage.getItem('selectedUsername') || 'Anonymous';
      }
  
      function getCurrentTime() {
        var now = new Date();
        var hours = now.getHours();
        var minutes = now.getMinutes();
        var ampm = hours >= 12 ? 'PM' : 'AM';
        hours = hours % 12;
        hours = hours ? hours : 12;
        minutes = minutes < 10 ? '0' + minutes : minutes;
        var currentTime = hours + ':' + minutes + ' ' + ampm;
        return currentTime;
      }
    </script>
  </body>
  </html>
  