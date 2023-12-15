<template>
    <footer>
      <p>&copy; 2023 Jk Expense tracker. <br> Developed by <a href="https://joshuakannan.com/" target="_blank">Joshua Kannan</a></p>
    </footer>
  </template>
  
  <style scoped>
    footer {
      background-color: #333;
      color: #fff;
      text-align: center;
      padding: 1px;
      position: unset;
      bottom: 0;
      left: 0; /* Set left to 0 to span the entire width */
      width: 100%;
      margin-top: 5.6rem;
    }
    footer a{
        color: #7762e0;
        text-decoration: none;
    }
    @media (max-width: 768px) {
  /* Adjust styles for screens with a width of 768px or less (typical tablets and smaller screens) */
  footer {
    position: relative;
    margin-bottom: 0;
  }
}
  </style>
  