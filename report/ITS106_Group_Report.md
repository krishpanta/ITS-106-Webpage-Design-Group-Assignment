# ITS106 – Webpage Design and Development
## Group Project Report — T1 2026
### Sydney Global Adventures Website

**Subject:** ITS106 Webpage Design and Development  
**Project:** Group Project — Multi-Page Website  
**Group Members:** [Member 1 Name], [Member 2 Name], [Member 3 Name]  
**Campus:** SydMain  
**Submission:** Week 10  

---

## 1. Introduction

The rapid growth of online commerce and digital services has transformed how businesses engage with customers, and the travel industry is no exception. Today, a professional and functional website is no longer a luxury for travel agencies — it is a fundamental requirement for attracting clients, building trust, and enabling seamless bookings. This project was undertaken as part of the ITS106 Webpage Design and Development subject and required our group to design and develop a fully functional multi-page website for a fictional travel agency named **Sydney Global Adventures**.

The objective of this project was to demonstrate our collective proficiency in the three core technologies of modern web development: HTML, CSS, and JavaScript. Beyond technical implementation, the project required us to apply principles of responsive design, accessibility, and user experience (UX) design to produce a website that functions effectively across a range of devices and screen sizes.

Sydney Global Adventures is a fictional Sydney-based travel agency that offers curated travel packages to destinations across Asia, Europe, the Pacific, and the Middle East. The website was designed to reflect the professionalism of a real-world travel business, featuring five complete pages: a Homepage, a Destinations and Packages page, a Tours and Experiences page, an About Us and Team page, and a Contact and Booking page. Each page was assigned to individual group members to ensure balanced contribution and clear accountability.

The importance of this project extends beyond the classroom. Web development skills are in high demand across the IT and business industries, and the ability to design and build accessible, responsive, and interactive websites is a critical competency for any modern technology professional. This report documents the process, tools, and outcomes of our development work, as well as the challenges we faced and the solutions we implemented.

---

## 2. Methodology

### 2.1 Planning and Division of Work

Our group began by carefully reviewing the project brief and dividing responsibilities across three members to ensure balanced workloads. The division was as follows:

- **Member 1** was responsible for the Homepage (index.html) and the Destinations and Packages page (destinations.html), as well as overall management of the shared navigation bar.
- **Member 2** was responsible for the Tours and Experiences page (tours.html) and the About Us and Team page (about.html), including content research and team profiles.
- **Member 3** was responsible for the Contact and Booking page (contact.html) with JavaScript form validation, and the preparation of this written report.

All three members contributed equally to the shared CSS stylesheet and reviewed each other's work during testing sessions.

### 2.2 Tools and Technologies

The following tools and technologies were used throughout the project:

- **HTML5** — Used for structuring all five web pages, including semantic elements such as `<nav>`, `<section>`, `<footer>`, and `<article>`.
- **CSS3** — Used for styling, layout (using CSS Grid and Flexbox), animations, and responsive design via media queries. All pages shared a single stylesheet (`css/style.css`) to ensure visual consistency across the site.
- **JavaScript (ES6)** — Used for interactive features including the hero image slideshow on the homepage, the destination filter functionality, the mobile navigation hamburger toggle, and JavaScript-based form validation on the Contact page.
- **Google Fonts** — Used to import the *Playfair Display* (display headings) and *DM Sans* (body text) typefaces, providing a professional and modern typographic pairing.
- **Visual Studio Code** — Primary code editor used by all group members, with the Live Server extension for real-time browser previewing.
- **GitHub** — Used for version control and collaboration, allowing all members to work on the codebase simultaneously without overwriting each other's work.
- **Browser DevTools** — Chrome and Firefox developer tools were used extensively for debugging, responsive design testing, and performance checking.

### 2.3 File Structure

The project follows a clean, logical folder structure:

```
sydney-global-adventures/
├── index.html              (Homepage — Member 1)
├── css/
│   └── style.css           (Shared stylesheet — all members)
└── pages/
    ├── destinations.html   (Member 1)
    ├── tours.html          (Member 2)
    ├── about.html          (Member 2)
    └── contact.html        (Member 3)
```

### 2.4 Development Approach

We followed an iterative development process. The shared stylesheet and navigation bar were built first to establish a consistent visual foundation. Each member then developed their assigned pages independently, following agreed-upon CSS variable naming conventions and class structures to maintain consistency.

CSS Custom Properties (variables) were used extensively to define the colour palette, typography, spacing, and border radius values, making the design system easy to update globally from a single location. For example, the primary teal colour (`#0a6e8a`) and accent orange (`#f4a12e`) were defined once as `--primary` and `--accent` and referenced throughout the stylesheet.

---

## 3. Outcome

### 3.1 Website Pages and Features

**Homepage (index.html)**  
The homepage serves as the primary entry point for visitors and introduces the Sydney Global Adventures brand. Key features include an auto-advancing hero slideshow with dot navigation, an animated ticker banner advertising current travel deals, and a curated featured deals section displaying three destination cards with pricing. A "Why Choose Us" section highlights key selling points. The page includes smooth CSS scroll behaviour and entry animations using `@keyframes` for a polished user experience.

**Destinations and Packages (destinations.html)**  
This page presents six travel destinations — Bali, Paris, Tokyo, New Zealand, Dubai, and the Maldives — using a responsive card grid layout. Each card includes the destination name, country, a description, a list of package inclusions, the duration, and the starting price. A JavaScript-powered filter system allows users to filter destinations by region (Asia, Europe, Pacific, Middle East), enhancing discoverability and user control.

