# Sprint Challenge: Advanced CSS - Space Walkers Web Page

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a concrete project. This Sprint explored advanced CSS techniques using Responsive Design and Preprocessing. During this Sprint, you studied how to use the viewport meta tag, media queries, setting up a preprocessor, and advanced use of preprocessing techniques. In your challenge this week, you will demonstrate proficiency by updating a website that is missing content as well as adding mobile styling.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your PM and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in advanced css and your command of the concepts and techniques in responsive web design and preprocessing.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your project manager.

## Description

The client for this challenge is _Spacewalkers Magazine_. Spacewalkers needs your help to build a small proof of concept website for their marketing team. They have provided designs for both desktop and phone views. In addition to designs and content they have most of the home page coded for you. You just need to finish the navigation and header as well as the mobile styles.

In meeting the minimum viable product (MVP) specifications listed below, your web page should look like the solution design files of the desktop and mobile views:

[Click here to review the home design](design-files/home-desktop.png)

[Click here to review the mobile design](design-files/home-mobile.png)

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your project manager

1. What is the difference between an adaptive website and a fully responsive website?

Adaptive layout adjusts to user's screen size to an extent. However, this is basically several different fixed webpages, and the size of the screen determines which fixed view the user sees. With a fully responsive website, there is a combination of fluid and adaptive design. This usually involves several break points for different screen sizes as well as percentage-based sizing so that the content will look best at many different screen sizes. Another big difference in the two is the time it takes the designer to create each type - adaptive usually takes the developer less time while fully responsive takes more time. In the end, the developer's extra time spent to create a fully responsive website is converted into a much better user experience for a large number of users.

2. Describe what it means to be mobile first vs desktop first.

Mobile first design means that the developer first creates a page that looks best on a mobile screen. After that, break points and responsive tools are used to make the page look better on larger and larger screens. Desktop first design goes in the opposite direction - the desktop page is designed first, and then breakpoints and design changes make the page adapt to smaller screen sizes.

3. What does `font-size: 62.5%` in the `html` tag do for us when using `rem` units?

This is primarily an accessibility fix. Setting font size to 62.5% makes the default 10px, so when em and rem units are used later in the design they will scale up from there. For users that set their font size to be larger or smaller (for varying eyesights), having the font size set to 62.5% and using ems/rems will cause their text to adjust to their personalized settings. This differs from using pixels throughout the code - using pixels would keep the users font size adjustments from having any effect on a page's display - pixels belong in fixed websites, and we don't like fixed websites.

4. How would you describe preprocessing to someone new to CSS?

Preprocessing is an amazing way to make CSS easier in so many ways! First, the way elements are nested makes it so much easier to read the design files. Second, you can split up your CSS into multiple files so you don't have to scroll through hundreds of lines of code to find what you want to change. For example, you can have all of your navigation design inside one file, while all your image design is in another file, etc. The third big advantage of preprocessing is that the compiler automatically error checks your code each time you change. It will let you know if you leave out some important syntax! This saves a ton of time scrolling through code trying to find where you left out that semicolon. Highly recommend you learn how to use a preprocessor!!

5. What is your favorite concept in preprocessing? What is the concept that gives you the most trouble?

Easy! My favorite preprocessing concept is having multiple design files that get imported into the index.less file. It took some getting used to, but it clicked when I discovered how easy it was to pop over to the right design file and go straight to the line of code that I needed to change. I struggled the most with escaping. It wasn't even that the way it works confused me - I actually got that immediately. For some reason, the word 'escaping' itself confused me. Like, why is it called that? What does it mean? I looked for more information online about it and paid extra attention in class to make sure I was at a comfortable level of understanding.

You are expected to be able to answer all these questions. Your responses contribute to your Sprint Challenge grade. Skipping this section *will* prevent you from passing this challenge.

## Project Set Up

Follow these steps to set up your project:

### Git Set up

- [ ] Create a forked copy of this project.
- [ ] Add your project manager as collaborator on Github.
- [ ] Clone your OWN version of the repository (Not Lambda's by mistake!).
- [ ] Create a new branch: git checkout -b `<firstName-lastName>`.
- [ ] Implement the project on your newly created `<firstName-lastName>` branch, committing changes regularly.
- [ ] Push commits: git push origin `<firstName-lastName>`.
 
Follow these steps for completing your project.

- [ ] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo). **Please don't merge your own pull request**
- [ ] Add your project manager as a reviewer on the pull-request
- [ ] Your project manager will count the project as complete by merging the branch back into master.
 

### Preprocessor Set up

* [ ] Verify that you have LESS installed correctly by running `lessc -v` in your terminal, if you don't get a version message back, reach out to your project manager for help.
* [ ] Open your terminal and navigate to your preprocessing project by using the `cd` command
* [ ] Once in your project's root folder, run the following command `less-watch-compiler less css index.less`
* [ ] Verify your compiler is working correctly by changing the `background-color` on the `html` selector to `red` in your `index.less` file.
* [ ] Once you see the red screen, you can delete that style and you're ready to start on the next task

## Minimum Viable Product

Your finished project must include all of the following requirements:

### Import LESS Files

* [ ] Navigate to your `index.less` file. Notice the file is blank. You have been asked to use a certain import order. That order is as follows:

```markdown
1.variables.less
2.mixins.less
3.reset.less
4.global.less
5.navigation.less
6.footer.less
7.home-page.less
```

_You will know everything is working properly when you see the styles enabled for the provided content._  

### Home Page - Desktop HTML & LESS

* [ ] Take 10 minutes to review the code that has already been provided for you. Take time to see how the home page was built.

* [ ] Add a viewport meta tag to the head of your index.html page

* [ ] [Review the provided home desktop design file](design-files/home-desktop.png). You are to build the missing navigation system and header image. You have been provided all content necessary in the [index.html file](index.html)

* [ ] Navigation Styles: Use the `navigation.less` file for styling.

* [ ] Main Content Styles: Use the `home-page.less` file for styling

* [ ] LESS Mixins: Create and use 2 different mixins to aid your styling. Use the `mixins.less` file for your mixins

* [ ] LESS Parametric Mixin: create a parametric mixin that is used to create the `sign up` button styles.

* [ ]  Use at least 2 parameters to create your button

* [ ] Create a hover state that swaps the background color and font color of the base button styles.

### Mobile Design

* [ ] Create a `@phone` variable that contains a `max-width: 500px` media query string. Use the `@phone` variable for all your nested mobile styling.

* [ ] [Review the provided home mobile design file](design-files/home-mobile.png). Match your mobile styling the best you can using the design file.

* [ ] Push your changes and create a pull request if you haven't already.

In your solution, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

After finishing your required elements, you can push your work further. These goals may or may not be things you have learned in this module but they build on the material you just studied. Time allowing, stretch your limits and see if you can deliver on the following optional goals:

* [ ] Build a page of your choosing from the navigation items. Come up with content and images that fit the theme.

* [ ] Introduce CSS animations to your site.

* [ ] Create a fixed navigation and add some opacity to the background

* [ ] Create a form that would allow someone to sign up for a Spacewalkers Magazine subscription