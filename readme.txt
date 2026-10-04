--Readme document for Sherry Tram, smtram@uci.edu--

A reminder on academic integrity, as described in the syllabus.

In general, the course staff expects that you will look at code and examples from many online resources as part of the assignments, particularly to resolve syntax and understand frameworks. We expect that you'll use other libraries you find, and will even require it in some assignments. These practices are often critical to the work of developers today. The best developers are adept at interpreting the examples they see, customizing them to their specific situation, and citing their sources so they can find them later. We expect you to do the same.

While learning from examples is encouraged, attempting to pass an existing project or example from the web as your own is not allowed. If you ever have a question about what is or is not appropriate, feel free to ask the course staff!

Talking to classmates about class material, assignment requirements, etc. is a great way to verify ideas and get feedback. But this distinctly does *not* permit attempting to pass off someone else’s code as your own. Talking over ideas and approaches is allowed, but the work that you produce and submit must be your own.

1. How many assignment points do you believe you completed (replace the *'s with your numbers)?

10/10
- 1/1 Readme
- 2/2 Basic HTML content
- 1/1 Basic CSS styling
- 1/1 Advanced feature
- 2/2 Responsive layout
- 1/1 Passes validation checks
- 2/2 Embraces spirit of the assignment

2. What (a) basic features, (b) CSS features, and (c) advanced features did you include in your portfolio?

(a) Basic features
    - Images with descriptive alt text (hero images, folder icons, project images)
    - Headings (different levels) and paragraph text on each page
    - Links to external pages: Github, Linkedin, mailto, project pages
    - Mulitple pages with working navagation bar between them: index.html (home), projects.html, about.html
    - Semantic HTML tags: header, nav, main, section, article, figure/figcaption, footer
    - Custom icons from Font Awesome (social icons in footer and about.html page)

(b) CSS features
    - Padding and margins to space out and indent content
    - Custom color palette (cream, brown, green) stored as CSS variables
    - Custom fonts from Google Fonts (Gaegu and DM Sans) with fallback fonts
    - Hover and keyboard focus effects (drop shawdow, button color swap, folder captions)

(c) Advanced features
    - Navagation bar with folder icons that highlight the current page (aria-current)
    - Complex layouts built with CSS flexbox and grid (hero section, folder directory, 2-column project grid, "currently into" row)
    - Responsive design: fluid sizing with clamp() and percentages, plus breakpoints that stack the hero, folders, and project grid on smaller screens
    - Descendant/nested selectors (for example .site-header nav a, .dir-card:hover .hovertext)
    - A "skip to content" link for keyboard and screen reader users

Changes I made to the portfolio I already had, to meet this assignment:
- Added a doctype, lang attribute, charset, and viewport meta tag so the pages validate
  and work on phones
- Fixed HTML errors (unclosed tags, duplicate ids, a nav placed outside the body)
- Combined the old splash page and directory page into one home page
- Replaced fixed-width, absolutely positioned layouts with flexbox/grid so the site is responsive
- Replaced the button + link pairs with single accessible links
- Added descriptive alt text, labeled the nav, and added a skip link
- Added the about-me page content, social icons, and the project grid with links
- Moved colors and fonts into CSS variables

3. Did you ignore any of the warnings or errors presented by the accessibility checker? If so, why does this not seem like an accessibility concern? If it's useful, you can consolidate your thoughts on multiple warnings/errors if the rationale is similar.

    I fixed every known problem AChecker reported (images used as links needed alt text, and the <i> icon tags were replaced with <span> tags). The remaining "potential problems" are manual-check reminders that appear on every page regardless of the code, so I reviewed them instead of changing code:

        - Image alt text / long description / color / images of text: every image has short alt text describing what it shows or where its link goes. None of my images contain text, and none need a long description.
        - Language and text direction: the whole site is in English, and every page has lang="en", so there are no foreign phrases or right-to-left text.
        - Visual lists, sensory characteristics, link text: navigation and folders are real lists, and every link has visible text or an aria-label, so nothing relies on shape, position, or color alone.
        - Multiple ways / consistent navigation: the nav bar appears in the same order on every page, and the home page also has a directory of folder links, so there is a second way to reach every page. A separate site map isn't needed for a three-page site.
        - Headings and quotations: headings are used for page structure, not styling, and the site has no long quotations.

    The W3C CSS validator also reports warnings that CSS variables (var(--...)) and calc() expressions that use them can't be statically checked. I ignored these because the values are valid and the variables are used on purpose to keep colors, fonts, and sizes in one place.

4. How long, in hours, did it take you to complete this assignment?

    This assingment took me about a total of 6-7 hours to complete.

5. What online resources did you consult when completing this assignment? (list specific URLs, describe queries to Generative AI, or use of AI-based code completion)

    - Google Fonts (Gaegu, DM Sans): https://fonts.google.com
    - Font Awesome icons: https://fontawesome.com
    - W3C HTML validator: https://validator.w3.org
    - W3C CSS validator: https://jigsaw.w3.org/css-validator/
    - AChecker accessibility checker: https://achecker.achecks.ca/checker/

    Generative AI: I used Claude (Anthropic) to help restructure my existing code. After slighly reworking my existing portfolio code, I asked it to review the markup and stylesheet for validity, accessibility, and responsiveness while keeping my original design and most of my oringal code. I also asked to explain new CSS concepts it suggested  (:root, the * selector, article tags, flex-wrap, clamp,
    media queries); to help me debug layout problems (the phone preview, squeezed images, folder stacking, background images); and to help interpret W3C and AChecker errors. I reviewed, edited, andtested the code myself and made the design decisions (layout, colors, fonts, content, and images).

6. What classmates or other individuals did you consult as part of this assignment? What did you discuss?

I worked with 2 other classmates to set up our github repoistories together as a starting point for the assignment.

7. Is there anything special we need to know in order to run your code?

- *Testing the mobile layout:* while testing in Chrome DevTools, I found that I had to maximize the browser window FIRST, and only then open DevTools (Inspect) and change the screen size or device ratio. If the window isn't maximized first, the preview keeps the current viewport size and just
  crops the page to the new ratio, so the layout doesn't resize properly. This is a quirk of the browser's preview, not of the site. For the best results, maximize the window, open Inspect, turn on the device toolbar, then pick a device or drag the width.
- The site loads Google Fonts and Font Awesome from the internet, so you need a connection to see the custom fonts and icons. Without it the site still works and uses fallback fonts.
- All images are in the img/ folder and use relative paths.
- Links on the projects page go to my live projects, so they open external sites.

