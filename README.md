<!DOCTYPE html>
<head>
    
    <title>Country Names and Their Respective Capitals Sorted in Alphabetical Ascending/Descending Order</title>
    <style>
        h1, h2 {
            color: purple;
        } 
        table {
            width: 50%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        th, td {
            border: 1px solid purple;
            padding: 10px;
            text-align: left;
        }

        .sort-button {
            padding: 10px 20px;
            margin: 10px;
            background-color: black;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .sort-button:hover {
            background-color: #0056b3;
        }
    </style>
</head>
<body>

<h1>Student ID: M23W7253 Name: BHATTARAI GANESH</h1>
<h2>Country Names and Their Respective Capitals Sorted in Ascending/Descending Order</h2>

<button class="sort-button" onclick="sortAscending()">Ascending</button>
<button class="sort-button" onclick="sortDescending()">Descending</button>

<table id="countryTable">
    <thead>
        <tr>
            <th>Country</th>
            <th>Capital</th>
        </tr>
    </thead>
    <tbody>
        <tr><td>Turkey</td><td>Ankara</td></tr>
        <tr><td>Laos</td><td>Vientiane</td></tr>
        <tr><td>Mexico</td><td>Mexico City</td></tr>
        <tr><td>Rwanda</td><td>Kigali</td></tr>
        <tr><td>Oman</td><td>Muscat</td></tr>
        <tr><td>Qatar</td><td>Doha</td></tr>
        <tr><td>Peru</td><td>Lima</td></tr>
        <tr><td>Nepal</td><td>Kathmandu</td></tr>
        <tr><td>Sweden</td><td>Stockholm</td></tr>
        <tr><td>Kenya</td><td>Nairobi</td></tr>
    </tbody>
</table>

<script>
    function sortAscending() {
        let table = document.getElementById("countryTable").getElementsByTagName("tbody")[0];
        let rows = Array.from(table.rows);

        rows.sort((a, b) => a.cells[0].innerText.localeCompare(b.cells[0].innerText));

        table.innerHTML = "";
        rows.forEach(row => table.appendChild(row));

        
        console.log("Ascending Order:");
        rows.forEach(row => console.log(`Country: ${row.cells[0].innerText}, Capital: ${row.cells[1].innerText}`));
    }


    function sortDescending() {
        let table = document.getElementById("countryTable").getElementsByTagName("tbody")[0];
        let rows = Array.from(table.rows);

        rows.sort((a, b) => b.cells[0].innerText.localeCompare(a.cells[0].innerText));

        table.innerHTML = "";
        rows.forEach(row => table.appendChild(row));

     
        console.log("Descending Order:");
        rows.forEach(row => console.log(`Country: ${row.cells[0].innerText}, Capital: ${row.cells[1].innerText}`));
    }
</script>

</body>
</html>

