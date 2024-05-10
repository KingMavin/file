<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Login Page</title>
  <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
</head>
<body>
  <div id="app">
    <h2>Login</h2>
    <form @submit.prevent="login">
      <div>
        <label for="username">Username:</label>
        <input type="text" id="username" v-model="username" required>
      </div>
      <div>
        <label for="password">Password:</label>
        <input type="password" id="password" v-model="password" required>
      </div>
      <button type="submit">Login</button>
    </form>
    <p v-if="errorMessage" style="color: red;">{{ errorMessage }}</p>
  </div>

  <script>
    new Vue({
      el: '#app',
      data: {
        username: '',
        password: '',
        errorMessage: ''
      },
      methods: {
        login() {
          // Here you can add your login logic.
          // For simplicity, let's just check if username and password are not empty
          if (this.username === '' || this.password === '') {
            this.errorMessage = 'Please enter both username and password.';
          } else {
            // Successful login logic can go here
            alert('Login successful!');
            // You can redirect to another page or do something else here
          }
        }
      }
    });
  </script>
</body>
</html>
