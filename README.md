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

**BACK END**: The back-end was built with good old **PHP** and **MYSQL**.

This project was writen in facebook react library and its source code is avaible on github repo:  `https://github.com/johnerry/swiip`.

**OTHERS**: Third party API's, plugins, packages and more used in this project include, **PayStack API**, **Google Map API**, **Draft.js** (for text editing which is one of **facebook features** that can be integrated to React). To see the list of packages used in this project, see the package.json file in the github project directory above. Last but not the least, i made use of some unicode characters, as well as fontawesome icons in this project.

**INTEGRALS**: The some templates used in this project is sourced from core-ui package. `CORE_UI` contains a list of templates for i.e toggles, breadcrumbs, input, modal etc. You can check their github repo to download, or on how to intall it here `https://github.com/coreui ` it can be installed using `npm install @coreui/coreui@ --save`

## **HOW I BUILD THE APP**

- First off all, about three months prior to this write up, i had no prior knowledge about react, redux and many more integrations that i used in this app, absolutely nothing. I only knew react to be a javascript library thats all. I planned on using just javascript but decided to google on several ideas till i stumbled upon react and what it does, so i decided to give it a try. Trust me, i never regretted it. Its just amazing how easy it is to pick it up on the job once you have a clear understanding of es6 javascript, so basically, the source code is straight forward and elaborate enough to understand by a beginner.

As a **beginner** in using react as a library. Google, Youtube totorials and stackoverflow was my companion all through the making of this audacious project.

To set the record straight, i already had prior knowledge in html,css,javascript and php before this project, and so i brushed through the react & redux totorial within 2 weeks in relative ease.

**Now lets get to the good stuff.......**

## **1\. Make a wire frame connection of what you want for the project with good old paper and pen.**

- Get some sheets and a pen and make a diagram on how the project connects together. For example, facebook. Your starting point will be the login page which is the landing page, having two input boxes for email and password. The next textual representation should be the home page. Containing top navigation bar, and a list of posts below.
- After the textual representation, proceeded to having a diagramatic representation of how the project will look like from the drafted wireframes on paper, you can also check on other websites for further ideas to add to your own. This diagrams should be the boxes, input, placeholder post flow and others. For Swiip, it started with a login page, with self hiding register view depending on viewport, followed by the account page, containing an image view, and some list of input boxes. These pages need to be interconnected, one leads to the other, which provides a natural flow to your app. Also take note on responsive design patterns while creating this diagrams.

## 2\. Proceed to making a demo representation in actual code

- This means actually presenting your diagrams in actual code. This involves alot of css and html for now. The javascript comes later. For the login page,

`@media screen and (max-width: .....px) { ....}`

- The line of code above takes care of responsive activity, on the page. The viewport is already added in the project default files. You can create your css file in the root file directly and imported into `app.js` so it serves every other file and component you build. For a smooth design, you can opt to use other text editors apart from vscode and an external `.html, .css` file. The reason for this is the number of times React reloads to make sure it renders you changes. Using external files will make sure you can fully make design choices and reload it when you are done. Ones done, always make sure to change all HTML tag to their JSX equivalent.
- For the login page, start with adding a margin, top and buttom to give it that centered feel, with a `div` surrounding the two input boxes and buttons. Give it each a class name and proceed to styling with css.
- The next after the login page was the register page and message page. I figured this should be taken care of, as they are the open directories.
- The `register.js` Uses tabs from `core-ui` template. You can check more on tabs from their tab.js file in their bundled app directories. Thes two tabs holds the customer and agent form. Since they share several input boxes together, you should assign this design to a variable and then include them in the full representation of thier form i.e Customer and agent form has a `phone` input field. Assign this to a variable like `let inputBox = <input......`, and after making the the two form fields, add it into it. `<form > <input > ...{inputBox}...</form>`
- Proceed to making the dashboard, for the dashboard, it has a `DefaultHeader.js`, `DefaultFooter`, all imported to the `DefaultLayour.js` files. In the `DefaultLayout.js`, should be your side panel with a mapped list of route links. Immediately on the right is the containing `div` that every other routes are displayed in. Import your list of routes object array and map it withing a router `switch` to make sure only one route is shown at a time.
- For the container tag that host every other routes, has a breadcrumb div that shows the root and subdirectories you are currently navigating. For more on how to use breadcrumbs, check `breadcrumb.js` in the core-ui folder directory.

## 3\. Building the `account.js` template

