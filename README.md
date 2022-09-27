# Portfolio-page-showcasing-web-developement-coding-skills-by-Mike-Seaman
This is a website that serves as a portfolio for all of Mike Seaman's current and future coding projects.  It's destined to grow! At this time, the main page showcases four projects, two of which are finished and two of which are not.  The two completed projects are 1) a webpage code refactoring project and 2) a CSS cheatsheet that was created in collaboration with my classmate William Crane.  The two incomplete projects are 1) a baseball graph project and 2) a surfing highlight reel project. There is also a brief "About Me" section so the user can feel like they've gotten to know me a little bit. When the user clicks on any of the links, they are taken to another page.  Some of those pages are rendered from HTML files that are within the project itself.  The baseball project, for example, loads a new html file and there are 6 links in that page, each leading to yet another html file.  For the baseball project, I decided to use a separate CSS file called "baseball.css."  I wasn't sure if this is common practice, but I wanted to try to separate the styling.  

## Overview of the Webpage:
<img src="./assets/images/portfolio screenshot.png" alt="Alt text" title="Optional title" style="max-width: 300px">

## Link to the Webpage
https://mseaman26.github.io/Portfolio-page-showcasing-web-developement-coding-skills-by-Mike-Seaman/

## Languages Used
This project primarily involved the HTML and CSS languages. However I also used command line, git, and github for storing the project in a repository and github pages for deployment

## Notable Features
- Flexbox functionality, including wrap, align-items, justify-content, grow/shrink, and more
- pseudo-classes, such as :hover
- the ::after pseudo class
- media queries, to make the pages render nicely on different sized screens
- variables, for reuse of colors

## Notable Methods
- I had originally experimented with using a lot of custom HTML tags, but learned that this is not best practice, so I refactored my code to use proper semantic HTML elements.  Below is an example of the code before:


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
and here is the code after:


```html
<main>
    <!-- The featured project is contained within a box that features a clickable image that links to the deployed project as well as a clickable box that links to the githup repo -->
        <section id="featured-box">
            <a href="https://mseaman26.github.io/Mikes-wonderful-refactoring-of-the-Horiseon-Webpage/" target="_blank" >
                <h2>Here is my most recent solo project.  I refactored some code for a website called Heriseon.  The code in deployed on Github Pages! Click anywhere in this box to visit!</h2>
                <img id="heriseon" src="./assets/Images/Heriseon homepage.png" alt="A thumbnail image of the Horiseon website">
            </a>
            
                <a href="https://github.com/mseaman26/Mikes-wonderful-refactoring-of-the-Horiseon-Webpage" target="_blank" id="feature-git">
                Feel free to visit the Github repository for this project by clicking here!</a>
            
        </section>
        <section id="about-me-section">
            <h2>About Mike Seaman:</h2>
            <img id="hike" src="./assets/Images/Mike_on_hike.JPG" alt="Mike on a hike">
            <p>I am a student attending the UC Berkeley full-stack web development bootcamp.  I have had an interest in coding for some time, but have never taken serious action to learn the skill…until NOW!  I enjoy surfing, hiking, baseball, and classical piano. I'm eager to learn more and practice more so that I can make great projects with ease!  

            </p>
        </section>
    </main>
```


- I used a reset.css file.  I simply took one from one of our activities, figuring this was good practice

- I split up the css styling into two separate files.  This is another method that left me uncertain as to weather or not I was using best practice, but again, it got the results I intended

- I assigned the width of some elements to a percentage of the screen width.  I would then use  media queries to change that percentage (make it larger) when the screen got smaller. Below is a snippet showing and example of those media queries

```css
@media screen and (max-width: 992px) {
    .project{
        width: 40%;
    }
}

@media screen and (max-width: 768px) {
   /* For elements that weren’t assigned width using a percentage, I used this method to make them fit nicely on a phone screen */
    main{
        flex-direction: column;
        align-items: center;
    }
    .project{
        width: 90%;
    }
}
```

- I used multiple .html files, as mentioned above.  I was just experimenting and it seemed to work fine, so I went with it.

## Things I've learned during this project (or maybe already knew, but relearned):
- CSS is hard, and possibly not my strong suit
- Visual design and aesthetics in general are also not my strong suits
- Organization of code is crucial and must be practiced from the beginning of any project
- I still enjoy learning code!
<br>
<br>
## -By Michael Seaman

## Author Links
[LinkedIn](https://www.linkedin.com/in/michael-seaman-120a59250/)
[GitHub](https://github.com/mseaman26)


