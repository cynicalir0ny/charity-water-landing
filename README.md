# charity-water-landing
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Charity:Water</title>
  <link rel="stylesheet" href="styles.css" />
</head>
<body>
  <header class="top-bar">
    <div class="logo">
      <img src="img/0.png" alt="Charity:Water logo">
      <span>Charity:Water</span>
    </div>
    <div class="buttons">
      <a href="#" class="btn">Become an Ambassador</a>
      <a href="#" class="btn secondary">Give</a>
    </div>
  </header>

  <section class="hero">
    <div class="overlay">
      <h1>Your Passion. Their Future. Our Mission.</h1>
      <p class="subhead">
        Fuel clean water projects with proven impact and complete transparency, and help shape a world where everyone has access to life’s most basic need.
      </p>
      <p class="support-text highlight-bg">
        Supporting Charity: Water can make a tangible difference in providing clean water to communities in need, aligning with desires to make measurable impacts and passions for global sustainability. This partnership offers transparency and data-driven results that ensure your contribution directly addresses critical water challenges.
      </p>
    </div>
  </section>

  <section class="info-section">
    <div class="image-side">
      <img src="img/clean and dirty water cup next to each other in a  struggling country.jpg" alt="Clean vs dirty water">
    </div>
    <div class="text-side">
      <p class="caption">
        It’s more than an image; it’s a story of transition: The photo above captures the powerful transformation from contaminated water to clean, life-sustaining water—symbolizing the heart of our mission.
      </p>
      <ul class="impact-list">
        <li>💧 $30 = clean water for one person</li>
        <li>✅ 100% funds go to field projects</li>
        <li>📍 GPS-tracked well locations</li>
      </ul>
    </div>
  </section>

  <footer class="bottom-bar">
    Not ready to donate? <a href="#">Join our mission as an advocate, intern, or ambassador.</a>
  </footer>
  <!-- Simple page footer at the very bottom -->
  <footer class="page-footer">
    <!-- For beginners: This is a simple copyright notice -->
    &copy; 2024 Charity:Water. All rights reserved.
  </footer>
  <!-- 
    For beginners: 
    To publish your website, upload this HTML file, your CSS file, and your images folder to a web host or use GitHub Pages.
    Then share the link with others!
  -->
</body>
</html>
/* charity: water Brand Colors & Fonts

Primary Colors:
- Yellow:     #FFC907
- Blue:       #2E9DF7

Secondary Colors:
- Light Blue: #8BD1CB
- Green:      #4FCB53
- Orange:     #FF902A
- Red:        #F5402C
- Dark Green: #159A48
- Pink:       #F16061

Fonts:
- Proxima Nova
- Avenir

*/
/* GENERAL PAGE STYLES */
body {
  margin: 0;
  font-family: Arial, sans-serif;
  line-height: 1.5;
  background-color: #f8f8f8;
  color: #222;
}

/* HEADER STYLES */
.top-bar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #f5f5f5;
  padding: 6px 16px;
  position: sticky;
  top: 0;
  z-index: 1000; /* Make sure header stays above the page content when scrolling */
  /* For beginners: z-index keeps the header on top of everything else */
}

/* Make the logo and buttons slightly bigger */
.logo {
  display: flex;
  align-items: center;
  font-size: 1.1em; /* slightly bigger font size */
  font-weight: bold;
}

.logo img {
  margin-right: 10px;
  border-radius: 50%;
  width: 32px;   /* slightly bigger logo image */
  height: 32px;  /* slightly bigger logo image */
}

.buttons .btn {
  background: #f4a300;
  color: white;
  padding: 7px 14px; /* slightly bigger button padding */
  margin-left: 10px;
  text-decoration: none;
  border-radius: 4px;
  font-weight: bold;
  font-size: 1em; /* slightly bigger button text */
  transition: background 0.3s, transform 0.2s;
}

.buttons .btn:hover {
  background: #ffb300;
  transform: translateY(-2px) scale(1.05);
}

/* HERO SECTION */
.hero {
  /* Use the child playing image as the background */
  background: url('img/blurred background child playing with clean water in their country.jpg') no-repeat center center/cover;
  color: white;
  position: relative;
  padding: 56px 16px 100px 16px;
  display: flex;
  flex-direction: row;         /* Place overlay and image side by side */
  justify-content: flex-start; /* Overlay on the left */
  align-items: flex-end;       /* Overlay at the bottom */
  min-height: 380px;
  transition: padding 0.3s;
}

/* Remove the splash-img styles since we no longer use the <img> tag for the child image */
.splash-img {
  display: none;
}

/* Overlay with background behind the words, stays in place over the hero image */
.overlay {
  max-width: 420px;
  width: 100%;
  background: rgba(30, 30, 30, 0.7); /* dark background for readability */
  padding: 24px 18px;
  margin: 0 120px 40px 0; /* increase right margin to move overlay further from the child image */
  border-radius: 12px;
  box-shadow: 0 3px 16px rgba(0,0,0,0.16);
  position: absolute; /* position overlay over the hero image */
  top: 56px;          /* distance from the top of the hero section */
  left: 16px;         /* distance from the left of the hero section */
  z-index: 2;         /* make sure overlay is above the image */
  /* For beginners: This keeps the text box in place over the image */
}

/* Make sure the hero section has enough height for the overlay */
.hero {
  min-height: 380px;
}

