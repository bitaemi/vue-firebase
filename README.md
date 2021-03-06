<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Visual Studio Code Installed extensions](#visual-studio-code-installed-extensions)
- [1. Dinamically bind data using `v-bind` directive](#1-dinamically-bind-data-using-v-bind-directive)
- [2. React to events with v-on directive](#2-react-to-events-with-v-on-directive)
- [3. React to double click events with v-on directive](#3-react-to-double-click-events-with-v-on-directive)
- [4. The Event Object](#4-the-event-object)
- [5. KeyBoard Events](#5-keyboard-events)
- [6. Two Way Data Binding](#6-two-way-data-binding)
- [7. Event and Key Modifiers](#7-event-and-key-modifiers)
- [8. Conditional Output with v-if](#8-conditional-output-with-v-if)
- [9. Looping with v-for](#9-looping-with-v-for)
- [10. The Vue CLI 3](#10-the-vue-cli-3)
- [10.1. VUE CLI Service, Plugins](#101-vue-cli-service-plugins)
- [11. Components and Vue files](#11-components-and-vue-files)
- [12. The data() function](#12-the-data-function)
- [13. Nesting components](#13-nesting-components)
- [14. Scoped CSS - not as efficient](#14-scoped-css---not-as-efficient)
- [15. Passing Data with Props](#15-passing-data-with-props)
- [16. Custom Events](#16-custom-events)
- [17. Life-cycle Hooks](#17-life-cycle-hooks)
- [18. Making Requests with Axious](#18-making-requests-with-axious)
- [19. Filters](#19-filters)
- [20. Computed Properties(custom search box)](#20-computed-propertiescustom-search-box)
- [21. What is the Vue Router](#21-what-is-the-vue-router)
- [22. Setting up Routes](#22-setting-up-routes)
- [23. Router Links](#23-router-links)
- [24. Route Parameters](#24-route-parameters)
- [25. Watching the $route Object](#25-watching-the-route-object)
- [26. More on Router Links](#26-more-on-router-links)
- [27. Programmatically Redirecting Users](#27-programmatically-redirecting-users)
- [28. Hash vs History Mode](#28-hash-vs-history-mode)
- [29. Styling Active Links](#29-styling-active-links)
- [30. Project Preview & Setup](#30-project-preview--setup)
- [31. Project Structure](#31-project-structure)
- [32. Material Design](#32-material-design)
- [33. Navbar Component](#33-navbar-component)
- [34. Index Component](#34-index-component)
- [35. Deleting (local) Data](#35-deleting-local-data)
- [36. Introduction to Firebase](#36-introduction-to-firebase)
- [37. Setting up Firestore](#37-setting-up-firestore)
- [38. Installing Firebase](#38-installing-firebase)
- [39. Retrieving Firestore Data](#39-retrieving-firestore-data)
- [40. Deleting Firestore Data](#40-deleting-firestore-data)
- [41. Add Smoothie Component](#41-add-smoothie-component)
- [42. Adding Ingredients](#42-adding-ingredients)
- [43. Outputting Ingredients](#43-outputting-ingredients)
- [45. Saving Records to Firestore](#45-saving-records-to-firestore)
- [46. Deleting Ingredients](#46-deleting-ingredients)
- [47. Edit Smoothie Route](#47-edit-smoothie-route)
- [48. Firestore Queries](#48-firestore-queries)
- [49. Edit Smoothie Form](#49-edit-smoothie-form)
- [50. Updating Firestore Records](#50-updating-firestore-records)
- [51. Deploying to Firebase](#51-deploying-to-firebase)
- [52. Chat Project Overview & Setup](#52-chat-project-overview--setup)
- [53. Passing `props` via Routes](#53-passing-props-via-routes)
- [54. Route Guard](#54-route-guard)
- [55. Add Firestore Docs in non-existent Collection](#55-add-firestore-docs-in-non-existent-collection)
- [56. Real time Events (Event Listeners)](#56-real-time-events-event-listeners)
- [57. Formating time with Moment.js](#57-formating-time-with-momentjs)
- [58. Auto scrolling for a Real Time Updating Page](#58-auto-scrolling-for-a-real-time-updating-page)
- [59. Google Maps Api](#59-google-maps-api)
- [60. Creating a new Map](#60-creating-a-new-map)
- [61. Firebase Auth](#61-firebase-auth)
- [62. Form Validations](#62-form-validations)
- [63. Route Guarding (auth)](#63-route-guarding-auth)
- [Check auth status with onAuthStateChanged](#check-auth-status-with-onauthstatechanged)
- [64. Google Map Marker](#64-google-map-marker)
- [65. Real time comments update](#65-real-time-comments-update)
- [66. Firebase Cloud Functions](#66-firebase-cloud-functions)
- [67. Firebase Rules](#67-firebase-rules)
- [68. Deploy to Firebase](#68-deploy-to-firebase)
- [69. Instant Prototypeing](#69-instant-prototypeing)
- [70. Use VUE CLI 3 to build App, Libs or Web Components](#70-use-vue-cli-3-to-build-app-libs-or-web-components)
- [71. Use VUE CLI GUI](#71-use-vue-cli-gui)
- [72. Redux Store in Vue](#72-redux-store-in-vue)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

Vue:

 - front-end JS framework  used for web SPAs or widgets

 - very small compared to Angular or React

 - for this project you need to replace the indexFake and initFake with real configs 

# Visual Studio Code Installed extensions

  VS Live Share

  npm Intellisense

  Debugger For Chrome

  TS Lint

  Auto Import

  Sass

  Npm

 Live Server, Monokai++, Vetur

# 1. Dinamically bind data using `v-bind` directive

    `<a v-bind:href="url">Youtube</a>`

    or shorter:

    `<a v-bind:href="url">Youtube</a>`

# 2. React to events with v-on directive

An event object is created;

```HTML
<p>I earn {{ wage }} pounds per hour</p>
<button v-on:click="wage++">Increase wage by 1$ </button>
<button v-on:click="changeWage(-1)">Decrease wage by 1$ </button>
```
# 3. React to double click events with v-on directive

``<button v-on:dblclick="changeWage(-4)">Decrease wage by 4$</button>``
# 4. The Event Object

```HTML
    <button @click="logEvent">Log Event info</button>
    <div class="canvas" @mouseMove="logCoords">{{ coords.x }},{{ coords.y }}</div>
```
```TypeScript
new Vue({
    el: '#app',
    data: {

    },
    methods: {
        logEvent(e){
            console.log(e);
        },
        logCoords(e){
            this.coords.x = e.offsetX;
            this.coords.y = e.offsetY;

            console.log(screenX, screenY);
        }
    }
});
```

# 5. KeyBoard Events

```HTML
<p>My name is {{ name }}</p>
<input type="text" @keyup="updateName">
```

```TypeScript
// ...
   updateName(e) {
            // console.log(e.target.value);
            this.name = e.target.value;

    }
```

# 6. Two Way Data Binding

```HTML
<p>Two way data-binding for title {{ title }}:</p>
<input type="text" v-model="title">
```

# 7. Event and Key Modifiers

Modify how we listen to click or key events using the `.` like this:

```HTML
<button @click.alt="eventModifiers">Test alt-click event key modifier</button>
<button @click.alt="eventModifiers">Test shift-click event key modifier</button>
```
runs eventModifiers method if Alt key, respectivly Shift is pressed when mouse clicking.
``
<a href="google.com" @click.prevent="eventModifiers">Google</a>
``
prevents default behaviour.

# 8. Conditional Output with v-if

`v-if` and `v-else-if` directives

```HTML
<p v-if="!loggedIn"> v-if show 'Login' for logged in {{ showName }}:
    <button @click="login">Login</button>
</p>
<p v-else-if="showName"> v-else-if show 'Hi, {{ name }}' for knowned loggedin user: {{ showName }}
    <button @click="logout">Logout </button>
</p>
```
# 9. Looping with v-for

```HTML
<div v-for="(ninja, index) in ninjas">
    <p>
        {{ index }}.{{ ninja.name }} is {{ ninja.age }} years old and has a {{ ninja.belt }}
    </p>
</div>
```
 where ninjas is an array of objects.

# 10. The Vue CLI 3

for the old CLI:

`npm i -g vue-cli`
`vue init webpack-simple vueproject`
...

For the new CLI 3:

`npm uninstall -g vue-cli`

`npm i -g @vue/cli` install cli package from @vue scope

`vue create vueproject`

- allows change of project config using plugins;

- graphical User Interface

Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, consult the [docs for vue-loader](http://vuejs.github.io/vue-loader).

# 10.1. VUE CLI Service, Plugins

`vue-cli-service serve` or ``npm run serve`` to preview  the app

``npm run lint`` to log the errors

Add plugins running: `vue add vuetify` - this will add the plugin `cli-plugin-vuetify` into package.json, dependencies file.

# 11. Components and Vue files

```TypeScript
new Vue({
  el: '#app',
  render: h => h(App)
})
```
because we want this instance to control the #app element.

Each Vue object/instance has a corresponding component (e.g. App.vue - the main component) with a template containing one main div(<div id="app">) identified by the value of 'el' (#app) object property.

# 12. The data() function

```JavaScript
data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
```
The data() function from each component is required to protect the data and make it unique (if if had been just an object,

data wouldn't be protected because it would be shared between components).

# 13. Nesting components

```JavaScript
import Nav from './Navbar';
// ..
export default {
  name: 'app',
  components: {
    Nav,
    // ..
  },
```
# 14. Scoped CSS - not as efficient

Vue.js automatically applies the `<style>` from a component side-wide( to all components imported into main component), not oly to that component.

- for scopeded CSS (available just for that component) we have to apply use scoped keyword `<style scoped>`,

but preferably, don't use it because is not so efficient - but rather add classes to elements.

Ctrl+Shift+R - hard refresh page to see changes after this CSS change.

# 15. Passing Data with Props

is the @Input from Angular - here we bind data using `:` in front of the property added in the component in the props array:

```HTML
    <OnlineFriends :friends="friends"/>
```
also add :

```JavaScript
export default {
    name: 'OnlineFriends',
    props: ['friends'],
   // ..
}
```

where friends is data inside the main component.

# 16. Custom Events

Delete a friend from data.

We use the `$emit` method to emit custom events (here delete) from the child component to main component:

```JavaScript
    methods: {
        unfriend(friend) {
            this.$emit('delete', { name : friend });
        }
    }
```
Parent component listens at the emitted  event in the component's call:

```<AllFriends :friends="friends" @delete="deleteFriend"/>``` (use `v-on:` or `@`)

and has the deleteFriends method:

```JavaScript
  methods: {
    deleteFriend(payload) {
      this.friends = this.friends.filter(
        friend =>  friend.name !== payload.name
      )
    }
    // ..
```

# 17. Life-cycle Hooks


- beforeCreate

- created ( load any data here)

- beforeMount (before compoment loads into the DOM)

- mounted

- beforeUpdated

- updated

- beforeDestroy

- destroyed (here any required cleanup after the component has been destroyed)

# 18. Making Requests with Axious

`npm i axios`

```JavaScript
    console.log('created hook');
    axios.get('https://jsonplaceholder.typicode.com/posts')
        .then(response => {
        console.log(response);
        this.posts = response.data;
    })
    .catch(error => console.log(error))
```
# 19. Filters

Add the snippet filter in main.js

```JavaScript
Vue.filter('snippet', val => {
  if(!val || typeof(val) != 'string') {
    return ' ';
  }
  val = val.slice(0, 50);
  return val + '...';
});
```
apply the filter(pipe from Angular) using the pipe:

```HTML
    <p>{{ post.body | snippet }}</p>
```
# 20. Computed Properties(custom search box)

The `computed` prop looks at some data  and manipulates that data

Add the `computed` property in component's export:

```JavaScript
export default {
    name: 'Blogs',
    data() {
        return {
            // ..
            posts: [],
            searchTerm: '',
            // ..
        }
    },
    computed: {
        filterPosts() {
            return this.posts.filter(
                posts => posts.title.match(this.searchTerm)
            );
        }
    },
    // ..
```
Iterate through the return of computed object (filterPosts() object), instead of all posts:

```HTML
    <div v-for="post in filterPosts" :key="post.id">
        <h3>{{ post.title }}</h3>
        <p>{{ post.body | snippet }}</p>
    </div>
```
# 21. What is the Vue Router

`vue init webpack vuerouting` with the old CLI

`vue create vuerouting`

to generate a new project with router

# 22. Setting up Routes

in main component we have : `<router-view/>` tag wich will load

all components added inside the Router object from index.js.

```JavaScript
Vue.use(Router)

export default new Router({
  routes: [
    {
      path: '/home',
      name: 'Home',
      component: Home
    },
    {
      path: '/about',
      name: 'About',
      component: About
    },
    {
      path: '/profile/:user_id',
      name: 'View Profile',
      component: ViewProfile
    }
  ]
  // ...
```
access the about page: http://localhost:8080/#/about

# 23. Router Links

We do not use `<a href=''>`, instead we use `<router-link to=''>` or `<router-link :to={}>`:

```HTML
    <li><router-link to="/">Home</router-link></li>
    <li><router-link :to="{ name: 'About' }">About</router-link></li>
```

# 24. Route Parameters

read the param from route:

```JavaScript
  data() {
      return {
          userId: this.$route.params.user_id
      }
      // ..
```

# 25. Watching the $route Object

```JavaScript
    methods: {
        updateId() {
            this.userId = this.$route.params.user_id;
        }
    },
    watch: {
        $route: 'updateId'
    }
```
when we have the watch property, the updateId will run and update data with the new route parameter;

# 26. More on Router Links

```HTML
    <li v-for="(id,index) in userIds" :key="index">
        <router-link :to="{name: 'ViewProfile', params: { user_id: id}}">
            <span>User Profile {{ id }}</span>
        </router-link>
    </li>
```
# 27. Programmatically Redirecting Users

`this.$router` keeps track of all routes, versus: `this.$route` that refers to the current route;

```JavaScript
    goHome() {
        this.$router.push({name: 'Home'});
    },
    goBack() {
        this.$router.go(-1);
    },
    goForward() {
        this.$router.go(1);
    }
```

```HTML
    <div>
        <button @click="goHome">
        Redirect to home
        </button>
        <button @click="goBack">
        Go back
        </button>
        <button @click="goForward">
        Go forward
        </button>
    </div>
```

# 28. Hash vs History Mode

The `#` symbol in links is required to be there to prevent a new call to the server, when accessing a new page.

**On local server**, to hide the hash, we set the `mode` property of the browser to 'history':

```JavaScript
  export default new Router({
  mode: 'history',
  routes: [
      // ..
```

# 29. Styling Active Links

```CSS
.router-link-exact-active {
  color: blue
}
```

# 30. Project Preview & Setup

Use Firestore = a real time noSQL database provided by Firebase.

# 31. Project Structure

# 32. Material Design

use Material CSS library: (https://materializecss.com/getting-started.html)[https://materializecss.com/getting-started.html]

# 33. Navbar Component

```HTML
<div class="navbar">
    <nav class="nav-extended indigo darken-2">
        <div class="nav-content">
            <router-link to="">
                <span class="nav-title">Ninja Smooties</span>
            </router-link>
            <a href="" class="btn-floating btn-small halfway-fab pink">
                <router-link to=""><i class="material-icons">add</i></router-link>
            </a>
        </div>
    </nav>
</div>
```

# 34. Index Component

```HTML
<div class="index container">
<div class="card" v-for="smootie in smooties" :key="smootie.id">
    <div class="card-content">
    <h2 class="indigo-text"> {{ smootie.title }}</h2>
    <ul class="ingredients">
        <li v-for="(ing, index) in smootie.ingredients" :key="index">
        <span class="chip">
            {{ ing }}
        </span>
        </li>
    </ul>
    <i class="material-icons delete" @click="deleteItem(smootie.id)">delete</i>
    </div>
</div>
</div>
```
# 35. Deleting (local) Data

```JavaScript
deleteItem(id) {
    this.smooties = this.smooties.filter(
    smootie => smootie.id !== id
    )
```

# 36. Introduction to Firebase

Use Firestore :

- a real time noSQL database provided by Firebase

- authentication

- app deployment

# 37. Setting up Firestore

Google Firebase -> Go to Dashboard


# 38. Installing Firebase

``npm i firebase``

Project Overview and click on: </> to copy the config object

# 39. Retrieving Firestore Data

- files initFake.js(src/firebase path) and indexFake.html should be replaced with index.html and init.js (currently mentioned in .gitignore)
```JavaScript
import firebase from 'firebase';

//initialize Firebase

var config = {
    apiKey: "YOUR_API_KEY",
    authDomain: "ninja-smooties-97572.firebaseapp.com",
    databaseURL: "https://ninja-smooties-97572.firebaseio.com",
    projectId: "ninja-smooties-97572",
    storageBucket: "ninja-smooties-97572.appspot.com",
    messagingSenderId: "291122468448"
  };

const firebaseApp = firebase.initializeApp(config);

// firebaseApp.firestore().settings({timestampsInSnapshot: true});

export default firebaseApp.firestore();
```
 and in the created life cicle hook:

 ```TypeScript
   created() {
      db.collection('sooties').get()
      .then(snapshot => {
        snapshot.forEach(doc => {
          // console.log(doc.data(), doc.id);
          let smootie = doc.data()
          smootie.id = doc.id
          this.sooties.push(smootie)
        })
      }).catch(err => console.log(err))

  },
```

# 40. Deleting Firestore Data

```TypeScript
    deleteItem(id) {

    db.collection('sooties').doc(id).delete()
        .then(() => {
        this.sooties = this.sooties.filter(
            smootie => smootie.id !== id
        )
        })
    }
```        

# 41. Add Smoothie Component

Prevent the defalt behaviour of the submit event(refresh page), using the prevent modifier:

```HTML
<form @submit.prevent="AddSmootie">
```

``<input type="text" for="title" name="title" v-model="title" >``

# 42. Adding Ingredients

After entering an ingredient, and pressing tab the defalt event of passing to the following field is prevented

and addIng method is executed:

```HTML
    <div class="field add-ingredient">
        <label for="text" name="add-ingredient">
            Add an ingredient:
        </label>
        <input type="text" for="add-ingredient" @keydown.tab.prevent="addIng" v-model="another">
    </div>
```
# 43. Outputting Ingredients

```HTML
    <div v-for="(ing, index) in ingredients" :key="index">
            <label for="ingredient">
            Ingredient:
            </label> 
            <input type="text" v-model="ingredients[index]" />
    </div>
```            

# 45. Saving Records to Firestore

`npm i slugify --save` to import a llibrary to generate slugs

```JavaScript
    AddSmootie() {
        if (this.title) {
            this.feedback = null
            this.slug = slugify(this.title, {
                replacement: '-',
                remove: /[$*_+¬.()'"!\-:@]/g,
                lower:true
            })
            db.collection('sooties').add({
                title: this.title,
                slug: this.slug,
                ingredients: this.ingredients
            }).then(
                () => this.$router.push({ name: 'Index' })
            ).catch( err => console.log(err))
        } else {
            feedback = ' You must enter a new title'
        }

    },
```

# 46. Deleting Ingredients

Delete an ingredient localy, before saving into database:

```HTML
    <div class="field" v-for="(ing, index) in ingredients" :key="index">
        <label for="ingredient">
        Ingredient
        </label> 
        <input type="text" v-model="ingredients[index]" />
        <i class="material-icons delete" @click="deleteIng(ing)">delete</i>
    </div>
```

```JavaScript
    deleteIng(ing) {
            this.ingredients = this.ingredients.filter( ingredient => ingredient !== ing)
    }
```        
# 47. Edit Smoothie Route

```JavaScript
    {
      path: '/edit-smootie/:slug',
      name: 'EditSmootie',
      component: EditSmootie
    }
```

# 48. Firestore Queries

collection is like a table in database, doc is like an entry in the table

db.collection.doc.update // similar to update a row from tb

db.collection.doc.add // add a row in table

db.collection.doc.push // add a row in table

db.collection.where('row', 'comparison operator', 'value for the entry to be returned').get // is a select whit where clause

db.collection.where('row', 'comparison operator', 'value for the entry to be returned').onSnapshot to use the returned snapsot with docChanges()

db.collection.orderBy.get //select with order clause


// ..

# 49. Edit Smoothie Form

is like the add form, but this time we specify input values using v-model directive with `smootie` object obtained in the `created()` 

lifecycle hook.


# 50. Updating Firestore Records

Done like this, but is not correct to get the doc id from slug if slug is not unique:

```JavaScript
    created() {
        let ref = db.collection('sooties').where('slug', '==', this.$route.params.slug);
        ref.get().then(snapshot => {
            return snapshot.forEach(doc => {
                this.smootie = doc.data();
                this.smootie.id = doc.id;
            })
        }).catch(err => console.log(err));
```
but rather use the id, or even don't make a new http request to get data, use local data!:

```JavaScript
    let ref = db.collection('sooties').doc(this.id);
    ref.get().then(doc => {
            this.smootie = doc.data();
            this.smootie.id = doc.data().id;
            console.log(this.smootie);
    }).catch(err => console.log(err));
    console.log(ref);
```

```JavaScript
db.collection('sooties').doc(this.smootie.id).update({
    // ..
```
# 51. Deploying to Firebase

access firebase  prj console: [https://console.firebase.google.com/project/myprojid/overview]

go to Hosting section

`npm i -g firebase-tools --save`

`firebase login`

`firebase init` and here:

-  navigate with the arrow to firestore option and hosting option and select each by pressing space

- press enter

- select the defalt project ( your prj name)

- select as public folder the dist folder

-select spa

`npm run build` ?? have to build the project before deploy, otherwise  you'll have an empty index filed - deployed project:

at https://myprojid.firebaseapp.com/

`firebase deploy`


# 52. Chat Project Overview & Setup

Use REAL-TIME DATA update TECHIQUE

`vue init webpack vue-chat`

`npm start`

# 53. Passing `props` via Routes

```JavaScript

    // in the redirecting component:
    
    this.$router.push({ name: 'Chat', params: { name: this.name }});

    // ... and in the Chat component:

    export default {
    name: 'Chat',
    props: ['name'],
     // ...

     // and  in router:
    {
      path: '/chat',
      name: 'Chat',
      component: Chat,
      props: true
    },
    // ...
```

# 54. Route Guard

Handle the case where the route does not exist - add a beforeEnter function value:

```JavaScript
    {
      path: '/chat',
      name: 'Chat',
      component: Chat,
      props: true,
      beforeEnter: (to, from, next) => {
        if (to.params.name) {
          next()
        }
        else {
          next({name: 'Welcome'})
        }
      }
    }
```    

# 55. Add Firestore Docs in non-existent Collection

if the collection doesn't exist will automatically create it:

```JavaScript

    db.collection('message').add({
        content: this.newMessage,
        name: this.name,
        timestamp: Date.now()
    }).catch(
        err => console.log(err)
    )
```
# 56. Real time Events (Event Listeners)

In chat's page we should see all the messages (messages = []) of the conversation

Listen for the messages when the component is created (created())

Each entered message is added in firebase, so we can use  a snapshot of the messages collection,

and get only those added using the docChanges method:

```JavaScript
    created() {
        let ref = db.collection('messages').orderBy('timestamp')
        ref.onSnapshot(snapshot => {
            snapshot.docChanges().forEach(change => {
                if (change.type == 'added') {
                    let doc = change.doc
                    this.messages.push({
                        id: doc.id,
                        name: doc.data().name,
                        content: doc.data().content,
                        timestamp: doc.data().timestamp,

                    })
                }
                
            });
        }
        )
    },
```
 # 57. Formating time with Moment.js

`npm i moment --save`

```JavaScript
 timestamp: moment(doc.data().timestamp).format('lll'),
```

# 58. Auto scrolling for a Real Time Updating Page

`npm i vue-chat-scroll`

```CSS
.messages {
    text-align: left;
    max-height:  300px;
    overflow: auto;
}
.messages::-webkit-scrollbar {
    width: 3px;
}
.messages::-webkit-scrollbar-track{
    width: #ddd;
}
.messages::-webkit-scrollbar-thumb {
    width: #aaa;
}
```

In main.js import the VueChatScroll class from the `vue-chat-scroll` library

and plugin this class(plugin = package) like this:

`Vue.use(VueChatScroll)`

# 59. Google Maps Api

Head to : (https://console.developers.google.com/apis/dashboard?pli=1)[https://console.developers.google.com/apis/dashboard?pli=1] 

to enable the Maps JavaScript Api for your project.

Then: Credentials -> Credentials Manager -> Create Credentials -> and copy the API key for later usage.

Go to: (https://cloud.google.com/maps-platform/)[https://cloud.google.com/maps-platform/]

Copy the `<script>` tag from the buttom of the page:

```JavaScript
    <script src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap"
    async defer></script>
``` 

and place it in the index.

# 60. Creating a new Map

We need to insert the map into the DOM, so we cannot create it in the created() lifecle hook of the component, but rather in the mounted()

hook, when the component has already mounted the DOM.

# 61. Firebase Auth

 The Server( Firebase ) will interact with  the Vue App:

  - Firebase Auth generates an id for each added user

  - Firestore DB will have a geolocation entry for each user(identified by id)

  - Google project console > Authentication > Get a sign-up method > email & pass method
  
   (for example)> Enable

# 62. Form Validations

For the moment we will handle the validation on Vue App side, but is better to do it using 

Firebase Cloud.
 
 - create a reference to the document (entry in the users table=collection) of interest (in this case with the provided slug):

```let usersRef = db.collection('users').doc(this.slug)```

 - use Google's Firebase Auth for autenticating users (provides field validation also):

 ```JavaScript
    firebase.auth().createUserWithEmailAndPassword(this.email, this.password)
        .catch( err => {
        this.feedback = err.message;
    })
```
Calling ``createUserWithEmailAndPassword`` of Firebase Auth service will receive the credentials object (`cred`):

```JavaScript
firebase.auth().createUserWithEmailAndPassword(this.email, this.password)
    .then(
    cred => {
        usersRef.set({
            alias: this.alias,
            geolocation: null,
            id: cred.user.uid
        })
    })
```

Get CurrentUser info : ``firebase.auth().currentUser``

Some rendering componets need firebase response and that's why we need to delay the rendering of the app until the firebase data loads:

```JavaScript
let app = null;

//wait for firebase auth before creating the app:
firebase.auth().onAuthStateChanged(() => {
//init app if not already created:
  if (!app) {
    new Vue({
      el: '#app',
      router,
      components: { App },
      template: '<App/>'
    })
  }
})
```
Logout the user using Firebase Auth method:

```JavaScript
    logout() {
        firebase.auth().signOut().then(
            () => {
                this.$router.push({name: 'Login'})
            }
        )
    }
```
Login the user :

```firebase.auth().signInWithEmailAndPassword(this.email, this.password) ```

Use browser's geolocation  info to render the map using coordinates provided by browser:

```JavaScript
    navigator.geolocation.getCurrentPosition(pos => {
            this.lat = pos.coords.latitude
            this.lng = pos.coords.longitude
            this.renderMap()
        },
        (err) => {
            console.log(err)
            this.renderMap()
        },
        { maximumAge: 60000, timeout: 3000})
```

# 63. Route Guarding (auth)

Protect page from non-authenticated users, by adding to component's route:

```JavaScript
    meta: {
        requiresAuth: true
    }
```

Before each route coming ``from`` and going `to` a route with ``requiresAuth`` ``meta`` property, the ``next`` method is called in different ways, accordig to user's auth status:

- with no params, will proceed to route

- with redirecting component as parameter

```JavaScript
router.beforeEach((to, from, next) => {
  //check to see if route requires auth

  if (to.matched.some(rec => rec.meta.requiresAuth)) {
    // check auth state of user
    let user = firebase.auth().currentUser
    if (user) {
        // user signed in proceed to route
        next()
        } else {
        // no  user signed in, redirect to home
        next({name: 'Login'})
        }
   } else {
       next()
  }
})
```
# Check auth status with onAuthStateChanged

```JavaScript
created() {
    firebase.auth().onAuthStateChanged((user) => {
        if (user) {
            this.user = user
        } else {
            this.user = null
        }

    })
},
```

# 64. Google Map Marker

Create a new google.maps.Marker object and use it to display user's current location:

```JavaScript

    db.collection('users').get().then(
        users => {
            users.docs.forEach(doc =>
            {
                let data = doc.data()
                if (data.geolocation) {
                    let marker = new google.maps.Marker({
                        position: {
                        lat: data.geolocation.lat,
                        lng: data.geolocation.lng
                    },
                    map 
                    })
                    // add click event to marker:
                    marker.addListener('click', () => {
                        console.log(doc.id)
                    })
                }
            })
        }
    )
```

# 65. Real time comments update

Use the onSnapshot and docChanges methods:

```JavaScript
    db.collection('comments').where('to', '==', this.$route.params.id)
    .onSnapshot((snapshot) =>
        {
            snapshot.docChanges().forEach(
                change => {
                    if (change.type == 'added') {
                        this.comments.unshift({
                            from: change.doc.data().from,
                            content: change.doc.data().content
                        })
                        console.log(this.comments);

                    }
                }
            )
        }
    )
```
# 66. Firebase Cloud Functions

 - can be used to create configurations to take care of all the server management ( data processing functions that we use inside our app).

``npm install firebase-functions@latest firebase-admin@latest --save``

``npm install -g firebase-tools``

``firebase login``

`` firebase init functions``

write the functions into functions/index.js

``cd ./functions``

`npm i googleapis`

`firebase deploy --only functions` to deploy the functions to Firestore

# 67. Firebase Rules

You can restrict database access, changing the `Rules` section or the firestore.rules file

```
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read;
      allow write: if requests.auth.uid !=null;
    }
  }
}
```
deploy project to propagate rules changes to Firebase.

# 68. Deploy to Firebase

Remember to use VUE CLI 3 and you will build the app simple:

`nmp run build` ( this is not  executing the build.js file like in the old project created with the old VUE CLI)

You can access your firebase app at https://yourprjname.firebaseapp.com after deploing:


`firebase deploy --only hosting`

# 69. Instant Prototypeing

`npm  i -g @vue/cli-service-global`

this adds the serve vue cli and we can run:

`vue serve online.vue` inside's online.vue component to instantly preview the component

# 70. Use VUE CLI 3 to build App, Libs or Web Components

`npm  i -g @vue/cli-service-global`

we build the web componet into a web component(online-status):

`vue build online.vue --target wc --name online-status`

# 71. Use VUE CLI GUI

`vue ui`

and  in the opened [http://localhost:8000/project/select]:

import your projects

or create a new one with the default presets ...
cd into prj folder and run npm serve

# 72. [Redux Store in Vue](./src/redux/README.md)