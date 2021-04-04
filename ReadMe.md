homework01-refactoring

## Index.html

Updated page title = <title>Horiseon Social Solution Services, Inc. | Marketing Agency</title>

Changed <div class="header"> to <header>

Added Span tag for the screen readers to know the div class="hero" is an image of a "Digital Marketing Meeting".

<section class="hero">
<span role="img" aria-label="Digital Marketing Meeting"></span>
</section>

Header > Fixed broken anchor link for "Search Engine Optimization" by adding an ID="search-engine-optimization" to that specific section in the <main>

<div class="descriptions" id="search-engine-optimization">

Added <main></main>around all of the Content, below </header> and above the <footer>.

Made a section <section class="services"> that has 3 sub-sections that share the same <div class="descriptions" id="">
but each has it's own unique id

<div class="descriptions" id="search-engine-optimization">
<div class="descriptions" id="online-reputation-management">
<div class="descriptions" id="social-media-marketing">

Added ALT text descriptions for each image that is listed inside each of the 3 Services sub-sections
<img src="./Assets/images/search-engine-optimization.jpg" class="float-left" alt="SEO guide notebook" />
<img src="./Assets/images/online-reputation-management.jpg" class="float-right" alt="Laptop displaying a Reputation dashboard showing a steady increase." />
<img src="./Assets/images/social-media-marketing.jpg" class="float-left" alt="Marketing team meeting with all social media represented." />

Made a section <section class="benefits"> that has 3 sub-sections that share the same class = <div class="explanations">

Added ALT text descriptions for each image that is listed for each of the 3 Benefits sub-sections
<img src="./Assets/images/lead-generation.png" alt="Lead Generation icon = A large cog is located halfway down into a vertical funnel. The funnel has a downward arrow on it. Below the spout of the funnel is a coin, circle with a US dollar symbol on it." />
<img src="./Assets/images/brand-awareness.png" alt="Brand Awareness icon = A person's torso wearing shirt and tie. The person's head is a giant lightbulb emmitting waves of light." />
<img src="./Assets/images/cost-management.png" alt="Cost Managemtn icon = Three different sized coins, circles each bearing a US dollar symbol, sit with a large cog in the background." />

Replaced <div class="footer"> with <footer>

Added Aria-level to have ALT text description of the heart emoji for screen readers. <h2 aria-level="Made with Heart/Love by Horiseon">Made with ❤️️ by Horiseon</h2>

## style.css

Consolidated the instances of font-family and default font color by adding them to the body
body {
background-color: #d9dcd6;
font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
"Lucida Sans", Arial, sans-serif;
color: #fff;
}

ADDED
header h1 .seo:hover {
background-color: #fff;
color: #2a607c;
}

CHANGED ALL related style references of .header div  
TO
nav

ADDED
a:hover {
color: #d9dcd6;
text-decoration: underline;
}

CONSLIDATED the font references in the various sections into a new MAIN section
main {
font-family: "Gill Sans", "Gill Sans MT", Calibri, "Trebuchet MS", sans-serif;
}

CHANGED .content TO .services

CHANGED THE NAMES AND CONSOLIDATED THE DUPLICATE DETAILS
.search-engine-optimization
.online-reputation-management
.social-media-marketing
TO
.descriptions {
margin-bottom: 20px;
padding: 50px;
height: 300px;
background-color: #0072bb;
}

.descriptions h2 {
margin-bottom: 20px;
font-size: 36px;
}
.descriptions img {
max-height: 200px;
}

.descriptions .float-left {
float: left;
margin-right: 25px;
}

.descriptions .float-right {
float: right;
margin-left: 25px;
}

CHANGED THE NAMES AND CONSOLIDATED THE DUPLICATE DETAILS
.benefits
.benefit-lead
.benefit-brand
.benefit-cost
.benefit-lead h3
.benefit-brand h3
.benefit-cost h3
.benefit-lead img
.benefit-brand img
.benefit-cost img
TO
.benefits {
margin-right: 20px;
padding: 20px;
clear: both;
float: right;
width: 20%;
height: 100%;
background-color: #2589bd;
}

.explanations {
margin-bottom: 32px;
}

.explanations h3 {
margin-bottom: 10px;
text-align: center;
}

.explanations img {
display: block;
margin: 10px auto;
max-width: 150px;
}

UPDATED the class = .footer to the tag = footer

Removed the font-family and ADDED the color for the text
.footer {
padding: 30px;
clear: both;
font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
text-align: center;
}
TO
footer {
padding: 30px;
clear: both;
text-align: center;
color: black;
}
AND
.footer h2 TO footer h2
