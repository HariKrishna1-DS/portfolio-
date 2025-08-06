<!DOCTYPE html>
<html lang="en">
<head>
  <marquee style="font-size: 20px ;	scrollamount="30" ><font color ="Blue"> the Houses prices is based on 2023&2024 </font></marquee>
<body>
    <img src="citi.jpg" 
         alt="Beach vacation photo" 
         width="1300" 
         height="700"
         >
    <meta charset="UTF-8">
    <title>Bangalore House Price Predictor</title>
    <style>
        body {
             }
        .container {
            max-width: 500px;
            margin: 60px auto;
            background: rgba(255, 255, 255, 0.92);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
        }
      h1 {
            text-align: center;
            color: #2c3e50;
        }
        label {
            display: block;
            margin-top: 15px;
            color: #333;
        }
        input, select {
            width: 100%;
            padding: 10px;
            margin-top: 6px;
            border: 1px solid #bbb;
            border-radius: 6px;
            font-size: 14px;
        }
        button {
            width: 100%;
            padding: 12px;
            margin-top: 20px;
            background-color: #3498db;
            color: white;
            font-size: 16px;
            border: none;
            border-radius: 6px;
            cursor: pointer;
        }
        button:hover {
            background-color: #2980b9;
        }
        .result {
            margin-top: 20px;
            padding: 15px;
            background-color: #ecf0f1;
            border-left: 6px solid #3498db;
            font-size: 18px;
        }
    </style>
</head>
<body
    <div class="container">
        <h1>Bangalore House Price Predictor</h1>
        <form>
<body>
            <label for="sqft">Total Square Feet:</label>
            <input type="number" id="sqft" name="sqft" placeholder="e.g. 1000">
            <label for="bath">Number of Bathrooms:</label>
            <input type="number" id="bath" name="bath" placeholder="e.g. 2">
            <label for="bhk">Number of BHK:</label>
            <input type="number" id="bhk" name="bhk" placeholder="e.g. 3">
            <label for="location">Select Location:</label>
            <select id="location" name="location">
                <option value="">--Select Location--</option>
                <option value="Uttarahalli">Uttarahalli</option>
                <option value="Whitefield">Whitefield</option>
                <option value="Electronic City">Electronic City</option>
                <option value="Rajaji Nagar">Rajaji Nagar</option>
		<option value="Vijayanagar">Vijayanagar</option>
		<option value="Thubarahalli">Thubarahalli</option>
                <option value="Shivaji Nagar">Shivaji Nagar</option>
                <option value="Nagasandra">Nagasandra</option>
                <option value="Others">Other</option>
            </select>
            <button type="button" onclick="predictPrice()">Predict Price</button>
       </form>
        <div class="result" id="output"></div>
    </div>
    <script>
        function predictPrice() {
            const sqft = document.getElementById("sqft").value;
            const bath = document.getElementById("bath").value;
            const bhk = document.getElementById("bhk").value;
            const location = document.getElementById("location").value;
            if (sqft && bath && bhk && location) {
                const price = (parseFloat(sqft) * 6000 / 100000).toFixed(2);
                document.getElementById("output").innerHTML = 
                    `Estimated Price: ₹ <strong>${price}</strong> Lakhs`;
            } else {
                document.getElementById("output").innerHTML = 
                    "Please fill all fields to get prediction.";
            }
        }</body>
    </script>
</body>
</html>