**Tours and Experiences (tours.html)**  
This page showcases five distinct travel experience categories: Adventure Tours, Cultural Tours, Luxury Holidays, Family Packages, and Cruise Trips. Each tour type is presented in an alternating two-column layout (text and visual), creating visual rhythm and preventing monotony. Each section includes specific highlights, activity descriptions, duration ranges, pricing, and a link to the booking page.

**About Us and Team (about.html)**  
This page introduces the agency's background and mission, presents a vertical history timeline tracing the company from 2010 to 2026, and profiles six fictional team members with their specialisations and experience. A values section at the bottom reinforces the brand's commitment to trust, sustainability, and customer care.

**Contact and Booking (contact.html)**  
The contact page presents all agency contact details alongside a comprehensive booking enquiry form. The form collects the visitor's first name, last name, email, phone number, preferred destination (via a dropdown), travel dates, number of travellers, and a message. Full JavaScript validation is implemented, checking for empty required fields, valid email format (using a regular expression), and minimum message length. Upon successful submission, a success confirmation message is displayed and the submitted entry is rendered on the page, satisfying the requirement to display submitted entries on the webpage.

### 3.2 Responsive Design

Responsive design was implemented using CSS Grid, Flexbox, and a three-tier media query system targeting screen widths of 1024px, 768px, and 480px. On mobile devices, the navigation bar collapses into a hamburger menu toggled via JavaScript. Grid layouts transition from three or four columns on desktop to two columns on tablet and a single column on mobile, ensuring usability across all device sizes.

### 3.3 Accessibility

To ensure accessibility, all images include descriptive `alt` attributes, colour contrast ratios were checked against WCAG 2.1 guidelines, form fields include associated `<label>` elements, and the navigation toggle button uses an `aria-label` attribute. Semantic HTML elements were used throughout to support screen reader compatibility.

---

## 4. Challenges

### 4.1 Shared Stylesheet Coordination

One of the first challenges was coordinating a shared CSS file across three developers. Early in the project, conflicting class names caused styling inconsistencies. We resolved this by creating a shared naming convention document and prefixing page-specific classes (e.g., `.dest-card` for the destinations page) to avoid conflicts.

### 4.2 JavaScript Form Validation

Implementing reliable client-side form validation for the booking page required careful handling of multiple edge cases — empty fields, invalid email formats, and date validation. The email validation was implemented using the regular expression `/^[^\s@]+@[^\s@]+\.[^\s@]+$/`, which checks for the presence of an `@` symbol and a valid domain structure. Live validation on field blur (`blur` event) was also added to provide real-time feedback without waiting for form submission.

### 4.3 Responsive Layout on Safari

During testing, we discovered that certain CSS Grid configurations rendered differently on Safari mobile compared to Chrome and Firefox. Specifically, the `gap` property within flex containers required a workaround using `margin` instead of `gap` for older Safari versions. This was identified using browser DevTools and corrected without breaking the layout on other browsers.

### 4.4 Hero Slideshow Timing

The homepage hero slideshow initially had a flickering issue when transitioning between slides due to conflicting opacity transitions. We resolved this by ensuring that only one slide had the `active` class at any time and that the CSS `transition` property on `.hero-slide` was set to `opacity 1.2s ease` with sufficient duration to avoid abrupt changes.

---

## 5. Conclusion

This project provided our group with valuable hands-on experience in building a real-world, multi-page website from the ground up. Over the course of the trimester, we developed practical skills in HTML structure, CSS layout techniques (including Grid and Flexbox), CSS animations, JavaScript interactivity, form validation, and responsive design for multiple device sizes.

Working as a team introduced additional skills in project coordination, version control with GitHub, and communicating technical decisions collaboratively. Dividing responsibilities by page allowed each member to develop deep familiarity with their section, while peer review during testing ensured that quality was maintained across the entire site.

The Sydney Global Adventures website successfully meets all project requirements: five complete pages, responsive design, JavaScript interactivity, a validated booking form, and a consistent professional design. If extended further, the site could benefit from a backend form submission system, a real-time flight search API integration, and a content management system (CMS) to allow non-technical users to update destination content.

Overall, this project strengthened our confidence in web development and demonstrated that a well-structured, visually appealing, and functional website can be built effectively using only HTML, CSS, and JavaScript — the foundational technologies of the modern web.

---

## 6. References

[1] W3Schools, "HTML Tutorial," *W3Schools Online Web Tutorials*, 2024. [Online]. Available: https://www.w3schools.com/html/. [Accessed: May 2026].

[2] Mozilla Developer Network, "CSS: Cascading Style Sheets," *MDN Web Docs*, 2024. [Online]. Available: https://developer.mozilla.org/en-US/docs/Web/CSS. [Accessed: May 2026].

[3] Mozilla Developer Network, "JavaScript Reference," *MDN Web Docs*, 2024. [Online]. Available: https://developer.mozilla.org/en-US/docs/Web/JavaScript. [Accessed: May 2026].

[4] W3C, "Web Content Accessibility Guidelines (WCAG) 2.1," *World Wide Web Consortium*, 2018. [Online]. Available: https://www.w3.org/TR/WCAG21/. [Accessed: May 2026].

[5] A. Duckett, *HTML & CSS: Design and Build Websites*. Indianapolis, IN: John Wiley & Sons, 2011.

[6] CSS-Tricks, "A Complete Guide to CSS Grid," *CSS-Tricks*, 2023. [Online]. Available: https://css-tricks.com/snippets/css/complete-guide-grid/. [Accessed: May 2026].

[7] Google Fonts, "Google Fonts API," *Google Developers*, 2024. [Online]. Available: https://fonts.google.com/. [Accessed: May 2026].

---

*Word count: approximately 1,580 words (excluding references, headings, and code blocks)*

*ITS106 Group Project T1 2026 — Sydney Global Adventures*
