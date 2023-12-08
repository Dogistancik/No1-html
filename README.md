<html>
  <head>
  </head>
  <body>
    <div id="wynik">
    </div>
    <button onclick="generateNumbers()">pokaż mi te cyfry</button> 
    <div id="dane"></div>
    <div id="opis"></div> <!-- Added a div for displaying the description -->
    
    <script> 
      function generateNumbers() {
        const wynik = document.querySelector("#wynik");
        let kodHTML = "";
        
        for (let i = 1; i <= 100; i++) {
          kodHTML = kodHTML + i + ", ";
        }
        
        wynik.innerHTML = kodHTML;
        
        const dane = document.querySelector("#dane");
        let text = '<table>';
        
        for (let i = 1; i <= 10; i++) {
          text += '<tr><td>' + i + '</td><td>' + (i * i) + '</td></tr>';
        }
        
        text += '</table>';
        dane.innerHTML = text;
        
        // Assuming you want to display information about a number, let's set a sample value for 'liczba'
        let liczba = 5; 
        
        const opis = document.querySelector("#opis");
        if (liczba > 0) {
          opis.innerHTML = liczba + " to liczba dodatnia";
        } else if (liczba === 0) {
          opis.innerHTML = "ZERO";
        } else {
          opis.innerHTML = liczba + " to liczba ujemna";
        }
      }
    </script>
    <style>
      td {
        border: 2px solid black;
        padding: 10px;  
      }
    </style>
  </body>
</html>