- Start by adding the html and css template. For the image view. Surrount an image tag by input label. The imput is of type files. This input==file tag should be hidden and the label tag that represent it can be styled accordingly. Create a `Ref` to the input tag and an `onChange` handler. In the `onChange` handler method, use a file reader function to get capture the image file selected. This `fileReader` is useful for converting images and more to their base64 equivalent which can then be passed into a json format, or creating a temporary url representation of the file you selected. Meaning, a url you can insert as the source to the invinsible image tag to display the image you selected. For more on fileReader, check `https://developer.mozilla.org/en-US/docs/Web/API/FileReader`
- For every other thing below the image tag, their is a container and two seperte div with a max with of 20% and 80%. The first house the image representation of the input box, and the other house the input box, controlled by an `onChange` handler.
- State inside the constructor methos hold the changes to each input boxes. This is thesame all through the other pages in the project.
- For the community `index.js` Start by creating a markup of two or three colums wrapped inside a div, the columns hold each community details like the `image`, `fundNeeded`, `location` and `text`. the columbs or rather called cards uses `display: flexbox;` assigned a `flex: 1 1 auto` meaning they all maintain same height regardless of the `text.length` size in each. For more on the css styles used to make these column match each other in height and width with sepreration from each other, check the community_container list of style in the theme.css file.

## 4\. Handling redux store for the entire app

- Start by creating a store directory and having an `index.js` Your redux store should use a middleware and combineReducers() function that keeps each data seperate in one access store. Kind of like having multiple holders of different information and are accessed seperately. For this we have the `userData`, `communityData`, `orderData` and more...
- Then moved to create initial state for these reducers, along with the actions to perform such as:

`FETCH_COMMUNITY_DATA_SUCCESS` etc, that are then exported to the store which `combines` them for safe keeping and distribution between components that had the ` { connect } from'react-redux'` higher order imported. The `connect`, connects each component to the store and each components that requires information from the store is wrapped with connect, along with `dispatch` and `props` method that helps to send data, and get the latest information from the redux store when it arrives. This latest information is checked in the `componentDidUpdate` method and appropriate handling is done when a new change is captured.

## 5\. Creating a safe storage for the app that doesn't reset when the app refreshes

- For PHP equivalent of session_ in javascript, i used browser `localStorage`, and `sessionStorage` to storing some no critical data, such as token etc that accompanies axios requests to the server, which verifies it and return a new one. This locally stored non critical data also keeps a user logged in for the duration of their choice. Local, being forever and Session being for a single period till the page closes. It also identify user, routes (private and non private) which ensures no access to several forbidden routes for agents, customers and admins. It is essential that the app keeps some data used throught this app even if the user decides to reload for example. The states and redux store are reset to empty.
- This stored data can be used to render the appropriate data when need. Example of this is getting the user email, token, image url and more.

For example: `getAuthEmail()` gets the email text for the user, nd `getAuthToken()` gets the latest user token that accompanies each ajax request. Below check if these are set, once set, i means the user has been authenticated and already logged in. Onces authenticated, diplay the protected routes for the user, if not authenticated, log the user out.

`render={(props) => (getAuthEmail() && getAuthUserType() ? (`

`<Component {...props} />`

`)`

## 6\. Creating seperate routes for each users (admin, agent, customer), so they do not access urls not assigned to them

The routes are different for each users and so to ensure no mix of routes for customer, agent and admin, births this function:

`routePicker(user_type, cusRoutes, agtRoutes, admRoutes) {`

`return {`

`'customer': cusRoutes,`

`'agent': agtRoutes,`

`'admin': admRoutes`

`}[user_type];`

`}`

- The route picker function, which list of routes are its arguments returns the list of available routes for that user. Before actually mapping the return `route` inside `switch` in the container `div` used in the `defaultLayout,js` file.
- The routeList.js contains a bunch of routes imported in and structured objects inside an array, which is then exported to the defaultLayout to be mapped through in the switch statment inside the container div that shows all these routes. For list of routes, check `routeList.js`
- After following the same convention in building the order page, summary and more, and including their route in the `routeList.js`, you can move to check on **PayStack**. Paystack is a simplified payment api you can integrate into your project for a simple payment platform. Their documentation is simple and straight forward for any use cases.
- To start using Paystack, you can decided to create a seperate component for it. The inline-paystack api is easy to integrate. Start by dynamically creating a script file in the `componentDidMount` method using `document.createElement()` assigning its `src`  and appending it to windows.
- Then create an onClick handler that initialise the `payWithPaytack()` function/method. For more on this function, check the payment directory in `https://github.com/johnerry/Swiip` where this project source code is hosted, or check the doc directly on `https://paystack.com` for more information.
- For the backend, i used php and mysqli, you can opt for anything that suites you. If you are familiar with firebase, you can use that as well, but this tutorial only covers the front-end side of it, which is hosted at `https://github.com/johnerry/Swiip`
- After creating a **database table**, if you are using php or other server side language, you can go back to the front end, and integrate **axios** for the ajax requests and then **redux** to store these data. Since these data varies i.e **account data**, **community data** etc and they all needed their seperated stored states, so use a middleware and several dispatch functions to handle different requests to the server.
- For convinience sake, data snapped up at the `componentDidUpdate` returns token, while some do not. This is because, you can limit setting new token for critical changes you make, while navigating the app. For something as critical as making changes to your **account** data to **order** data and more requires this, while getting the list of **communities** from the server can omit this.

