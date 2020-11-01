# CB Angular Test

### 1. Getting started

This repository is a simple Angular CLI generated project. Contains no styles and no pre-defined logic. It is based on Angular 9.x version, if you already have it pre-installed fork the repo and jump to Section 2.

If you are not conformable with Angular 9.0 and/or you are having other versions pre-installed, you can use your prefered version as long as it's minimum Angular 7.

### 2. Fake API server setup
To be able to work on the test project you will need to run a local server. I've already added to package.json the required dependency, but if you want to install it globally: `npm install -g json-server`

To start the fake API server, you have to run: `json-server --watch db.json` and will generate the following endpoints:
a. settings
b. menu
c. pools/:id

More details about how to use the fake API server, here: https://github.com/typicode/json-server

### 3. Coding Test

You have *4 hours* to complete the test. 

Based on the data within the `menu` endpoint. You will need to generate functional views: a single pool coupon and an official pool view. For UI/UX inspiration you can have a look at our product website. Anything extra would be a bonus.
*You can find more details about what is a betting pool on Google or our blog.*

##### 3.1 Requirements for basic test
- have the views required to 'play the game' or 'check my results'
- being able to make selections, choose stake and post required data for placing my ticket (POST `tickets` endpoint)
- being able to view a pool results

##### 3.2 What we want to see except the above
- usage of Angular architecture
- usage of NgRx / Akita
- code understanding and logic
- testing; minimum 50% coverage
- UI/UX - we value a good clean design. You can use any CSS framework you want (Bootstrap, Tailwind, etc). 
 
Although we don't recommend the usage of UI Components libraries like Angular Material, if this will lead you to completion of the project in time, feel free.

#### 4. Submit test

If you haven't managed to finish the test within the required time, tell the recruiter you took an extra hour. Last commit (although would prefer multiple ones) should be at 4 hours +/- 5min. 

If you still haven't finished at least the requirements for the basic test, don't even stress yourself to send the test.
