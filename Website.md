[Website Created](https://claude.site/artifacts/6fed17d2-d4ca-49c2-9249-d985daef0bc4)

AI used: Claude

Prompt: "Build me an interactive website about synthetic data please for my AI final project!"

Website Code Provided by Claude: 
```{html}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Understanding Synthetic Data</title>
    <style>
        :root {
            --primary: #4a6fa5;
            --secondary: #5c88c5;
            --background: #f5f8ff;
            --text: #333;
            --accent: #ff7e5f;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--text);
            background-color: var(--background);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            background-color: var(--primary);
            color: white;
            padding: 30px 0;
            text-align: center;
        }

        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        h2 {
            font-size: 1.8rem;
            margin: 40px 0 20px;
            color: var(--primary);
        }

        h3 {
            font-size: 1.4rem;
            margin: 25px 0 15px;
            color: var(--secondary);
        }

        p {
            margin-bottom: 20px;
        }

        .nav {
            background-color: var(--secondary);
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 100;
        }

        .nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            flex-wrap: wrap;
        }

        .nav li {
            margin: 0 15px;
        }

        .nav a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s ease;
        }

        .nav a:hover {
            color: #ddd;
        }

        .section {
            padding: 40px 20px;
            margin-bottom: 30px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }

        .interactive-demo {
            background-color: #e9f0ff;
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
        }

        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1rem;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .btn:hover {
            background-color: #ff6347;
        }

        .data-container {
            margin: 20px 0;
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }

        table, th, td {
            border: 1px solid #ddd;
        }

        th, td {
            padding: 12px 15px;
            text-align: left;
        }

        th {
            background-color: var(--secondary);
            color: white;
        }

        tr:nth-child(even) {
            background-color: #f2f2f2;
        }

        .controls {
            margin: 20px 0;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        input, select {
            padding: 8px 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }

        canvas {
            max-width: 100%;
            margin: 20px 0;
        }

        footer {
            background-color: var(--primary);
            color: white;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }
            h2 {
                font-size: 1.5rem;
            }
            .nav ul {
                flex-direction: column;
                align-items: center;
            }
            .nav li {
                margin: 5px 0;
            }
            .controls {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Understanding Synthetic Data</h1>
            <p>An interactive exploration of synthetic data generation and its applications in AI</p>
        </div>
    </header>

    <nav class="nav">
        <ul>
            <li><a href="#introduction">Introduction</a></li>
            <li><a href="#what-is">What is Synthetic Data?</a></li>
            <li><a href="#generation">Generation Methods</a></li>
            <li><a href="#applications">Applications</a></li>
            <li><a href="#challenges">Challenges</a></li>
            <li><a href="#interactive">Interactive Demo</a></li>
        </ul>
    </nav>

    <div class="container">
        <section id="introduction" class="section">
            <h2>Introduction</h2>
            <p>Synthetic data is artificially generated information that mimics real-world data. In the era of data-driven AI development, synthetic data has emerged as a powerful solution to many challenges faced by machine learning practitioners and researchers.</p>
            <p>This interactive website explores what synthetic data is, how it's generated, its applications, and the challenges associated with its use. You'll also get to experiment with generating and visualizing synthetic data through our interactive demonstrations.</p>
        </section>

        <section id="what-is" class="section">
            <h2>What is Synthetic Data?</h2>
            <p>Synthetic data is artificially created data that mimics the statistical properties and patterns of real data without containing any actual information from the original dataset. It's generated using algorithms and models rather than being collected from real-world events or observations.</p>
            
            <h3>Key Characteristics:</h3>
            <p>
                • <strong>Privacy-preserving</strong>: Does not contain personal or sensitive information<br>
                • <strong>Customizable</strong>: Can be tailored to specific needs or scenarios<br>
                • <strong>Scalable</strong>: Can generate virtually unlimited amounts of data<br>
                • <strong>Balanced</strong>: Can overcome class imbalance issues present in real datasets<br>
                • <strong>Representative</strong>: Maintains statistical properties of the original data
            </p>

            <h3>Types of Synthetic Data:</h3>
            <p>
                • <strong>Fully synthetic</strong>: Created entirely from algorithms with no real data involved<br>
                • <strong>Partially synthetic</strong>: Some portions of real data are replaced with synthetic elements<br>
                • <strong>Hybrid synthetic</strong>: Combines real data with synthetic augmentations
            </p>
        </section>

        <section id="generation" class="section">
            <h2>Generation Methods</h2>
            <p>Several techniques are used to generate synthetic data, ranging from simple statistical methods to sophisticated deep learning approaches:</p>

            <h3>1. Statistical Methods</h3>
            <p>Basic approaches involve sampling from statistical distributions that match the characteristics of the original data. These include:</p>
            <p>
                • <strong>Monte Carlo simulation</strong>: Random sampling from probability distributions<br>
                • <strong>Bootstrapping</strong>: Resampling with replacement from existing data<br>
                • <strong>SMOTE</strong> (Synthetic Minority Over-sampling Technique): Creating synthetic samples for minority classes
            </p>

            <h3>2. Generative Models</h3>
            <p>More advanced approaches use machine learning to capture complex patterns:</p>
            <p>
                • <strong>GANs</strong> (Generative Adversarial Networks): Two neural networks compete to generate realistic data<br>
                • <strong>VAEs</strong> (Variational Autoencoders): Encode data into a latent space and decode to generate new samples<br>
                • <strong>Diffusion Models</strong>: Gradually add and remove noise to learn data distribution<br>
                • <strong>Transformer-based models</strong>: Use attention mechanisms to generate sequential or structured data
            </p>

            <h3>3. Agent-Based Simulation</h3>
            <p>Creating synthetic data by simulating interactions between autonomous agents following predefined rules, particularly useful for behavioral and social data.</p>
        </section>

        <section id="applications" class="section">
            <h2>Applications of Synthetic Data</h2>

            <h3>1. Privacy and Compliance</h3>
            <p>Synthetic data helps organizations comply with data protection regulations (like GDPR, HIPAA, CCPA) by allowing analysis without exposing sensitive information. This is particularly valuable in healthcare, finance, and other industries dealing with personal data.</p>

            <h3>2. Training AI Models</h3>
            <p>Many AI applications benefit from synthetic data:</p>
            <p>
                • <strong>Addressing data scarcity</strong>: Generating training data when real examples are limited<br>
                • <strong>Balancing datasets</strong>: Creating additional samples for underrepresented classes<br>
                • <strong>Edge case simulation</strong>: Generating rare but important scenarios<br>
                • <strong>Pre-training</strong>: Using synthetic data before fine-tuning on real data
            </p>

            <h3>3. Testing and Development</h3>
            <p>Synthetic data provides realistic test environments without risking real data:</p>
            <p>
                • <strong>Software testing</strong>: Creating realistic test datasets<br>
                • <strong>System performance evaluation</strong>: Stress-testing with varied data volumes<br>
                • <strong>Algorithm validation</strong>: Verifying model performance across diverse scenarios
            </p>

            <h3>4. Data Augmentation</h3>
            <p>Extending existing datasets with synthetic samples to improve model robustness and performance, especially in computer vision, speech recognition, and NLP.</p>
        </section>

        <section id="challenges" class="section">
            <h2>Challenges and Limitations</h2>
            
            <h3>1. Realism and Fidelity</h3>
            <p>Ensuring synthetic data accurately represents the complexity and nuance of real-world data remains challenging. Synthetic data may miss subtle patterns or anomalies present in real data.</p>

            <h3>2. Validation</h3>
            <p>Verifying that synthetic data maintains the statistical properties and correlations of the original data requires robust validation techniques.</p>

            <h3>3. Privacy Leakage</h3>
            <p>Some generative models may memorize and reproduce elements of their training data, potentially leading to privacy leaks when generating synthetic data from sensitive sources.</p>

            <h3>4. Computational Resources</h3>
            <p>Advanced generative models (like GANs or diffusion models) require significant computational resources to train and generate high-quality synthetic data.</p>

            <h3>5. Domain Expertise</h3>
            <p>Creating realistic synthetic data often requires domain knowledge to ensure the generated data respects field-specific constraints and relationships.</p>
        </section>

        <section id="interactive" class="section">
            <h2>Interactive Demo: Synthetic Data Generation</h2>
            
            <div class="interactive-demo">
                <h3>Gaussian Mixture Model Generator</h3>
                <p>Experiment with generating synthetic data using a Gaussian Mixture Model. Adjust the parameters to see how they affect the generated data.</p>
                
                <div class="controls">
                    <div>
                        <label for="num-points">Number of points:</label>
                        <input type="range" id="num-points" min="50" max="1000" value="200" step="50">
                        <span id="points-value">200</span>
                    </div>
                    
                    <div>
                        <label for="num-clusters">Number of clusters:</label>
                        <input type="range" id="num-clusters" min="1" max="5" value="2" step="1">
                        <span id="clusters-value">2</span>
                    </div>
                    
                    <div>
                        <label for="noise-level">Noise level:</label>
                        <input type="range" id="noise-level" min="0" max="1" value="0.2" step="0.1">
                        <span id="noise-value">0.2</span>
                    </div>
                </div>
                
                <button id="generate-btn" class="btn">Generate Data</button>
                
                <div>
                    <canvas id="data-chart" width="600" height="400"></canvas>
                </div>
                
                <div class="data-container">
                    <h3>Generated Data Sample:</h3>
                    <table id="data-table">
                        <thead>
                            <tr>
                                <th>ID</th>
                                <th>X</th>
                                <th>Y</th>
                                <th>Cluster</th>
                            </tr>
                        </thead>
                        <tbody id="data-body">
                            <!-- Data will be inserted here -->
                        </tbody>
                    </table>
                </div>
                
                <div>
                    <h3>Applications of This Data:</h3>
                    <p>This type of synthetic data could be used for:</p>
                    <p>
                        • Testing clustering algorithms<br>
                        • Benchmarking classification models<br>
                        • Visualizing machine learning concepts<br>
                        • Simulating population distributions
                    </p>
                </div>
            </div>

            <div class="interactive-demo">
                <h3>Synthetic Time Series Generator</h3>
                <p>Create synthetic time series data with various patterns and noise levels.</p>
                
                <div class="controls">
                    <div>
                        <label for="series-length">Series length:</label>
                        <input type="range" id="series-length" min="20" max="200" value="100" step="10">
                        <span id="length-value">100</span>
                    </div>
                    
                    <div>
                        <label for="pattern-type">Pattern:</label>
                        <select id="pattern-type">
                            <option value="trend">Linear Trend</option>
                            <option value="seasonal">Seasonal Pattern</option>
                            <option value="cyclical">Cyclical Pattern</option>
                            <option value="combination">Combination</option>
                        </select>
                    </div>
                    
                    <div>
                        <label for="series-noise">Noise level:</label>
                        <input type="range" id="series-noise" min="0" max="1" value="0.3" step="0.1">
                        <span id="series-noise-value">0.3</span>
                    </div>
                </div>
                
                <button id="generate-series-btn" class="btn">Generate Time Series</button>
                
                <div>
                    <canvas id="series-chart" width="600" height="300"></canvas>
                </div>
                
                <div>
                    <h3>Applications:</h3>
                    <p>Synthetic time series data is valuable for:</p>
                    <p>
                        • Training forecasting models<br>
                        • Testing anomaly detection algorithms<br>
                        • Developing trading strategies<br>
                        • Simulating IoT sensor data
                    </p>
                </div>
            </div>
        </section>

        <section class="section">
            <h2>Real-World Examples</h2>
            
            <h3>Healthcare</h3>
            <p>Synthetic medical data is used to train diagnostic algorithms and test treatment protocols without exposing sensitive patient information. For example, synthetic medical images can help train AI to detect diseases from X-rays or MRIs.</p>
            
            <h3>Finance</h3>
            <p>Banks and financial institutions use synthetic transaction data to test fraud detection systems and develop risk models without exposing real customer data.</p>
            
            <h3>Autonomous Vehicles</h3>
            <p>Synthetic driving scenarios help train self-driving systems to handle rare but critical situations that might be dangerous or impossible to collect in real life.</p>
            
            <h3>Computer Vision</h3>
            <p>Synthetic images and videos enhance training datasets for object recognition, pose estimation, and scene understanding algorithms.</p>
        </section>

        <section class="section">
            <h2>Ethical Considerations</h2>
            
            <p>While synthetic data offers many benefits, its use raises important ethical questions:</p>
            
            <h3>Representation and Bias</h3>
            <p>Synthetic data may inherit or even amplify biases present in the original data. Careful attention must be paid to ensure synthetic data generation doesn't perpetuate or worsen existing biases.</p>
            
            <h3>Transparency</h3>
            <p>The use of synthetic data should be disclosed, especially in research and development of high-stakes AI systems. Users should be aware when they're working with artificially generated information.</p>
            
            <h3>Validation Standards</h3>
            <p>The AI community needs robust standards for validating synthetic data's quality, representativeness, and usefulness for specific applications.</p>
        </section>
    </div>

    <footer>
        <div class="container">
            <p>Created for AI Final Project | Understanding Synthetic Data | &copy; 2025</p>
        </div>
    </footer>

    <script>
        // Utility function for random numbers
        function randomInRange(min, max) {
            return Math.random() * (max - min) + min;
        }

        // Generate random cluster centers
        function generateClusterCenters(numClusters) {
            const centers = [];
            for (let i = 0; i < numClusters; i++) {
                centers.push({
                    x: randomInRange(100, 500),
                    y: randomInRange(50, 350)
                });
            }
            return centers;
        }

        // Generate synthetic data points around cluster centers
        function generateClusterData(numPoints, centers, noiseLevel) {
            const data = [];
            const pointsPerCluster = Math.floor(numPoints / centers.length);
            
            for (let c = 0; c < centers.length; c++) {
                const center = centers[c];
                const variance = 30 + (noiseLevel * 70); // Scale noise based on noise level
                
                for (let i = 0; i < pointsPerCluster; i++) {
                    // Box-Muller transform for normal distribution
                    const u1 = Math.random();
                    const u2 = Math.random();
                    
                    const z1 = Math.sqrt(-2 * Math.log(u1)) * Math.cos(2 * Math.PI * u2);
                    const z2 = Math.sqrt(-2 * Math.log(u1)) * Math.sin(2 * Math.PI * u2);
                    
                    data.push({
                        id: c * pointsPerCluster + i + 1,
                        x: center.x + z1 * variance,
                        y: center.y + z2 * variance,
                        cluster: c + 1
                    });
                }
            }
            
            // Add any remaining points to the last cluster
            const remaining = numPoints - (pointsPerCluster * centers.length);
            const lastCenter = centers[centers.length - 1];
            const variance = 30 + (noiseLevel * 70);
            
            for (let i = 0; i < remaining; i++) {
                const u1 = Math.random();
                const u2 = Math.random();
                
                const z1 = Math.sqrt(-2 * Math.log(u1)) * Math.cos(2 * Math.PI * u2);
                const z2 = Math.sqrt(-2 * Math.log(u1)) * Math.sin(2 * Math.PI * u2);
                
                data.push({
                    id: data.length + 1,
                    x: lastCenter.x + z1 * variance,
                    y: lastCenter.y + z2 * variance,
                    cluster: centers.length
                });
            }
            
            return data;
        }

        // Draw data points on canvas
        function drawDataPoints(canvas, data) {
            const ctx = canvas.getContext('2d');
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Define colors for clusters
            const colors = ['#FF5733', '#33FF57', '#3357FF', '#F033FF', '#FF9033'];
            
            // Draw axes
            ctx.strokeStyle = '#333';
            ctx.lineWidth = 1;
            ctx.beginPath();
            
            // X-axis
            ctx.moveTo(50, canvas.height - 30);
            ctx.lineTo(canvas.width - 20, canvas.height - 30);
            
            // Y-axis
            ctx.moveTo(50, 20);
            ctx.lineTo(50, canvas.height - 30);
            
            ctx.stroke();
            
            // Add axis labels
            ctx.fillStyle = '#333';
            ctx.font = '12px Arial';
            ctx.fillText('X', canvas.width - 15, canvas.height - 15);
            ctx.fillText('Y', 35, 15);
            
            // Draw data points
            data.forEach(point => {
                ctx.fillStyle = colors[(point.cluster - 1) % colors.length];
                ctx.beginPath();
                ctx.arc(point.x, point.y, 4, 0, Math.PI * 2);
                ctx.fill();
            });
        }

        // Populate table with data
        function populateTable(tableBody, data) {
            tableBody.innerHTML = '';
            
            // Only show first 10 rows to avoid overwhelming the page
            const displayData = data.slice(0, 10);
            
            displayData.forEach(point => {
                const row = document.createElement('tr');
                
                const idCell = document.createElement('td');
                idCell.textContent = point.id;
                
                const xCell = document.createElement('td');
                xCell.textContent = point.x.toFixed(2);
                
                const yCell = document.createElement('td');
                yCell.textContent = point.y.toFixed(2);
                
                const clusterCell = document.createElement('td');
                clusterCell.textContent = point.cluster;
                
                row.appendChild(idCell);
                row.appendChild(xCell);
                row.appendChild(yCell);
                row.appendChild(clusterCell);
                
                tableBody.appendChild(row);
            });
            
            if (data.length > 10) {
                const row = document.createElement('tr');
                const cell = document.createElement('td');
                cell.colSpan = 4;
                cell.textContent = `... and ${data.length - 10} more rows`;
                cell.style.textAlign = 'center';
                row.appendChild(cell);
                tableBody.appendChild(row);
            }
        }

        // Generate time series data
        function generateTimeSeries(length, pattern, noiseLevel) {
            const data = [];
            
            for (let i = 0; i < length; i++) {
                const x = i;
                let y = 0;
                
                // Base value depends on pattern
                switch (pattern) {
                    case 'trend':
                        y = 50 + (i / length) * 100;
                        break;
                    case 'seasonal':
                        y = 100 + 50 * Math.sin(i * 2 * Math.PI / (length / 4));
                        break;
                    case 'cyclical':
                        y = 100 + 30 * Math.sin(i * 2 * Math.PI / length) + 20 * Math.cos(i * 6 * Math.PI / length);
                        break;
                    case 'combination':
                        y = 50 + (i / length) * 50 + 40 * Math.sin(i * 2 * Math.PI / (length / 3));
                        break;
                }
                
                // Add noise
                const noise = (Math.random() - 0.5) * 2 * 50 * noiseLevel;
                y += noise;
                
                data.push({ x, y });
            }
            
            return data;
        }

        // Draw time series on canvas
        function drawTimeSeries(canvas, data) {
            const ctx = canvas.getContext('2d');
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            // Find min/max values for scaling
            let minY = Math.min(...data.map(d => d.y));
            let maxY = Math.max(...data.map(d => d.y));
            
            // Add padding
            minY = Math.max(0, minY - 10);
            maxY = maxY + 10;
            
            // Calculate scale factors
            const xScale = (canvas.width - 70) / (data.length - 1);
            const yScale = (canvas.height - 60) / (maxY - minY);
            
            // Draw axes
            ctx.strokeStyle = '#333';
            ctx.lineWidth = 1;
            ctx.beginPath();
            
            // X-axis
            ctx.moveTo(50, canvas.height - 30);
            ctx.lineTo(canvas.width - 20, canvas.height - 30);
            
            // Y-axis
            ctx.moveTo(50, 20);
            ctx.lineTo(50, canvas.height - 30);
            
            ctx.stroke();
            
            // Add axis labels
            ctx.fillStyle = '#333';
            ctx.font = '12px Arial';
            ctx.fillText('Time', canvas.width - 30, canvas.height - 15);
            ctx.fillText('Value', 20, 15);
            
            // Draw time series line
            ctx.strokeStyle = '#4a6fa5';
            ctx.lineWidth = 2;
            ctx.beginPath();
            
            data.forEach((point, i) => {
                const x = 50 + i * xScale;
                const y = canvas.height - 30 - (point.y - minY) * yScale;
                
                if (i === 0) {
                    ctx.moveTo(x, y);
                } else {
                    ctx.lineTo(x, y);
                }
            });
            
            ctx.stroke();
            
            // Draw points
            ctx.fillStyle = '#ff7e5f';
            data.forEach((point, i) => {
                const x = 50 + i * xScale;
                const y = canvas.height - 30 - (point.y - minY) * yScale;
                
                ctx.beginPath();
                ctx.arc(x, y, 3, 0, Math.PI * 2);
                ctx.fill();
            });
        }

        // Initialize UI elements and event handlers
        document.addEventListener('DOMContentLoaded', function() {
            // Cluster data generator
            const numPointsSlider = document.getElementById('num-points');
            const numClustersSlider = document.getElementById('num-clusters');
            const noiseLevelSlider = document.getElementById('noise-level');
            const generateBtn = document.getElementById('generate-btn');
            const dataChart = document.getElementById('data-chart');
            const dataBody = document.getElementById('data-body');
            const pointsValue = document.getElementById('points-value');
            const clustersValue = document.getElementById('clusters-value');
            const noiseValue = document.getElementById('noise-value');
            
            // Time series generator
            const seriesLengthSlider = document.getElementById('series-length');
            const patternSelector = document.getElementById('pattern-type');
            const seriesNoiseSlider = document.getElementById('series-noise');
            const generateSeriesBtn = document.getElementById('generate-series-btn');
            const seriesChart = document.getElementById('series-chart');
            const lengthValue = document.getElementById('length-value');
            const seriesNoiseValue = document.getElementById('series-noise-value');
            
            // Update displayed values when sliders change
            numPointsSlider.addEventListener('input', function() {
                pointsValue.textContent = this.value;
            });
            
            numClustersSlider.addEventListener('input', function() {
                clustersValue.textContent = this.value;
            });
            
            noiseLevelSlider.addEventListener('input', function() {
                noiseValue.textContent = this.value;
            });
            
            seriesLengthSlider.addEventListener('input', function() {
                lengthValue.textContent = this.value;
            });
            
            seriesNoiseSlider.addEventListener('input', function() {
                seriesNoiseValue.textContent = this.value;
            });
            
            // Generate cluster data
            generateBtn.addEventListener('click', function() {
                const numPoints = parseInt(numPointsSlider.value);
                const numClusters = parseInt(numClustersSlider.value);
                const noiseLevel = parseFloat(noiseLevelSlider.value);
                
                const centers = generateClusterCenters(numClusters);
                const data = generateClusterData(numPoints, centers, noiseLevel);
                
                drawDataPoints(dataChart, data);
                populateTable(dataBody, data);
            });
            
            // Generate time series data
            generateSeriesBtn.addEventListener('click', function() {
                const length = parseInt(seriesLengthSlider.value);
                const pattern = patternSelector.value;
                const noise = parseFloat(seriesNoiseSlider.value);
                
                const data = generateTimeSeries(length, pattern, noise);
                drawTimeSeries(seriesChart, data);
            });
            
            // Initialize with some data
            generateBtn.click();
            generateSeriesBtn.click();
            
            // Smooth scrolling for navigation
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    
                    const targetId = this.getAttribute('href');
                    const targetElement = document.querySelector(targetId);
                    
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html>
```

