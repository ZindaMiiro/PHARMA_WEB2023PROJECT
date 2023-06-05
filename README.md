# PHARMA_WEB2023PROJECT
<!DOCTYPE html>
<html>
<head>
  <title>PHARMA HOME PAGE</title>
  <style>
    body {
      background-color: green;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      height: 100vh;
      text-align: center; /* Center align the content */
    }
    
    h1 {
      margin-bottom: 0; /* Remove bottom margin of h1 */
    }
    
    h2 {
      color: blue; /* Set h2 color to bright blue */
    }
    
    label {
      color: blue; /* Set checkbox label color to bright blue */
    }
    
    h2#pharma-title {
      color: black; /* Set "Pharma Home Page" color to black */
      text-decoration: underline; /* Add underline to the text */
    }
    
    button {
      padding: 10px 20px; /* Increase button padding for a larger size */
      background-color: lightblue; /* Set button background color to light blue */
      color: darkgreen; /* Set button text color to dark green */
    }
  </style>
  <script>
    function redirect() {
      var checkboxes = document.getElementsByName("options");
      var selectedOptions = [];

      checkboxes.forEach(function(checkbox) {
        if (checkbox. checked) {
          selectedOptions.push(checkbox.value);
        }
      });

      if (selectedOptions.includes("option1")) {
        window.location.href = "PatientLogin.html";
      }
      if (selectedOptions.includes("option2")) {
        window.location.href = "DoctorLogin.html";
      }
      if (selectedOptions.includes("option3")) {
        window.location.href = "PharmacistLogin.html";
      }
    }
  </script>
</head>
<body>
<h1>Welcome</h1>
<h2 id="pharma-title">Pharma Home Page</h2>
  <h3>Select an option:</h3>
  <form>
    <label>
      <input type="checkbox" name="options" value="option1"> Patient
    </label>
    <label>
      <input type="checkbox" name="options" value="option2"> Doctor
    </label>
    <label>
      <input type="checkbox" name="options" value="option3"> Pharmacist
    </label>
  </form>
  <br><br>
  <button onclick="redirect()">Go to Login Page</button>
</body>
</html>
