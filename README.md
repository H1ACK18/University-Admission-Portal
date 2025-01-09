<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>University Portal</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <h1>University Admission Portal</h1>
        <p>Your one-stop solution for managing admissions, fees, and more.</p>
        <img src="images/university.jpg" alt="University Logo" style="width:100%; max-height:200px; object-fit:cover;">
    </header>

    <div class="container">
        <!-- Admission Form -->
        <section id="admission-form">
            <h2>Admission Application</h2>
            <p>Fill in the form below to apply for your desired course.</p>
            <form id="admissionForm">
                <label for="name">Full Name:</label>
                <input type="text" id="name" name="name" required><br><br>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required><br><br>

                <label for="course">Course Applying For:</label>
                <select id="course" name="course" required>
                    <option value="computer-science">Computer Science</option>
                    <option value="business-administration">Business Administration</option>
                    <option value="medicine">Medicine</option>
                    <option value="law">Law</option>
                </select><br><br>

                <label for="documents">Upload Documents (PDF, JPG, PNG):</label>
                <input type="file" id="documents" name="documents" accept=".pdf,.jpg,.png" required><br><br>

                <button type="submit">Submit Application</button>
            </form>

            <div id="statusMessage" class="hidden">
                <h2>Application Status</h2>
                <p>Your application has been <strong>submitted successfully</strong>.</p>
                <p>Status: <span id="status">Pending</span></p>
            </div>
        </section>

        <!-- Fee Payment Section -->
        <section id="fee-payment">
            <h2>Fee Payment Portal</h2>
            <p>Make your fee payments securely and download receipts.</p>
            <form id="paymentForm">
                <label for="studentId">Student ID:</label>
                <input type="text" id="studentId" name="studentId" required><br><br>

                <label for="feeAmount">Fee Amount (in $):</label>
                <input type="number" id="feeAmount" name="feeAmount" required><br><br>

                <label for="paymentMethod">Payment Method:</label>
                <select id="paymentMethod" name="paymentMethod" required>
                    <option value="credit-card">Credit Card</option>
                    <option value="paypal">PayPal</option>
                    <option value="bank-transfer">Bank Transfer</option>
                </select><br><br>

                <button type="submit">Make Payment</button>
            </form>

            <div id="receiptSection" class="hidden">
                <h2>Payment Receipt</h2>
                <p><strong>Student ID:</strong> <span id="receiptStudentId"></span></p>
                <p><strong>Fee Amount:</strong> $<span id="receiptAmount"></span></p>
                <p><strong>Payment Method:</strong> <span id="receiptPaymentMethod"></span></p>
                <p><strong>Status:</strong> <span id="paymentStatus">Paid</span></p>
                <button id="downloadReceipt">Download Receipt</button>
            </div>
        </section>

        <!-- Social Media Links -->
        <footer>
            <h2>Connect with Us</h2>
            <ul>
                <li><a href="https://www.facebook.com" target="_blank">Facebook</a></li>
                <li><a href="https://www.instagram.com" target="_blank">Instagram</a></li>
                <li><a href="https://www.twitter.com" target="_blank">Twitter</a></li>
                <li><a href="https://www.whatsapp.com" target="_blank">WhatsApp</a></li>
            </ul>
            <p>&copy; 2025 University Portal. All Rights Reserved.</p>
        </footer>

        <script>
            // Admission Form Submission
            document.getElementById('admissionForm').addEventListener('submit', function(event) {
                event.preventDefault();
                document.getElementById('statusMessage').classList.remove('hidden');
                document.getElementById('status').textContent = "Pending";
                alert("Your application has been submitted!");
                document.getElementById('admissionForm').reset();
            });

            // Payment Form Submission
            document.getElementById('paymentForm').addEventListener('submit', function(event) {
                event.preventDefault();
                const studentId = document.getElementById('studentId').value;
                const feeAmount = document.getElementById('feeAmount').value;
                const paymentMethod = document.getElementById('paymentMethod').value;
                document.getElementById('receiptStudentId').textContent = studentId;
                document.getElementById('receiptAmount').textContent = feeAmount;
                document.getElementById('receiptPaymentMethod').textContent = paymentMethod;
                document.getElementById('receiptSection').classList.remove('hidden');
                document.getElementById('paymentForm').reset();
            });

            // Receipt Download
            document.getElementById('downloadReceipt').addEventListener('click', function() {
                const receiptContent = `Receipt\n\nStudent ID: ${document.getElementById('receiptStudentId').textContent}\nFee Amount: $${document.getElementById('receiptAmount').textContent}\nPayment Method: ${document.getElementById('receiptPaymentMethod').textContent}\nStatus: Paid`;
                const blob = new Blob([receiptContent], { type: 'text/plain' });
                const link = document.createElement('a');
                link.href = URL.createObjectURL(blob);
                link.download = 'fee_receipt.txt';
                link.click();
            });
        </script>
    </div>
</body>
</html>
