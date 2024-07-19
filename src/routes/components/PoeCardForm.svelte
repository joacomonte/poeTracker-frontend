<script>
    let formData = $state({
      username: '',
      email: '',
      password: ''
    });
  
    function handleSubmit() {
      console.log('Form submitted:', formData);
      // Here you would typically send the data to a server
      alert('Form submitted!');
    }
  </script>
  
  <form onsubmit={handleSubmit}>
    <div>
      <label for="username">Username:</label>
      <input 
        id="username" 
        type="text" 
        bind:value={formData.username} 
        required
      />
    </div>
    
    <div>
      <label for="email">Email:</label>
      <input 
        id="email" 
        type="email" 
        bind:value={formData.email} 
        required
      />
    </div>
    
    <div>
      <label for="password">Password:</label>
      <input 
        id="password" 
        type="password" 
        bind:value={formData.password} 
        required
      />
    </div>
    
    <button type="submit">Register</button>
  </form>
  
  <style>
    form {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      max-width: 300px;
      margin: 0 auto;
    }
  
    label {
      font-weight: bold;
    }
  
    input {
      width: 100%;
      padding: 0.5rem;
    }
  
    button {
      background-color: #4CAF50;
      color: white;
      padding: 0.5rem;
      border: none;
      cursor: pointer;
    }
  
    button:hover {
      background-color: #45a049;
    }
  </style>