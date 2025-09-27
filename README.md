
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>College Tech Fest 2026</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Comic+Neue:wght@700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <style>
        /* Basic Reset and Global Styles */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        :root {
            --primary-bg-color: #f0f0f0; /* Light Gray */
            --secondary-bg-color: #ffffff; /* White */
            --accent-color-1: #ff6347; /* Tomato Red */
            --accent-color-2: #4682b4; /* Steel Blue */
            --accent-color-3: #32cd32; /* Lime Green */
            --text-dark: #333333; /* Dark Gray */
            --text-light: #555555; /* Medium Gray */
            --font-main: 'Comic Neue', cursive; /* Playful Header Font */
            --font-secondary: 'Open Sans', sans-serif; /* Readable Body Font */
        }

        body {
            background-color: #c0d9e9; /* A slightly duller, common blue */
            color: var(--text-dark);
            font-family: var(--font-secondary);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 15px; /* Slightly less padding */
        }

        .poster-container {
            background-color: var(--secondary-bg-color);
            max-width: 700px; /* Slightly smaller max-width */
            width: 100%;
            padding: 30px; /* Reduced padding */
            border-radius: 8px; /* Sharper corners */
            box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.2); /* More obvious, slightly offset shadow */
            border: 3px dashed var(--accent-color-3); /* Fun, dashed border */
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        /* Header */
        .event-header {
            margin-bottom: 25px; /* Less margin */
            padding-bottom: 15px;
            border-bottom: 2px solid var(--accent-color-1); /* Solid, simple divider */
        }

        .event-title {
            font-family: var(--font-main);
            font-size: 3.5rem; /* Large and in-your-face */
            font-weight: 700;
            color: var(--accent-color-1);
            text-transform: uppercase;
            letter-spacing: 1px; /* Less refined letter spacing */
            line-height: 1.2;
            margin-bottom: 8px;
            text-shadow: 2px 2px 0px #ffe0b3; /* Simple, noticeable text shadow */
        }

        .event-tagline {
            font-family: var(--font-secondary);
            font-size: 1.1rem; /* Slightly smaller tagline */
            color: var(--text-light);
            font-style: italic;
            font-weight: 400;
        }

        /* Details Section */
        .details-section {
            display: flex;
            justify-content: space-around; /* Simple spacing */
            gap: 15px; /* Smaller gap */
            margin-bottom: 30px;
            padding: 15px 0;
            background-color: var(--primary-bg-color); /* Different background for this section */
            border-radius: 5px;
            box-shadow: inset 0 0 8px rgba(0, 0, 0, 0.1); /* Inner shadow for depth */
        }

        .details-item {
            font-size: 1rem;
            font-weight: 600;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 5px;
        }

        .detail-label {
            color: var(--accent-color-2);
            font-family: var(--font-secondary);
            font-weight: 700;
            margin-bottom: 5px;
            text-transform: uppercase;
            font-size: 0.85rem;
            letter-spacing: 0.5px;
        }

        .detail-value {
            color: var(--text-dark);
            font-size: 1.3rem;
            font-family: var(--font-main); /* Using main font for values too */
        }

        /* Speakers Section */
        .speakers-section h2 {
            font-family: var(--font-main);
            color: var(--accent-color-1);
            margin-bottom: 20px;
            font-size: 2.2rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            border-bottom: 1px dashed var(--accent-color-2); /* Another dashed border */
            padding-bottom: 10px;
        }

        .speaker-list {
            display: flex; /* Using flex for simplicity */
            justify-content: center;
            flex-wrap: wrap; /* Allow wrapping */
            gap: 20px; /* Closer gap */
            margin-bottom: 35px;
        }

        .speaker-card {
            background-color: var(--primary-bg-color);
            padding: 15px;
            border-radius: 50px; /* More rounded, almost pill-shaped */
            border: 2px solid var(--accent-color-2);
            text-align: center;
            width: 180px; /* Fixed width for a slightly less refined look */
            box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.15); /* Softer shadow */
        }

        .speaker-photo {
            width: 80px; /* Smaller photo */
            height: 80px;
            border-radius: 50%;
            border: 3px solid var(--accent-color-3); /* Green border */
            object-fit: cover;
            margin-bottom: 10px;
        }

        .speaker-name {
            font-size: 1.1rem;
            font-family: var(--font-main);
            color: var(--text-dark);
            margin-bottom: 5px;
        }

        .speaker-bio {
            font-size: 0.8rem; /* Smaller bio text */
            color: var(--text-light);
            line-height: 1.4;
        }

        /* Call to Action (CTA) Section */
        .cta-section {
            margin-bottom: 30px;
        }

        .cta-button {
            display: inline-block;
            padding: 12px 30px; /* Smaller button */
            background-color: var(--accent-color-1); /* Solid background */
            color: white;
            font-family: var(--font-main);
            font-weight: 700;
            font-size: 1.1rem;
            text-decoration: none;
            border-radius: 5px; /* Square button */
            transition: transform 0.2s ease;
            text-transform: uppercase;
            letter-spacing: 0.8px;
            box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.2); /* Simple shadow */
            border: none;
        }

        .cta-button:hover {
            transform: scale(1.05);
            background-color: var(--accent-color-2); /* Color change on hover */
        }

        .cta-text {
            margin-top: 10px;
            font-style: normal; /* Not italic */
            color: var(--text-dark);
            font-size: 0.95rem;
            font-weight: 600; /* Bolder text */
        }

        /* Footer */
        footer {
            font-size: 0.75rem; /* Smaller footer text */
            color: var(--text-light);
            margin-top: 20px;
            border-top: 1px solid #ccc;
            padding-top: 15px;
        }

        /* Responsiveness - Still trying to make it work! */
        @media (max-width: 768px) {
            .poster-container {
                padding: 20px;
                border: 2px dashed var(--accent-color-3); /* Adjusted border on mobile */
            }

            .event-title {
                font-size: 2.8rem;
            }

            .event-tagline {
                font-size: 1rem;
            }

            .details-section {
                flex-direction: column;
                gap: 10px;
            }

            .details-item {
                font-size: 0.9rem;
            }

            .detail-value {
                font-size: 1.1rem;
            }

            .speaker-list {
                gap: 15px;
            }

            .speaker-card {
                width: 150px; /* Smaller cards on mobile */
                padding: 10px;
            }

            .speaker-photo {
                width: 60px;
                height: 60px;
            }

            .speaker-name {
                font-size: 1rem;
            }

            .speaker-bio {
                font-size: 0.75rem;
            }

            .cta-button {
                padding: 10px 25px;
                font-size: 1rem;
            }
        }

        @media (max-width: 480px) {
            .event-title {
                font-size: 2rem;
            }

            .event-tagline {
                font-size: 0.9rem;
            }

            .speakers-section h2 {
                font-size: 1.8rem;
            }
        }
    </style>
