# spark-web
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Spark - Home</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <nav>
            <img src="Spark-Logo.png" alt="Spark Logo" class="logo">
            <ul>
                <li><a href="home.html">Home</a></li>
                <li><a href="our-team.html">Our Team</a></li>
                <li><a href="https://discord.gg/rjcDryDSuP">Support</a></li>
                <li><a href="faq.html">FAQ</a></li>
            </ul>
            <a href="https://discord.com/oauth2/authorize?client_id=1156019927577276456" class="btn invite-btn">Invite</a>
        </nav>
        <div class="hero">
            <h1>Spark</h1>
            <p>The future of ER:LC Staff, Game, and Server management</p>
            <a href="https://discord.com/oauth2/authorize?client_id=1156019927577276456" class="btn">Use Spark Now</a>
        </div>
    </header>

    <section id="features" class="features-section">
        <h2>Features</h2>
        <div class="features-grid">
            <div class="feature-card">
                <i class="fas fa-shield-alt feature-icon"></i>
                <h3>Secure</h3>
                <p>All data that our bot takes, is kept safe and secure</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-users feature-icon"></i>
                <h3>User Friendly</h3>
                <p>Easy to use with intuitive commands and a helpful support team.</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-trophy feature-icon"></i>
                <h3>Staff Management</h3>
                <p>We offer an array of commands to help manage your Discord and ER:LC staff.</p>
            </div>
            <div class="feature-card">
                <i class="fas fa-cogs feature-icon"></i>
                <h3>Server Management</h3>
                <p>We offer an array of commands to manage your Discord server and protect it.</p>
            </div>
        </div>
    </section>

    <section id="statistics" class="statistics-section">
        <h2>Statistics</h2>
        <div class="statistics-grid">
            <div class="stat-card">
                <i class="fas fa-server stat-icon"></i>
                <h3>Servers</h3>
                <p id="serverCount">30+</p>
            </div>
            <div class="stat-card">
                <i class="fas fa-user-friends stat-icon"></i>
                <h3>Users</h3>
                <p id="userCount">1k+</p>
            </div>
            <div class="stat-card">
                <i class="fas fa-tasks stat-icon"></i>
                <h3>Commands Executed</h3>
                <p id="commandCount">200+</p>
            </div>
        </div>
    </section>

    <section id="contact" class="contact">
        <h2>Contact Us</h2>
        <form id="contactForm">
            <input type="text" name="name" placeholder="Your Name" required>
            <input type="email" name="email" placeholder="Your Email" required>
            <select name="topic" required>
                <option value="" disabled selected>Select a Topic</option>
                <option value="General Inquiry">General Inquiry</option>
                <option value="Partnership Information">Partnership Information</option>
                <option value="Spark Premium">Spark Premium</option>
                <option value="Staff Application">Staff Application</option>
            </select>
            <textarea name="message" placeholder="Your Message" required></textarea>
            <button type="submit" class="btn">Send Message</button>
        </form>
    </section>

    <script src="https://cdn.emailjs.com/dist/email.min.js"></script>
    <script>
        (function(){
            emailjs.init("QGeZtmcb_bUY_HV2W"); // Replace with your actual EmailJS user ID
        })();

        document.getElementById('contactForm').addEventListener('submit', function(event) {
            event.preventDefault();

            emailjs.sendForm('service_88d3y5o', 'template_pz1f1p8', this)
                .then(function(response) {
                    alert('Your message has been sent successfully!', response.status, response.text);
                    // Optionally clear the form after successful submission
                    document.getElementById('contactForm').reset();
                }, function(error) {
                    alert('Failed to send your message. Please try again later.', error);
                });
        });
    </script>

    <footer>
        <p>&copy; 2024 Capyman. All rights reserved.</p>
    </footer>
</body>
</html>
