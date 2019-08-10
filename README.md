# About Vanilla Js Accordion
Accessible accordion widget with less than 1kb of vanilla JavaScript and 3 lines of CSS. Style as you please!

# Download
git clone https://github.com/carl-evans/Vanilla-Js-Accordion.git

# Usage
Include the .min CSS and JavaScript files from the dist folder and use or refer to the markup in vanilla-js-accordion.html

# Walkthrough
<!-- walkthrough.html is simply a commented walkthrough showing how this accordion aims to be accessible
     all the classes on elements must be used for the accordion to work
     you should always use the .min files in a production environment to improve page load speed
-->

    <!-- Aria-label tells visually impaired users they are using an accordion -->
    <ul aria-label="Accordion Control Group Buttons">

        <!-- Accordion 'sections' are stored in list items so visually impaired users get a count -->
        <li>

            <!-- Buttons are tabbable and accessible to screen readers. The aria labels give further info to screen readers about content and state of the UI -->
            <button aria-controls="accordion-content-1" aria-expanded="false" class="accordion-controls__button"
                title="Show content">Show me some Lorem!</button>
            
            <!-- Aria-hidden makes the content neither visible or comprehensible when set to true
                 We also use an id on the content div which matches the button's aria-controls value-->
            <div aria-hidden="true" id="accordion-content-1" class="accordion-controls__content">
                <!-- You're not just limited to paragraph tags here - use some semantic markup! -->
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                </p>
            </div>

        </li>

        <!-- as you can see, the aria-controls and accordion-controls__content id are unique -->
        <li>
            <button aria-controls="accordion-content-2" aria-expanded="false" class="accordion-controls__button"
                title="Show content">Show me more Lorem!</button>
            <div aria-hidden="true" id="accordion-content-2" class="accordion-controls__content">
                <p>
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                </p>
            </div>
        </li>

    </ul>
