<html>
    <head>
        <title>Form title</title>
        <link rel="stylesheet" type="text/css" href="style.css">
    </head>
    <body>
        <div class="container">
            <header><h1>Form</h1></header>
            <form action="submit_form.php" method="post">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" placeholder="name" required><br>

                <label for="age">Age:</label>
                <input type="number" id="age" name="age" placeholder="age" required><br>

                <label for="birthdate">Birth date:</label>
                <input type="date" id="birthdate" name="birthdate" required><br>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required><br>

                <label for="phone">Phone Number:</label>
                <input type="tel" id="phone" name="phone" placeholder="123-456-7890" required><br>

                <label for="gender">Gender:</label>
                <select id="gender" name="gender" required>
                    <option value="">Select</option>
                    <option value="male">Male</option>
                    <option value="female">Female</option>
                    <option value="other">Other</option>
                </select><br>

                <label for="address">Address:</label>
                <input type="text" id="address" name="address" placeholder="address" required><br>

                <label for="message">Message:</label>
                <textarea id="message" name="message" required></textarea><hr>

                <button type="submit">Submit</button>
            </form>
        </div>
    </body>
</html>

<script>
document.querySelector('form').addEventListener('submit', function(e) {
    e.preventDefault();
    document.body.innerHTML = `
        <div class="container">
            <header><h1>Thank You!</h1></header>
            <p><h3><b>Your form has been submitted successfully.</b></h3></p>
        </div>
    `;
});
</script>
