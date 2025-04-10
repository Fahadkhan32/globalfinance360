# globalfinance360
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GlobalFinance360° - Master the World’s Financial Pulse</title>
    <style>
        /* CSS for layout and styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        header {
            background-color: #1a2a44;
            color: white;
            text-align: center;
            padding: 20px;
        }
        header h1 {
            margin: 0;
            font-size: 2.5em;
        }
        header p {
            margin: 5px 0;
            font-style: italic;
        }
        .container {
            display: flex;
            flex-wrap: wrap;
            max-width: 1200px;
            margin: 20px auto;
            gap: 20px;
        }
        .dashboard, .tools, .education {
            flex: 1;
            min-width: 300px;
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .dashboard h2, .tools h2, .education h2 {
            margin-top: 0;
            color: #1a2a44;
        }
        .market-data div {
            margin: 10px 0;
            padding: 10px;
            background: #eef;
            border-radius: 5px;
        }
        .alert {
            background: #ffdddd;
            padding: 10px;
            border-left: 5px solid #ff5555;
            margin: 10px 0;
        }
        button {
            background: #1a2a44;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background: #2b4066;
        }
        @media (max-width: 600px) {
            .container {
                flex-direction: column;
                margin: 10px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <h1>GlobalFinance360°</h1>
        <p>Every Market, Every Metric, Every Moment – Master the World’s Financial Pulse.</p>
    </header>

    <!-- Main Content -->
    <div class="container">
        <!-- Real-Time Global Market Dashboard -->
        <section class="dashboard">
            <h2>Real-Time Market Dashboard</h2>
            <div class="market-data">
                <div id="forex">Forex: EUR/USD - <span id="eurusd">1.0850</span></div>
                <div id="crypto">Crypto: BTC/USD - <span id="btcusd">67250.32</span></div>
                <div id="stocks">Stocks: S&P 500 - <span id="sp500">5200.45</span></div>
            </div>
            <button onclick="refreshData()">Refresh Data</button>
        </section>

        <!-- Market Analysis Tools -->
        <section class="tools">
            <h2>Analysis Tools</h2>
            <p>AI Predictive Analytics: <span id="prediction">Loading...</span></p>
            <p>Interactive Charts: <a href="#">View Gold vs. BTC</a></p>
            <button onclick="simulateCrisis()">Run Crisis Simulator</button>
        </section>

        <!-- Educational Hub -->
        <section class="education">
            <h2>Educational Hub</h2>
            <ul>
                <li><a href="#">Forex for Beginners</a></li>
                <li><a href="#">Crypto Wallets 101</a></li>
                <li><a href="#">Case Study: 2022 UK Gilts Crisis</a></li>
            </ul>
        </section>
    </div>

    <!-- JavaScript for interactivity -->
    <script>
        // Simulate live market data updates
        function updateMarketData() {
            const eurusd = (Math.random() * 0.01 + 1.08).toFixed(4);
            const btcusd = (Math.random() * 1000 + 67000).toFixed(2);
            const sp500 = (Math.random() * 50 + 5180).toFixed(2);
            document.getElementById("eurusd").innerText = eurusd;
            document.getElementById("btcusd").innerText = btcusd;
            document.getElementById("sp500").innerText = sp500;
        }

        // Refresh data on button click
        function refreshData() {
            updateMarketData();
            alert("Market data refreshed!");
        }

        // Simulate AI prediction
        function updatePrediction() {
            const predictions = [
                "AI projects a 15% drop in Bitcoin if Fed hikes rates.",
                "EUR/USD likely to rebound at 1.0800 support.",
                "S&P 500 showing overbought signals."
            ];
            const randomPrediction = predictions[Math.floor(Math.random() * predictions.length)];
            document.getElementById("prediction").innerText = randomPrediction;
        }

        // Simulate crisis scenario
        function simulateCrisis() {
            const alertDiv = document.createElement("div");
            alertDiv.className = "alert";
            alertDiv.innerText = "Crisis Simulator: Portfolio down 25% due to a hypothetical 2025 crypto crash.";
            document.querySelector(".tools").appendChild(alertDiv);
            setTimeout(() => alertDiv.remove(), 5000); // Remove after 5 seconds
        }

        // Initial data load
        updateMarketData();
        updatePrediction();

        // Auto-update market data every 10 seconds
        setInterval(updateMarketData, 10000);
    </script>
</body>
</html>
