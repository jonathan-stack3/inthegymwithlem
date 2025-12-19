📘 LEM Basketball Training – Official Site

Developed by Stack3

A fully responsive, modern static website built for LEM Basketball Training — a professional basketball skills trainer.
The site showcases training packages, embedded Instagram training clips, and provides direct booking options via Calendly.
Deployed on AWS using S3, CloudFront, and ACM for a fast, secure, global experience.

🚀 Live Site

https://lem.stack3.tech

🏀 Features
✅ Training Packages Section

First session (free)

Monthly training plan (2×/week)

10-session pack (must be used in 45 days)

Clean neon-dark design matching brand identity

Buttons link directly to Calendly booking pages

🎥 Instagram Video Carousel

Custom horizontal scrolling carousel

Embedded public Instagram reels

Mobile swipe support

Arrow button navigation

Cards styled to match the site theme (neon + dark)

📅 Booking & Scheduling (via Calendly)

Trainers manage availability, scheduling, reminders, and payments

Website buttons link to Calendly event pages

Zero backend required — perfect for small businesses

⚡ Fast + Secure Deployment

Hosted on Amazon S3

Served globally via CloudFront CDN

Protected by AWS Certificate Manager (ACM) with HTTPS

Cache invalidation for instant updates

📂 Project Structure
lem-basketball-training/
│
├── index.html            # Main site markup
├── styles.css            # Global styling + carousel + packages
├── assets/               # Images / logos (if applicable)
│
└── README.md             # Project documentation

🔧 Tech Stack
Category	Technology
Hosting	AWS S3 (static website hosting)
CDN / SSL	AWS CloudFront + AWS ACM
Frontend	HTML, CSS, JavaScript
Booking	Calendly event booking links
Video Embeds	Instagram Reels embed API
Tools	Git, GitHub, VS Code
📘 Deployment Workflow
1️⃣ Update local files

Edit index.html, styles.css, or your assets.

2️⃣ Sync to S3

From your project folder:

aws s3 sync . s3://YOUR-BUCKET-NAME \
  --exclude ".git/*" \
  --exclude ".vscode/*"

3️⃣ Invalidate CloudFront cache
aws cloudfront create-invalidation \
  --distribution-id YOUR_DISTRIBUTION_ID \
  --paths "/*"

4️⃣ Commit + push to GitHub
git add .
git commit -m "Update site content"
git push origin main

🎥 Updating Video Clips

Get the Instagram Reel links from the trainer

Ensure they are public

Replace the URLs in the <blockquote class="instagram-media"> elements

The carousel will auto-format them

Save → Sync to S3 → Invalidate CloudFront

🏋️ Updating Training Packages

Update pricing, names, or descriptions inside the #programs section

Update the Calendly booking links (href="")

Save → Sync to S3 → Invalidate CloudFront

📅 Calendly Setup (Trainer Instructions)

The trainer must:

Create a Calendly account

Add three event types:

Free Session

Monthly Plan – 2× Per Week

10-Session Pack

Optional: Connect Stripe/PayPal for payments

Send the event URLs to the developer (Stack3)

URLs get plugged into the site buttons

📈 Future Enhancements (Optional)

Stripe subscription integration

Member login portal for recurring clients

Blog or training tips section

Automated SMS reminders

Custom admin dashboard

More advanced carousel with thumbnails

💼 Developer

Developed by:

Stack3
