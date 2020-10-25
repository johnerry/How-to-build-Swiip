# Introduction

This is a step-by-step guide on how anyone can build a project like **SWIIP.** Firstly, i would like to start by giving the reason and inspiration behind this project.

**Swiip** was coined from **sweep,** meaning, keeping a place clean.

Coming from a country in Africa with little to non existence of a clean environment in most places, leaving so many of its inhabitant ridden with disease such as hepatitis, diarrhea, skin infections and many more, there was a need to at least reduce this from happening.

Every year, the developed countries come into several African countries with drugs and practical hands but they all miss one thing, alot that has to do with environment are the cause of many of these diseases for which they spend millions treating. Another major issue is clean water, but we should not forget that a clean environment breeds clean water for these society to use. When we stop litering our rivers, roads and more, we get clean water right?

W.H.O estimate about 12 million deaths each year as a result of environmental pollution, underdeveloped countries the most. Lets not forget the impending result of the continous global warming. Its simply a plague we all need to start taking seriously, less an impending consequences.

The worldwide spread of COVID-19 pandemic is also a consequence of numerous impacts on the environment. I also predict this as one of many impending disease that rises due to our environment. So, birth this project for everyone.

It is my hope that people can find a solution to environmental issues to make an impact to thier society, and a joint effort by everyone will go a long way to ensuring that.

# Inspiration

The sole inspiration for this project is a result of the impact of environmental pollution, as well as the hope to create awareness that we can all do something about it together. I hail from Nigeria, and i can tell you its not pretty. The environmental impacts of pollution alone has killed so many in to about a million each year. These less fortunate people who couldn't protect themselves due to their inability are the most affected. Regardless, this project was inspired by a need to make a change and improve the society we all live in, by giving everyone a platform to contribute and make a difference.

# AIM

This project aim to build a connection between its customer and qualified agencies responsible for waste management i.e picking, cleaning, recycle waste, and more.

It also aim to bring us together towards a goal of cleaning our community and making it safe, one place and step at a time through crowd funding. Those who donate can see the progress they made towards this goal, and know the percentage left to realise such goals.

# STEP BY STEP PROCESS ON BUILDING THIS PROJECT

### **Requirements for this project**

**FRONT END**: You need to have a basic understanding of **HTML**, **CSS**, **JAVASCRIPT**, **REACT**, **REDUX** & **AXIOS**.

\*\*BACK END: \*\*The back-end was built with good old **PHP** and **MYSQL**.

This project was all writen and its source code pushed to github repo:  **@github.com/johnerry/swiip**   using vscode.

\*\*OTHERS: \*\*Third party API's, plugins, packages and more used in this project include, PayStack API, Google Map API, Draft.js (for text editing). To see the list of packages used in this project, see the package.json file in the github project directory above. Last but not the least, i made use of some unicode characters, as well as fontawesome icons in this project.

## **HOW I BUILD THE APP**

- First off all, about three months prior to this write up, i had no prior knowledge about react, redux and many more integrations that i used in this app, absolutely nothing. I only knew react to be a javascript library thats all. I planned on using just javascript but decided to google on several ideas till i stumbled upon react and what it does, so i decided to give it a try. Trust me, i never regretted it. Its just amazing how easy it is to pick it up on the job once you have a clear understanding of es6 javascript, so basically, the source code is straight forward and elaborate enough to understand by a beginner.

As a **beginner** in using react as a library. Google, Youtube totorials and stackoverflow was my companion all through the making of this audacious project.

To set the record straight, i already had prior knowledge in html,css,javascript and php before this project, and so i brushed through the react & redux totorial within 2 weeks in relative ease.

**Now lets get to the good stuff.......**

First of all, i made wire frame connection of what i want for the project with good old paper and pen.

I proceeded to having a diagramatic representation of how the project will look like using my drafted wireframes on paper, i also had to check on other websites for ideas and different other mixes for this project.

Then i proceeded to the final diagram of how it will look like as a finished product. Meaning i drew multiple pages and how they are interconnected to each other. It doesn't need to be top notch designer work. Just simple lines, box sketches and sample text etc. And because i wanted a responsive design, i also take account of how it would look like on tablets and phones.

Then, i moved to creating a sample design from my sketches using html and css. One thing i immediately realise is how inconvinient it is using react, due to its realoads and screen blanks when making too many concurrent changes at a time. You will essentially do so when building you design structure.

So, i made an external html and css file to test on my browser the frames and structure i built before copying, pasting and correcting its syntax like classname for example to a proper JSX syntax.

I started by building a dashboard panel. With self hidding links on the left, dependent on:

`@media screen and (max-width: .....px) { ....}`

The dashboard also has an heading containing several permanent links and user image whose border was reduced to 50% for that circular feel.

To prevent the use of javascript in controlling the closing and opening of the panel, i used a checkbox which is invisible but represented by a label image, and a div immediately below it which can then be controlled using CSS Selector class e.g  `~`   like an example below:

`#_button:checked ~ .panel {`

`width: 10em;`

`}`

The dashboard has a container `<div>` below the top nav bar and the right panel that all other routes can be displayed in using a `router switch` which ensures only one single route at a time.

After building my dashboard, login page and register page using my own code, i realised there was a critical bug that needed me to keep overflow hidden in some tags even after assigning a 100% width. Mind you, this was not apparent when building these blocks in my external file. It was only after pasting it to react did i see this bug.

So, i searched online for several admin react template and CoreUI strikes out for me. Since its admin template was strikenly close to what i had already built, so i installed it using:

