# Random Project
---
#### Cloning, Installing, and Running
1. Clone The Repo
2. Then cd into the folder: `cd random-project/`
3. Install NPM Packages: `npm install`
4. To Run the Server: `npm run dev` 
   1. This will build and spin a local instance on `http://localhost:3000`
  
- *Note*: You must have NPM installed to do this, the process may look different if you are on windows. But for mac and linux the process above is how you build it in dev
- NPM: https://www.npmjs.com/get-npm

#### Basic Project
Just putting together a super barebones repo that you can fork and play around with. Below I will describe a basic problem to try and solve with it, I will try to base it around what we are doing in the class.

###### Problem
So, for a basic good start here's what you need to try to make:
- Create a button that once clicked opens a modal (popup), this modal should include:
  - A form for a user to create a new account for some random website, try to include a couple different input types such as username, email, password, birthday, etc. 
  - It needs a submit and cancel button
    - The cancel button should close the form and reset all the values, so that if the form is reopened it is a blank form
    - The submit button doesn't really have to do anything
  - Important things to focus on:
    - Try to get the content inside the form to support window resizing (hint: look at `v-row` and `v-col` on the vuetify website)
    - Make the form not close when someone clicks off the actual popup
    - Learning how component files are formatted and how they are imported and included in the `pages`
    - Learn the structure of Vue, for a basic reference it goes `layouts -> pages -> components`

*If you run into any trouble or have questions feel free to ask in slack, im out of town but i'll have my phone on me! Also feel free to do whatever you want, the thing above is just an idea of something to create, but you can of course make anything.*
