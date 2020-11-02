# CB Angular Test

Greetings, candidate. Welcome to Colossusbets challenge! Please read carefully the README before starting the test.

If you run into any issues please contact aurel.tirnovanu@colossusbets.com.

Good luck!

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

You have ***4 hours*** to complete the test.

Based on the data within the `menu` endpoint, you will need to generate functional views (not css only) for the following: a single **pool coupon view** and an **official pool view**. For UI/UX inspiration you can have a look at our product website. Anything extra would be a bonus. *You can find more details about what is a betting pool on Google or our blog.*

##### 3.1 Requirements for basic test
* have the view required to 'play the game' (aka pool coupon view)
* being able to view a pool results (aka official pool view)
* being able to make selections, choose stake and post required data for placing my ticket (`POST tickets` endpoint). The endpoint should contain
    * cost
    * pool id
    * customer's selection (more details in section 5)

##### 3.2 What we want to see in addition to the above
- usage of Angular architecture
- usage of NgRx / Akita
- code understanding and logic
- testing; minimum 50% coverage
- UI/UX - we value a good clean design. You can use any SASS/SCSS/LESS/CSS framework you want (Eg: Tailwind, Bootstrap). 
 
Although we don't recommend the usage of UI Components libraries like Angular Material, if this will lead you to completion of the project in time, feel free.

#### 4. Submit test

If you haven't managed to finish the test within the required time, tell the recruiter you took an extra hour. Last commit (although would prefer multiple ones) should be at 4 hours +/- 5min. 

We are looking forward to evaluate your test as long as the basic requirements are implemented.

#### 5. Additional notes

- selections are build as in per match/game/leg;
- a pool is considered 'OFFICIAL' if status is official; and OPEN if status is 'OPEN'. A user can bet only in a 'OPEN' pool;
- for ticket placement (POST to `tickets` endpoint) - the selections are build based on the following: 
  `"leg[leg_index].selection[selection_index].bin[,leg[leg_index].selection[selection_index].bin] / leg[leg_index].selection[selection_index].bin"`
