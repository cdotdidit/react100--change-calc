Instructions: Change Calculator


Introduction
In this project, we're going to build Change Calculator in React and:

Understand the folder structure
Convert visual wireframe to JSX markup
Setup state management
Setup event binding for the button elements
Port calculation logic from jQuery
Update view state based on calculation results
Step 1 - Understand the folder structure
Open a terminal
Clone your starter files from Github and open the project in VS code.
Run: npm install to install all the dependencies.
Step 2 - Convert visual wireframe to JSX markup
For this project, we must first tackle the visual aspect of the application. To start, add a <link> element in the <head> section to include Bootstrap styling in your project.

Once you have included Bootstrap's CSS styling, add the following elements to the page, ensuring the user interface matches the screenshot at the top of this document.

- Header
- Tagline
- Bootstrap Row
  - Bootstrap Column (4 columns wide)
    - Bootstrap Panel
      - How much is due?
      - How much was received?
      - Calculate button
  - Bootstrap Column (8 columns wide)
    - Outcome alerts.
      - Success: Total change due.
      - Danger: Additional money owed.
    - Grid for denominations
      - Twenties
      - Tens
      - Fives
      - Ones
      - Quarters
      - Dimes
      - Nickels
      - Pennies
Step 3 - Setup state management
Next, we will need to change our input elements such that:

The value of the input elements are bound to a value in the component's state.
When a user changes the input element, it changes the value in the component's state.


For a refresher on how this is accomplished, rewatch this section of the React course, from 7 minutes in to the end of the video.

Step 4 - Setup event binding for button elements
After you have completed the above step, the next piece of the puzzle is to connect the click event of your button to a calculate function you will need to add to your component class. This is similar to passing an event listener to $('button').click() in jQuery.

Step 5 - Port calculation logic from jQuery
Once your button has been set up to call your component function whenever the click event is fired, you should take your calculation logic that you wrote in jQuery and port it to this application.

Your function should calculate the value for the following 11 variables.

amountDue - Amount due as entered by user
amountReceived - Amount received as entered by user.
changeDue - Subtract amount due from amount received.
twenties - # of $20 bills.
tens - # of $10 bills.
fives - # of $5 bills.
ones - # of $1 bills.
quarters - # of 25c coins.
dimes - # of 10c coins.
nickels - # of 5c coins.
pennies - # of 1c coins.
Step 6 - Update view state based on calculation results
Once you have calculated the above 11 variables, you need to call this.setState to update the state with the values calculated by your function.

For a refresher on this.setState, you should check out the React documentation on the setState function.

Step 7 - Show state values in the DOM
Now that you have the calculated counts for each denomation contained in the state of the component, the final step is to print the number of denomations to the correct area of the application. For example, the markup for showing the number of twenties to dispense would look something like this:

<div className='well'>
  <h1>Twenties</h1>
  <p className="change">{this.state.twenties}</p>
</div>
Hint: Make sure you add the className change as seen in the example above. Otherwise, your tests will not pass!

Bonus
Find and include images of each denomination, changing styling as necessary.
Modify the app so that it calculates change in another currency such as Euros or Mexican Peso. Additionally, you could also try to allow users to switch between USD and another currency.
Project Submission
Make sure you commit your work and push it up to github. To submit this project, please deploy this website using Now.

# navigate to the project
$ cd ~/projects/{project-name}

# run "now" to deploy the site
$ now
After running that command, you should see the following output:

> Deploying ~/oca/{project-name} under your@email.com
> Ready! https://{project-name}-skckceswsd.now.sh (copied to clipboard)
Submit your Now URL using the link at the bottom to navigate to the submission page, and do it again once more for your github repository URL on the following page. Once you submit both URLs for the project, you can move onto the next assignment. An instructor will evaluate your work at a later time, giving feedback if necessary