</head>
<body>
    <div class="poster-container">
        <header class="event-header">
            <h1 class="event-title">College Tech Fest 2026</h1>
            <p class="event-tagline">Where Ideas Spark & Code Flows (Mostly)!</p>
        </header>
        <main>
            <section class="details-section">
                <div class="details-item">
                    <span class="detail-label">When</span>
                    <span class="detail-value">April 1-3, 2026</span>
                </div>
                <div class="details-item">
                    <span class="detail-label">Where</span>
                    <span class="detail-value">Campus Auditorium & Zoom</span>
                </div>
            </section>

            <section class="speakers-section">
                <h2>Cool Speakers & Profs</h2>
                <div class="speaker-list">
                    <div class="speaker-card">
                        <img src="https://via.placeholder.com/150/ff6347/ffffff?text=Prof.+Smith" alt="Professor Smith" class="speaker-photo">
                        <h3 class="speaker-name">Prof. Smith</h3>
                        <p class="speaker-bio">Intro to CS Guru</p>
                    </div>
                    <div class="speaker-card">
                        <img src="https://via.placeholder.com/150/4682b4/ffffff?text=Dr.+Jones" alt="Dr. Jones" class="speaker-photo">
                        <h3 class="speaker-name">Dr. Jones</h3>
                        <p class="speaker-bio">Robotics Enthusiast</p>
                    </div>
                    <div class="speaker-card">
                        <img src="https://via.placeholder.com/150/32cd32/ffffff?text=Guest+Dev" alt="Guest Developer" class="speaker-photo">
                        <h3 class="speaker-name">Guest Dev</h3>
                        <p class="speaker-bio">Recent Alumni (Cool!)</p>
                    </div>
                </div>
            </section>

            <section class="cta-section">
                <a href="#" class="cta-button">Sign Up HERE!</a>
                <p class="cta-text">Don't miss out! It's gonna be awesome!</p>
            </section>
        </main>
        <footer>
            <p>&copy; 2026 College Tech Fest Committee. (Probably)</p>
        </footer>
    </div>
</body>
</html>
