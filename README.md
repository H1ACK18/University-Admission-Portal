<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>University Admission Portal</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js" defer></script>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(to right, #6a11cb, #2575fc);
            color: white;
        }
        header {
            text-align: center;
            padding: 20px;
            background-color: #4a90e2;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        header img {
            width: 100px;
            display: block;
            margin: 0 auto 10px;
        }
        .container {
            padding: 20px;
            max-width: 800px;
            margin: auto;
            background: white;
            color: black;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        footer {
            text-align: center;
            padding: 10px;
            background-color: #4a90e2;
            color: white;
            position: relative;
        }
        footer .social-icons img {
            width: 30px;
            margin: 0 10px;
            cursor: pointer;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        table th, table td {
            border: 1px solid #ddd;
            padding: 8px;
            text-align: center;
        }
        table th {
            background-color: #4a90e2;
            color: white;
        }
        button {
            background-color: #2575fc;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: #6a11cb;
        }
    </style>
</head>
<body>
    <header>
        <img src="university-logo.png" alt="University Logo">
        <h1>Welcome to the University Admission Portal</h1>
        <p>Your guide to transparent admissions, fee management, and application updates.</p>
    </header>

    <div class="container">
        <section id="admission-process">
            <h2>Admission Process</h2>
            <p>Follow these steps to apply for admission:</p>
            <ol>
                <li><strong>Step 1:</strong> Fill out the online application form.</li>
                <li><strong>Step 2:</strong> Upload required documents (ID, certificates, etc.).</li>
                <li><strong>Step 3:</strong> Pay the application fee.</li>
                <li><strong>Step 4:</strong> Wait for application review and status update.</li>
                <li><strong>Step 5:</strong> Receive admission decision and instructions.</li>
            </ol>
        </section>

        <section id="fee-structure">
            <h2>Fee Structure</h2>
            <table>
                <thead>
                    <tr>
                        <th>Course</th>
                        <th>Tuition Fee (per year)</th>
                        <th>Other Fees</th>
                        <th>Total Fee</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Computer Science</td>
                        <td>₹8,30,000</td>
                        <td>₹41,500</td>
                        <td>₹8,71,500</td>
                    </tr>
                    <tr>
                        <td>Business Administration</td>
                        <td>₹7,47,000</td>
                        <td>₹41,500</td>
                        <td>₹7,88,500</td>
                    </tr>
                    <tr>
                        <td>Medicine</td>
                        <td>₹12,45,000</td>
                        <td>₹41,500</td>
                        <td>₹12,86,500</td>
                    </tr>
                    <tr>
                        <td>Law</td>
                        <td>₹6,64,000</td>
                        <td>₹41,500</td>
                        <td>₹7,05,500</td>
                    </tr>
                </tbody>
            </table>
        </section>

        <section id="status-updates">
            <h2>Application Status</h2>
            <form>
                <label for="applicant-id">Enter Your Application ID:</label>
                <input type="text" id="applicant-id" name="applicant-id" required>
                <button type="submit">Check Status</button>
            </form>
            <div id="status-message" class="hidden">
                <p>Status: <strong id="status">Pending</strong></p>
                <p>Next Step: <span id="next-step">Awaiting review</span></p>
            </div>
        </section>
    </div>

    <footer>
        <p>&copy; 2025 University Admission Portal. All Rights Reserved.</p>
        <div class="social-icons">
            <img src="facebook-icon.png" alt="Facebook">
            <img src="instagram-icon.png" alt="Instagram">
            <img src="twitter-icon.png" alt="Twitter">
            <img src="whatsapp-icon.png" alt="WhatsApp">
        </div>
    </footer>
</body>
</html>
