# raasofyoga.github.io
from pathlib import Path
from zipfile import ZipFile

# Create the directory and HTML file
project_dir = Path("/mnt/data/tejas_hatha_yoga_site")
project_dir.mkdir(parents=True, exist_ok=True)
html_file = project_dir / "index.html"

html_content = """<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tejas Hatha Yoga</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background: #f5f5f5;
      color: #333;
    }
    header {
      background: #1e3d59;
      color: #fff;
      padding: 2rem;
      text-align: center;
    }
    nav {
      background: #16324f;
      color: white;
      display: flex;
      justify-content: center;
      padding: 1rem;
    }
    nav a {
      color: white;
      margin: 0 1rem;
      text-decoration: none;
    }
    section {
      padding: 2rem;
      max-width: 900px;
      margin: auto;
    }
    footer {
      text-align: center;
      padding: 2rem;
      background: #1e3d59;
      color: white;
    }
  </style>
</head>
<body>
  <header>
    <h1>Tejas Hatha Yoga</h1>
    <p>Classical Hatha Yoga in its Purest Form</p>
  </header>

  <nav>
    <a href="#about">About</a>
    <a href="#benefits">Benefits</a>
    <a href="#programs">Programs</a>
    <a href="#contact">Contact</a>
  </nav>

  <section id="about">
    <h2>What is Classical Hatha Yoga?</h2>
    <p>
      Classical Hatha Yoga is a profound science of aligning the body, mind, emotions, and energies. Passed down in its purest form, it is not merely physical exercise, but a doorway to transformation, self-realization, and inner balance.
    </p>
    <p>
      With its roots in ancient yogic traditions, Classical Hatha Yoga goes beyond fitness – it is a sacred process to establish absolute balance and harmony within. The practices are designed to bring stability, enhance clarity, and deepen inner stillness.
    </p>
  </section>

  <section id="benefits">
    <h2>How It Benefits You</h2>
    <ul>
      <li>Enhances physical strength, flexibility, and stamina</li>
      <li>Balances the body’s energy system and boosts vitality</li>
      <li>Stabilizes emotions and sharpens mental clarity</li>
      <li>Improves sleep quality and reduces stress levels</li>
      <li>Aligns body and mind to support spiritual growth</li>
      <li>Brings a sense of peace, joy, and inner stability</li>
    </ul>
  </section>

  <section id="programs">
    <h2>Our Offerings</h2>
    <h3>Offline Programs</h3>
    <p>
      Conducted in Kannur and surrounding areas, these in-person sessions include Surya Kriya, Yogasanas, Angamardana, and tailored workshops for children, women, and senior citizens.
    </p>
    <h3>Online Sessions</h3>
    <p>
      Join from anywhere through guided Zoom sessions. Perfect for working professionals, travelers, or those who prefer practicing from home. Includes live classes, recordings, and follow-up support.
    </p>
    <h3>Private Sessions</h3>
    <p>
      Personalized one-on-one sessions designed to meet your individual needs, be it for health, emotional wellbeing, or spiritual exploration. Available both online and offline.
    </p>
  </section>

  <section id="contact">
    <h2>Contact & Bookings</h2>
    <p>Email: tejas@yogicbalance.in</p>
    <p>Phone/WhatsApp: +91-XXXXXXXXXX</p>
    <p>Follow us on Instagram: @tejas.hatha.yoga</p>
  </section>

  <footer>
    <p>&copy; 2025 Tejas Hatha Yoga | Designed with heart in Kannur</p>
  </footer>
</body>
</html>
"""

# Write the HTML file
html_file.write_text(html_content)

# Create a zip file
zip_path = "/mnt/data/tejas_hatha_yoga_site.zip"
with ZipFile(zip_path, "w") as zipf:
    zipf.write(html_file, arcname="index.html")

zip_path
