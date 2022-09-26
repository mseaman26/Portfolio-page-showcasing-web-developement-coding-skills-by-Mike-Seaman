# Portfolio-page-showcasing-web-developement-coding-skills-by-Mike-Seaman
This is a website that serves as a portfolio for all of Mike Seaman's current and future coding projects.  It's destined to grow! At this time, the main page showcases four projects, two of which are finished and two of which are not.  The two completed projects are 1) a webpage code refactoring project and 2) a CSS cheatsheet that was created in collaboration with my classmate William Crane.  The two incomplete projects are 1) a baseball graph project and 2) a surfing highlight reel project. There is also a brief "About Me" section so the user can feel like they've gotten to know me a little bit. When the user clicks on any of the links, they are taken to another page.  Some of those pages are rendered from HTML files that are within the project itself.  The baseball project, for example, loads a new html file and there are 6 links in that page, each leading to yet another html file.  For the baseball project, I decided to use a separate CSS file called "baseball.css."  I wasn't sure if this is common practice, but I wanted to try to separate the styling.  

## Link to the Webpage
https://mseaman26.github.io/Portfolio-page-showcasing-web-developement-coding-skills-by-Mike-Seaman/

## Languages Used
This project primarily involved the HTML and CSS languages. However I also used command line, git, and github for storing the project in a repository and github pages for deployment

## Key Features
- Flexbox functionality, including wrap, align-items, justify-content, grow/shrink, and more
- pseudo-classes, such as :hover
- media queries, to make the pages render nicely on different sized screens
- variables, for reuse of colors

## Notable Methods
- One key method I used with the HTML, was making up names for HTML elements and treating them as if they were classes.  For example, I have an element called \<project\>, and another one called \<division\>.  I learned that this could be done from a partner in class.  I'm not sure if this is common practice, or best practice, but it did ultimately get results that I intended. I'm starting to think that it's better practice to use the built-in semantic elements when possible and \<div\> elements when it's not possible. Below is an example.  Notice the tags called \<featured-box\>, \<horiseon-git\>, and \<about-me-section\>

```html
 <!-- The “main” section included a “featured project” and an “About Me” section.  Using semantic tags to make it easier for me to differentiate items -->
    <main>
        <featured-box>
            <a href="https://mseaman26.github.io/Mikes-wonderful-refactoring-of-the-Horiseon-Webpage/" target="_blank" >
                <h2>Here is my most recent solo project.  I refactored some code for a website called Heriseon.  The code is in deployed on Github Pages! Click anywhere in this box to visit!</h2>
                <img id="heriseon" src="./assets/Images/Heriseon homepage.png" alt="thumbnail of the Horiseon website">
            </a>
            <horiseon-git>
                <a href="https://github.com/mseaman26/Mikes-wonderful-refactoring-of-the-Horiseon-Webpage" target="_blank" id="feature-git">
                Feel free to visit the Github repository for this projecty by clicking here!</a>
            </horiseon-git>
        </featured-box>
        <about-me-section>
            <img id="hike" src="./assets/Images/Mike_on_hike.JPG" alt="Mike on a hike">
            <p>About me: I am a student attending the UC Berkeley full-stack web development bootcamp.  I have had an interest in coding for some time, but have never taken serious action to learn the skill…until NOW!  I enjoy surfing, hiking, baseball, and classical piano.  
            </p>
        </about-me-section>
```



- I used a reset.css file.  I simply took one from one of our activities, figuring this was good practice

- I split up the css styling into two separate files.  This is another method that left me uncertain as to weather or not I was using best practice, but again, it got the results I needed

- I don't like when flex wrap creates a new row one element at a time.  The grid layout gets lost when this happens. To avoid this, in certain sections, I assigned the width of these elements to a percentage of the screen width.  I would then use  media queries to change that percentage (make it larger) when the screen got smaller.  I imagine I'll learn a better way to do this as I further my knowledge. Below is a snippet shoeing those media queries

```css
@media screen and (max-width: 992px) {
    project{
        width: 45%;
    }
}
@media screen and (max-width: 768px) {
    /* using tow methods to do esentially the same thing.  I suppose this is an example of me trying out different ways of doing things to hopefully settle on the right one */
    main{
        flex-direction: column;
        align-items: center;
    }
    project{
        width: 90%;
    }
}
```

- I used multiple .html files, as mentioned above.  I was just experimenting and it seemed to work fine, so I went with it.


