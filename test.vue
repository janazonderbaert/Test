<template>
    <div class="library-page">
      <header class="header">
        <div class="top-nav">
          <button class="sign-in">Sign in</button>
          <button class="register">Register</button>
        </div>
        <h1>Bibliotheek Sint-Lukas</h1>
      </header>
  
      <main class="content">
        <h2 class="best-choice">Best Choice</h2>
        <h1 class="books-title">BOOKS FOR ALL</h1>
        <input type="text" class="search-input" placeholder="Enter" />
  
        <div class="books">
          <div class="book book-audiovisual">AUDIOVISUAL ART</div>
          <div class="book book-architecture">ARCHITECTURE</div>
          <div class="book book-visual">VISUAL ART</div>
        </div>
      </main>
  
      <footer class="footer">
        <div class="social-icons">
          <i class="icon-instagram"></i>
          <i class="icon-youtube"></i>
          <i class="icon-linkedin"></i>
        </div>
      </footer>
    </div>
  </template>
  
  <style scoped>
  .library-page {
    font-family: 'Arial', sans-serif;
    text-align: center;
    padding: 20px;
  }
  
  .header {
    text-align: center;
  }
  
  .top-nav {
    display: flex;
    justify-content: flex-end;
    gap: 10px;
  }
  
  .sign-in {
    background: lightgreen;
  }
  
  .register {
    background: black;
    color: white;
  }
  
  .books-title {
    font-size: 2em;
    margin: 10px 0;
  }
  
  .search-input {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  .books {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
  }
  
  .book {
    padding: 20px;
    font-size: 1.2em;
    font-weight: bold;
    transform: rotate(-10deg);
  }
  
  .book-audiovisual {
    background: lightgreen;
  }
  
  .book-architecture {
    background: orange;
  }
  
  .book-visual {
    background: lightgray;
  }
  </style>
