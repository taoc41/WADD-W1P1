# Week 1 Practical 1 - Web development workflow and tools

This practical is all about getting familiar with the web development workflow and tools that are available for you to use in your development and testing. The practical also highlights the differences between poor HTML and quality HTML.
The work for this practical has been broken down into 4 stages.
## Stage 1 Exercises: Getting Online
### Exercise 1.1: Setting Up Git Pages
If you haven’t already done so, you will need to follow [this tutorial](https://github.com/IM-WADD/GitPages-Tutorial) to learn how to set up Git Pages for your repositories. 

### Exercise 1.2: Familiarisation with CatCatMoose
In this repository, there is a folder called CatCatMoose, which contains a very simple website that you will use in a few exercises in the coming weeks. The website has the following structure.
- index.html
- catCatMoose.html
  - resources
  - styles
    - styles.css
  - scripts
    - script.js
    
Don’t open these files in your IDE just yet. We’ll do that in Stage 3.
Create a copy of this template repository in your own GitHub if you haven't already done so. Enable GitPages on that respository. Go the following URL on your desktop (but replace YOURUSERNAME with your Git username and Practical1 with the name you gave the repository): 
- https://yourusername.github.io/Practical1/CatCatMoose

Open the same webpage on a mobile device. I recommend bookmarking the URL above on both your personal computer and mobile device.

You do not always need to put your websites on the Internet, as you’ll often want to test sites when run locally from your computer before putting them online.

Open the same webpage locally, by double clicking on the index.html page which will probably open it in Chrome (if Chrome is your default browser). If not, right click on the file, and open it with Chrome.

Look at the file URL in Chrome, you should see that it begins file:// on a Mac or C:// on a Windows machine (if it’s stored on your C: drive) rather than http://. That’s how you know you are working on a local copy of the file.

## Stage 2 Exercises: Using Visual Studio Code
These exercises are designed to help you become familiar with using the Visual Studio Code IDE for web development while improving your HTML skills.

### Exercise 2.1: Setup
You may later choose to use a different IDE (e.g. if you have one that you are already familiar with) but for now, please give VS Code a trial even if you use something different.
First, you will install a few VS Code extensions that will make developing websites a little easier.
1. Open VS Code then click the Extensions button![Extensions button on VS Code](https://github.com/IM-WADD/Week1Practical1/assets/5978932/1899e4ec-a3f4-4ff2-b47c-f52b38f92979)
2. Search for and install **HTMLHint.** Make sure the extension you install also has HTMLHint as the author name. This extension performs basic validation, like checking that open HTML tags are properly closed.
3. Search for and install **W3C Web Validator** by Celian Riboulet. This extension performs deeper validation to check that your HTML is compliant with W3C standards.
4. Search for and install **Live Preview** by Microsoft, which runs a local server to allow you to preview live changes to your website much more easily. This might not mean much to you yet, but it will be useful in the coming weeks!

### Exercise 2.2: Using VS Code
Open the CatCatMoose project in VS Code. You can open files individually by double clicking on a specific file to open it in the IDE. Exactly how this works will depend on your operating system. However, it is strongly recommended that you open all your web projects as folders:
1. If VS Code is not already running, start it by double clicking the application icon.
2. In VS Code, go to File > Open Folder, then select the folder containing your website. For example, to open CatCatMoose, select the CatCatMoose folder rather than the individual files it contains. This approach will show the complete folder structure in the Explorer pane in VS Code, allowing you to easily switch between files and create new files in the folder.

**Open index.html by clicking on it in the VS Code Explorer pane. Then, use the Live Preview extension to spin up a server and open the webpage in your default browser.** To use the Live Preview extension, click icon that looks like a book with a magnifying glass that should be at the top right of the VS Code window: ![Live preview button on VS Code](https://github.com/IM-WADD/Week1Practical1/assets/5978932/1aa242e1-a785-4e93-9d50-166ff6dfd9e7)

If you would like to open the file in a different browser, you can copy paste the URL into the browser of your choosing. Notice that the URL no longer starts with file:// or C://. Instead, it will show an IP address or the word “localhost”. This lets you know that the file is running on a server, similar to a hosted webpage but only accessible on your computer. The nice thing about Live Preview is that it will immediately show in your browser any changes you make to the code of your website. If you don’t use Live Preview, you will have to manually refresh your browser every time you make a change. To test the extension, edit line 7 of index.html to change the page heading:
```
<h1>Cat Cat Moose Home Page!!!</h1>
```
Save your changes then check the live preview of the webpage to see the update.

### Exercise 2.3: Validating HTML
In the previous exercise, you should have seen that the webpages open and render in the browser completely fine and without issues.

However, the HTML code in both the index.html and catCatMoose.html files are both invalid with many examples of bad practice. The browser’s job is to do its best to render HTML files, even if they fail to meet W3C standards. In this module, you will be marked on the quality of your code, not just how your webpages appear, so it’s important to get in the habit of validating your HTML.

There are three main ways to validate your HTML in VS Code:
1. The **HTMLHint** extension automatically provides some basic “linting” capabilities. You may have already noticed a couple of yellow underlines in index.html. These are warnings from the extension that you have issues in your code. Mouse over a yellow line to see more about a particular issue or go to View > Problems to see all problems at once. The HTMLHint extension doesn’t go far enough, however. If you look at the code for catCatMoose.html, you will not see any yellow warning lines even though the code has a lot of issues.
2. The **W3C Web Validator** extension provides more validation but, unlike HTMLHint, it has to be manually run each time you want to check your code. To run the validator, look for the W3C validation button at the very bottom of the VS Code window:
![W3C Validation button](https://github.com/IM-WADD/Week1Practical1/assets/5978932/cf037a15-4d10-4da3-8e10-38cadce2a8c9) When you click the button, you should briefly see a spinner, then it will either open the Problems pane and show you the issues it has found, or it will pop up a message saying that the HTML is valid. If the spinner doesn’t stop after a while, the validator has crashed. This occasionally happens if the extension encounters an error it can’t handle. You may find this with index.html in the CatCatMoose project. When this happens, try the next validation option—the online service.
3. The official **W3C Nu HTML Checker**, [https://validator.w3.org/nu/](https://validator.w3.org/nu/) is by far the most reliable option, and you should use make sure you use this service before submitting your assessments. However, using it does require a little extra work on your part. To check a file, open the link, then select “text input” from the “check by…” dropdown menu. Copy-paste your HTML into the text box then click the ”check” button.

See if you can fix the many validation problems in both HTML files. We haven’t started learning HTML yet so don’t worry if you get stuck, the answers will be revealed in lecture.

## Stage 3 Exercises: Familiarisation with Chrome’s Developer Tools
The exercises in this stage are designed to introduce you to some of the developer tools included in the Chrome Browser. There are many features in this tool, that provide lots of functionality, we’ll introduce them gradually through the module as and when we need them. First up, a few tools to allow you to view the DOM and see your site on different devices.

### Exercise 3.1: Viewing and Analysing the DOM
Open your corrected CatCatMoose index page in Chrome and open the Chrome developer tools by right clicking in the window and selecting ‘inspect’ from the menu.

Click on the Elements tab in the menu in the developer tools to see the Document Object Model (DOM) for this page. Expand the elements to see the nested structure.

### Exercise 3.2: The Device Simulator
In the developer tools menu, just to the left of the Elements tab, you should see a tiny icon that looks like a phone and a tablet. Click on this icon to open the Device Simulator. 

The Device Simulator is a very handy tool that allows you to see what a page looks like on different screen sizes right from your browser. Experiment with changing the device to different tablets and smartphones. The CatCatMoose webpage is not be responsive and therefore may appear weirdly when viewed on different size screens. We will work on making responsive websites later in the module!

Use the “Edit…” option at the bottom of the dimensions list to add tablet dimensions (1280 X 800 px, landscape and portrait) and laptop dimensions (1920 x 1080 px) to your list of devices. You might want to name them something like WADD laptop and WADD tablet portrait, and WADD tablet landscape. 

Note that you can use the ![Rotate device button](https://github.com/IM-WADD/Week1Practical1/assets/5978932/60321b2f-66bd-4edb-a1d4-ba7881e99934)icon to rotate the device and preview what your website would look like on these devices when in portrait or landscape mode. 

## Stage 4 Exercises: Familiarisation with MDN and W3Schools
There are A LOT of resources on HTML available online. Some resources are better than others. I recommend using [MDN (Mozilla Developer Network)](https://developer.mozilla.org/en-US/) for in-depth documentation and W3Schools for quick reference. Both sites provide tutorials as well as documentation.

Open both MDN and W3Schools in separate tabs. In MDN, go to References > HTML, then find the HTML Reference section and click “HTML elements”. Finally, locate the <p> element to get more information. Find the reference for the same element on W3Schools by going to References > HTML tag reference.

Compare the information on each site. It is likely you will prefer one site over the other. I tend to find W3Schools a bit more accessible but, be warned, it is occasionally incomplete or not up to current standards. MDN is more reliable but also more complex.

Both sites also provide tutorials. If you’re brand new to web development, you might find it helpful to go through the MDN [front end web development tutorial](https://developer.mozilla.org/en-US/docs/Learn/Front-end_web_developer) and/or the W3Schools [learn HTML tutorial](https://www.w3schools.com/html/default.asp) as well as attending lectures and practicals.