`npm install @coreui/coreui@ --save`

This template is always updating and at the time of writing these, had release version 3.0.0, different from the version 2.5.8 i used in these project. While the update, they maintain thesame convention all through.

I had gone through **core-ui** doc and source code to see how it works and make my changes. Finally, i deleted some files i did not need and that took care of my overflow bug. Although i did realised later that i could fix my bug using some reactstrap tags, which i use sparsely around this project. ReactStrap means React Bootstrap.

At this point, i already made the design block for several pages that i needed. The register, message, login and dashboard pages was completed. I prefere to complete my design blocks with sample text etc, before adding functional code logics to it. Besides, i haven't started work on the back end yet. Doing the design before the logic also gives you an idea what data you will be needing down the line, and how to structure it.

Only after those three pages did i decide to create a sample json response api to test the project flow. For this:

i have a redux store the state using a middleware and combineReducers() function that keeps each data seperate in one access store.

I then moved to create initial state for these reducers, along with the actions to perform such as:

`FETCH_COMMUNITY_DATA_SUCCESS`

etc, that are then exported to the store which combines them for safe keeping and distribution between components that had the ` { connect } from'react-redux'`

For PHP equivalent of session_, i used browser localstorage, and sessionstorage to storing some no critical data, such as token etc that accompanies axios requests to the server, which verifies it and return a new one. This locally stored non critical data also keeps a user logged in for the duration of their choice. Local, being forever and Session being for a single period till the page closes. It also identify user, routes (private and non private) which ensures no access to several forbidden routes for agents, customers and admins.

`render={(props) => (getAuthEmail() && getAuthUserType() ? (`

`<Component {...props} />`

`)`

The routes are different for each users and so to ensure no mix of routes for customer, agent and admin, birth the function:

`routePicker(user_type, cusRoutes, agtRoutes, admRoutes) {`

`return {`

`'customer': cusRoutes,`

`'agent': agtRoutes,`

`'admin': admRoutes`

`}[user_type];`

`}`

Before actually mapping the return `route` inside `switch` in the container `div`

After building the order page, summary and more, and including their route to the `routeList.js`, i stopped to google on **PayStack**.

Their documentation was relatively straight forward. It was as simple as registering, copy and pasting about 10 lines of javascript code, changing the public key to yours, and you have a payment platform.

After building several more pages, i moved towards building a proper backend. I used **procedural php** and **mysqli** all through, rather than classes for my own relative ease, since they both work thesame way.

Then, i made a framework php file containing several functions that takes care of certain things like, **data sanitizing**, **encryption**, **decyption**, **file upload**, **database queries**, **token verification**, **payment verification** etc.

After creating a **database table**, i went back to the front end, integrating **axios** and **redux** to communicate and store data for these pages. Since these data varies i.e **account data**, **community data** etc and they all needed their seperated stored states, so used a middleware and several dispatch functions to handle different requests to the server.

You will notice that some request returns, snapped up at the `componentDidUpdate` returns token, while some do not. This is because, i limited token changes to critical changes you make while navigating the app. For something as critical as making changes to your **account**, to **order** and more requires this, while getting the list of **communities** do not.

To make locating customers easy, i decided to integrate google maps to this project. That is because it give an accurate location through using ones latitude and logitude, and can also give route, and imagery of certain location to give a discriptive representation to agent, what they should look out for.

For more on google map, read on google map javascript api. They have samples for beter understanding and use cases.

One major **issue** with google map for me was the lack of documentation on its third party **react package** from a **different source** of cause. So, i decided to use their javascript documentation, by dynamically creating the script on demand.

You can use:

`React.createElement`

But for this project i decided to use `document.createElement` instead for no particular reason to worry about. They both do thesame thing.

Navigating through several using `<Link>`  from react-router-dom rather than `<a>` tag, to prevent reload during routing url.

Each community is a JSON **object** inside an array and so are **mapped** through to be displayed to the user.

For the order page, i made use of localStorage to store the state of `orderQty`. **With an increament and decreament button, a payment button that initialise PayStack API and followed by a call back function in PayStack API that sends the information to the server for verification and storage.

For the community list which are limited to changes by the admin, i needed a text editor. Google gave me Draft.js.

One major issue with **draft.js** was converting its object representation to JSX. Of cause they provided a function to convert **draft** to **raw** object and back, but nothing to convert **draft** to **HTML** or **JSX**. Further search got me to install `drafttohtml` dependency. Well, this returns a string **html** code, but JSX doesn't accept string **html** code.

I found out i could use **dangeriouslyInsertHtml** but the name was scary enough for me to find another solution. Finally, i built my own function that maps through each tags *nodes*, style and props and returns a JSX valid syntax.

For sending request to the server, i made use of `formData()`  in browsers, that let's your send request like in a normal form in html.

I also noticed that data could change once it gets to the server, even while using **POST** request, it is an invisible sent url data afterall just like **GET**. Things like `"+"` are represented as `" "`, and so the need to `uriEncode` each data sent to the server.

For safety of data going into the database, tags are converted to their html special characters and certain characters are escaped before being prepared and sent to the database.

Data retrieved needs to be decode. While a simple `htmlspecialcharacter_decode()` can do the job, for display, leaving it as a special character is safe, and so i made a utitlity javascript function for special character decode on demand, eg passing location data.

For the community editor, `fileReader` is used to convert files to their base64 reprisentation, as well as their temporary url representation, which i then pass to an image tag `src` to display the current selected image.

A video walkthrough of this project is available:

      https://youtu.be/OaaXgO6btcY
