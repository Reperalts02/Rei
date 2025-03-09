<template>
    <div class="confirmation-window">
      <h1>On The Go! Go! Go!</h1>
      <p>Enter The Confirmation Code</p>
      <input
        type="text"
        placeholder="Confirmation Code"
        v-model="code"
        class="input-field"
      />
      <button @click="confirmCode" class="confirm-btn">
        Recover Account
      </button>
      <p class="resend">
        Didn't receive Confirmation Code?
        <span @click="resendCode" class="resend-link">Resend Now</span>
      </p>
    </div>
  </template>
  
  <script>
  export default {
    name: "Confirmation",
    data() {
      return {
        code: "",
      };
    },
    methods: {
      confirmCode() {
        alert(`Code Entered: ${this.code}`);
      },
      resendCode() {
        alert("Confirmation code resent!");
      },
    },
  };
  </script>
  
  <style scoped>
  .confirmation-window {
    max-width: 400px;
    margin: auto;
    padding: 20px;
    text-align: center;
    background: #ffffff;
    border-radius: 16px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  }
  
  h1 {
    font-size: 28px;
    color: #333;
  }
  
  .input-field {
    width: 100%;
    padding: 10px;
    margin: 10px 0;
    border: 1px solid #ccc;
    border-radius: 10px;
  }
  
  .confirm-btn {
    width: 100%;
    padding: 10px;
    background: black;
    color: white;
    border: none;
    border-radius: 10px;
    cursor: pointer;
  }
  
  .confirm-btn:hover {
    background: purple;
  }
  
  .resend {
    margin-top: 10px;
    color: #555;
  }
  
  .resend-link {
    color: purple;
    cursor: pointer;
    text-decoration: underline;
  }
  </style>