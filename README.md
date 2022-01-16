# cypress-workshop-Epitech


## Installing

[![npm version](https://badge.fury.io/js/cypress.svg)](https://badge.fury.io/js/cypress)

Install Cypress for Mac, Linux, or Windows, then [get started](https://docs.cypress.io/guides/getting-started/installing-cypress.html).

```bash
cd /your/project/path
```
then

```bash
npm install cypress --save-dev
```
or
```bash
yarn add cypress --dev
```
Make sure that you have already run npm init or have a node_modules folder or package.json file in the root of your project to ensure cypress is installed in the correct directory.

## Discover Cypress
Open cypress with the following command inside your project file :

```bash
node_modules/.bin/cypress open
```

then, if it's your first time, you must see the message :

```bash
➜  cypress-workshop-Epitech git:(main) ✗ node_modules/.bin/cypress open
It looks like this is your first time using Cypress: 9.2.1

✔  Verified Cypress! /Users/your-name/Library/Caches/Cypress/9.2.1/Cypress.app

Opening Cypress...
```

Now, check some sample test files that demonstrate key Cypress concepts to help you get started.

## Writing Your First Test

### Add a test file

Assuming you've successfully installed the Test Runner and opened the Cypress app, now it's time to write our first test. We're going to:

- Create a sample_spec.js file.
- Watch Cypress update our list of specs.
- Launch the Cypress Test Runner.

Let's create a new file in the cypress/integration folder that was created for us:

```bash
touch {your_project}/cypress/integration/sample_spec.js
```
Once we've created that file, we should see the Cypress Test Runner immediately display it in the list of Integration Tests. Cypress monitors your spec files for any changes and automatically displays any changes.

Even though we haven't written any tests yet - that's okay - let's click on sample_spec.js and watch Cypress launch your browser.


### Step 1 - Visit a page

```javascript
describe('My First Test', () => {
  it('Visits the Kitchen Sink', () => {
    cy.visit('https://your-web-site.com')
  })
})
```
### Step 2 - Query for an element

```javascript
describe('My First Test', () => {
  it('Visits the Kitchen Sink', () => {
    cy.visit('https://your-web-site.com')
    
    cy.contains('type')
  })
})
```
### Step 3 - Click an element

```javascript
describe('My First Test', () => {
  it('Visits the Kitchen Sink', () => {
    cy.visit('https://your-web-site.com')
    
    cy.contains('type').click()
  })
})
```
### Step 4 - Make an assertion

```javascript
describe('My First Test', () => {
  it('Visits the Kitchen Sink', () => {
    cy.visit('https://your-web-site.com')
    
    cy.contains('type').click()

    // Should be on a new URL which includes '/commands/actions'
    cy.url().should('include', '/commands/actions')

    // Get an input, type into it and verify that the value has been updated
    cy.get('.action-email')
      .type('fake@email.com')
      .should('have.value', 'fake@email.com')
  })
})
```



### Special commands
In addition to having a helpful UI, there are also special commands dedicated to the task of debugging.

For instance there is:

- cy.pause()
- cy.debug()



-----------
Youssra El-Ajli : youssra.el-ajli@epitech.eu  
Hugo Suzanne    : hugo.suzanne@epitech.eu  