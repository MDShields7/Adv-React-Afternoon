# Afternoon Practice

## (Part 1) presentation / container

### step 1 (container)

Build a container component that makes an axios call to the swapi api to retreive specific character by id including the characters homeworld (the homeworld will be a nested axios call)

The Data you should be getting

**Character**

-   name
-   height
-   mass
-   hair_color
-   skin_color
-   homeworld


    - It should setState with the character data
    - The first call to get the character data only returns url for the homeworld property, you will need to make a nested axios call to get the `name` of the homeworld
    - setState with all returned data

### step 2 (display)

-   Build a Display Component that will only be worried about the ui of you component, you can make either a stateless functional or a class

### step 3 (hook it up)

import the Display into the Container component pass props down to the display component

be creative in how you display this components props!

## (Part 2) HOC's

### step 1 (Build HOC)

Create a higher order component that accepts both a Component and a URL as arguments and returns a new component with the data passed in as a prop.

this is the data you should plan for in your Display Class Component, feel free to add more data from the API (stretch yourself and refer back to the nested call you did in step 1 for inspiration)

**character**

-   name
-   height
-   mass
-   hair_color


    - Create a function call `myHOC` that returns an anonymous class
    - declare a function within the anonymous class called `fetcher` that fetches data using an axios call and the URL passed in to the HOC. setState with the returned data
    - the Anonymous class should return the component that was passed into the HOC with all props and state passed to the returned component as props

### step 2 Build a reusable display

Create a Display Class Component that will be wrapped by the HOC.

-   import the HOC into your class component
-   Export Default the Invoked HOC with the display class component passed in as the first argument and the URL of a swapi character as the second argument
-   render the display component in App.js

### step 3 Style

style your component beautifully!

## (Part 3) Render Props

-   using the lecture code as an example recreate part 2 using render props instead