## 7\. Integrating google map

First of all, you should check google map javascript api, and samples are the best way to learn how they work. check it here:  `https://developers.google.com/maps/documentation/javascript/examples`

- For geoloaction, routes, map, imagery, etc, you will see all the samples, which makes it easy when trying to integrate one feature with the other. On this project SWIIP, you will see that imagery, routes and map are fused to work together, thats the power of google map. Its worth checking out.
- To make locating customers easy, you should decided to integrate google maps to your project. That is because it give an accurate location through using users latitude and logitude calculations, and can also give route, and imagery of certain location to give a discriptive representation to the agent, what they should look out for, and how to pin point customers location without getting confused or calling them on their line for directions, they can simply follow the route given.
- Once again, for more on google map, read on google map javascript api. They have samples for beter understanding and use cases.
- One major issue with google map could be is its lack of React package, leaving this to a third party integration from a different source entirely. This source(s) lack better documentation and cannot be easily understood for my use case. Since React is javascript, and thirparty api uses their javascript documentation anyway, you should decide to use google map official javascript documentation, by dynamically creating the script on demand like the payStack api above.

## 8\. Use Links rather than anchor tags

- Links are part of React. They are thesame with anchor tags in html but has added advantages or features. For example, they take care of routing, so that the page does not refresh like in using a normal anchor tag, and they can carrry alone with them seperate information know as props to the location they target.
- One good usecase of this is in the mesage.js file in swiip project directory. Once a user registers, they are directed to the message.js which serves them the `props.data` information passed along in the `link` from `register.js` This also alows message.js to be used to serve other functions like password_reset as a default view, and congratulatory message in extension when the props.data is no longer available or the page must have been refreshed.

## 9\. Looping through each JSON object returned from the server for a listview display, i.e community list

- Each community is a JSON **object** inside an array and so should be **mapped** through to be displayed to the user. i.e `ArrayOfObject.map( call_back_function( each_object) { return <div> each_object.title </>})` maps through the list of object inside the array.

## 10\. The order and order summary page

- In the order page, make use of localStorage to store the state of `orderQty`.  Meaning, with an increament and decreament button. This ensures the data always stay thesame even after a refresh. Then in the summary page, a payment button that initialise PayStack API component in the project and followed by a call back function in PayStack API that sends the information to the server for verification and storage.

## 11\. Integrating the text editor used for editing the community list.

- First visit `https://draftjs.org` draftjs is a Facebook built feature that can be integrated to your React projects. This gives you a text editor like a mini word processor. It uses states to store its data, and histories. This can then be converted by using its `getCurrentState()` method from the editor. This currentState can then be converted to JSON object, suitable for database safekeeping. These object can also be converted to its text editor equivalent. 
- A thirdparty package called drafttohtml used in this project converts draft object to html string. Of cause these string cannot be used in JSX, so the need to convert them to a valid JSX syntax is necessary. This was achieved using the nodePasser function in utitltyFunction.js in utils directory from the source code folder at `https://github.com/johnerry/Swiip`.
- The community list which are limited to changes by the admin, needs a text editor and facebook Draft.js, or its equivalent css rapping of it, used in this project can be used in your projects, that is refering to `react-draft-wysiwyg` package.

## 12\. Sending JSON string to the server for processing

- For sending request to the server throught this project,  `formData()` method in browsers was used, this let's you construct and send request like in a normal form in html with an action attribute. 
- You should take not that **POST** data is almost equivalent of  **GET** , ony that it is more secure, invisible in the url, suitable for form data, but it still uses a url construct, athough not visible but it how it sends data too and also suitable for long length of information. Also take note that data could change once it gets to the server, even while using **POST** request. Things like `"+"` are represented as `" "`, this can create a bug in your app because, token, password or any text can contain things like this and you wouldn't want that to happen. So, you would need to `encodeURIComponent` for the JSON data sent to the server, and then decode it at the server.
- For safety of data going into the database, things like html tags, quotes etc are converted to their html special characters and certain characters are escaped before being prepared and sent to the database. So, data retrieved from the database needs to be decode. While a simple `htmlspecialcharacter_decode()` can do the job in the php side before being sent to the browser, for display purposes, leaving it as a special character is termed safe, and prevent running conspicious scripts in your aplication. So, you can make use of a utitlity javascript function for special character decode on demand for certain necessary use case, eg passing location object which this function can convert its htmleqivalent of double quotes back to object string with quotes and then parse to JSON object used in google map.

A video walkthrough of this project is available @:

```
  https://github.com/johnerry/How-to-build-Swiip

```