/* Remove the old overlay styles */
.overlay {
  background: none; /* No background color */
  padding: 0;
  margin: 0 120px 40px 0; /* increase right margin to move overlay further from the child image */
  border-radius: 0;
  box-shadow: none;
  transition: box-shadow 0.3s, transform 0.3s;
  /* For beginners: This puts the text box on the left side of the hero section and away from the child image */
}

.overlay:hover {
  box-shadow: 0 6px 24px rgba(0,0,0,0.25);
  transform: scale(1.03);
}

.hero h1 {
  font-size: 2.2em; /* revert to previous size */
  color: #ffd600;
  margin-bottom: 20px;
  text-shadow: 1px 1px 6px #222;
  /* Remove width, letter-spacing, text-align, display so words are side by side */
}

.hero h1,
.hero .subhead {
  color: #ffc907; /* Make heading and subhead yellow */
}

.subhead {
  font-size: 0.8em; /* make the subhead text smaller for beginners */
  color: #ffc907;
  margin-bottom: 18px;
  text-shadow: 1px 1px 4px #222;
  /* For beginners: This is a simple style for the subhead text */
}

.support-text {
  font-size: 1em; /* revert support text to previous size */
  color: #003366; /* dark blue for support text */
  margin-bottom: 0;
  text-shadow: 1px 1px 4px #222;
  /* For beginners: This is a simple style for the support text */
}

/* Responsive: Stack overlay and image vertically on small screens */
@media (max-width: 900px) {
  .hero {
    flex-direction: column;
    align-items: center;
    padding: 36px 8px 60px 8px;
    min-height: 320px;
    text-align: center;
  }
  .overlay {
    position: static;
    margin: 0 0 24px 0;
    max-width: 80vw;   /* make overlay even smaller on small screens */
    width: 100%;
    border-radius: 10px;
  }
}

/* INFO SECTION */
.info-section {
  display: flex;
  flex-wrap: wrap;
  background: #e9f5f2;
  padding: 40px 20px;
  justify-content: center;
  gap: 40px;
}

/* Make images in info-section responsive */
.image-side img {
  width: 100%;
  max-width: 320px;
  transition: transform 0.3s;
}

.image-side img:hover {
  transform: scale(1.04) rotate(-2deg);
}

.caption {
  max-width: 400px;
  color: #2b4c3b;
  font-size: 1em;
}

/* Responsive: Info section stacks vertically on small screens */
@media (max-width: 700px) {
  .info-section {
    flex-direction: column;
    gap: 20px;
    padding: 20px 8px;
    transition: padding 0.3s;
  }
  .caption {
    max-width: 100%;
  }
}

.impact-list {
  margin-top: 20px;
  list-style: none;
  padding: 0;
  background: #fff9c4;
  border-radius: 8px;
  padding: 15px;
  font-weight: bold;
}

.impact-list li {
  margin: 8px 0;
}

/* FOOTER */
.bottom-bar {
  background: #111;
  color: white;
  padding: 15px;
  text-align: center;
  font-size: 0.9em;
}

.bottom-bar a {
  color: #f4a300;
  text-decoration: none;
  font-weight: bold;
}

/* Simple page footer styles */
.page-footer {
  background: #222;           /* dark background */
  color: #fff;                /* white text */
  text-align: center;         /* center the text */
  padding: 10px 0;            /* space above and below */
  font-size: 0.85em;          /* slightly smaller text */
  margin-top: 0;              /* no extra space above */
}

/* ===========================
   Responsive Styles for Mobile
   ===========================
   We use media queries to change the layout and font sizes on smaller screens (like phones).
   This helps make the website easier to read and use on any device.
*/
@media (max-width: 600px) {
  /* Make header stack vertically on small screens */
  .top-bar {
    flex-direction: column;
    align-items: flex-start;
    padding: 10px;
  }

  .logo {
    margin-bottom: 10px;
  }

  .buttons .btn {
    margin-left: 0;
    margin-right: 10px;
    margin-bottom: 8px;
    display: inline-block;
  }

  /* Make hero section padding smaller and text centered */
  .hero {
    padding: 40px 10px 60px 10px;
    text-align: center;
  }

  .overlay {
    padding: 15px;
    max-width: 90vw;   /* make overlay smaller on very small screens */
  }

  .hero h1 {
    font-size: 1.5em;
  }

  .subhead,
  .support-text {
    font-size: 1em;
  }

  /* Hide the splash image on small screens to save space */
  .splash-img {
    display: none;
  }

  /* Stack info section vertically */
  .info-section {
    flex-direction: column;
    gap: 20px;
    padding: 20px 10px;
  }

  .image-side img {
    width: 100%;
    max-width: 300px;
    margin: 0 auto;
    display: block;
  }

  .caption {
    font-size: 0.95em;
    max-width: 100%;
  }

  .impact-list {
    font-size: 0.95em;
    padding: 10px;
  }

  /* Footer font size smaller on mobile */
  .bottom-bar {
    font-size: 0.85em;
    padding: 10px;
  }
}

/* For beginners: This class adds a light background and padding to make text easier to read */
.highlight-bg {
  background-color: #fffde7; /* very light yellow */
  padding: 12px;
  border-radius: 8px;
  color: #003366; /* keep the text dark blue for contrast */
  margin-top: 10px;
  margin-bottom: 10px;
  /* Remove text-shadow to make the text sharper and easier to read */
  text-shadow: none;
  /* For beginners: Use this class on any text you want to highlight */
}

/* 
  You can add more media queries for tablets or larger screens if needed.
  Media queries help make your website look good on all devices!
*/
