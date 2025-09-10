# tourist-spot-active-status-and-entry-fee
This project is a model of html, CSS and JavaScript. It is an initiative idea about the active status of the tourist place and the entry fee if it.
<!DOCTYPE html>
<html>
<head>
  <title>Tourist Spot Status</title>
  <style>
    body {
      font-family: Arial;
      background: #f2f2f2;
      padding: 20px;
    }
    h1 { text-align: center; }
    .spot {
      background: white;
      padding: 10px;
      margin: 10px;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    .active { color: green; font-weight: bold; }
    .inactive { color: red; font-weight: bold; }
  </style>
</head>
<body>

  <h1>Tourist Spot Active Status</h1>

  <div id="spots"></div>

  <script>
    // simple data
    var spots = [
      { name: "Ooty Botanical Garden", fee: 30, active: true },
      { name: "Meenakshi Temple, Madurai", fee: 0, active: false },
      { name: "Marina Beach, Chennai", fee: 0, active: true }
    ];

    var container = document.getElementById("spots");

    // show all spots
    for (var i = 0; i < spots.length; i++) {
      var s = spots[i];
      var div = document.createElement("div");
      div.className = "spot";

      var statusText = s.active ? "Active" : "Inactive";
      var statusClass = s.active ? "active" : "inactive";

      div.innerHTML =
        "<h3>" + s.name + "</h3>" +
        "<p>Entry Fee: ₹" + s.fee + "</p>" +
        "<p>Status: <span class='" + statusClass + "'>" + statusText + "</span></p>";

      container.appendChild(div);
    }
  </script>

</body>
</html>
