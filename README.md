# Afternoon Practice

## presentation / container

### part 1 (container)

Build a container component that makes an axios call to the swapi api to retreive specific character by id including the characters homeworld (this is a nested axios call)

The Data you should be getting:

    character = {
            name,
    	    height,
    		mass,
    		hair_color
    		skin_color
    		homeworld
    }

    - It should setState with the character data
    - The first call to get the character data only returns url for the homeworld property, you will need to make a nested axios call to get the `name` of the homeworld
    - setState with all returned data

### part 2 (display)

Build a Display Component that will only be worried about the ui of you component, you can make either a stateless functional or a class

### part 3 (hook it up)

import the Display into the Container component pass props down to the display component

be creative in how you display this components props!

## HOC's

### part 1 (Build HOC)

Create a higher order component that accepts both a Component and a URL as arguments and returns a new component with the data passed in.

this is the data you should plan for in your Display Class Component, feel free to add more data from the API

character = {
name,
height,
mass,
hair_color
}

    1.) Create a function that returns an anonymous class
    2.) declare a function within then anonymous class called `fetcher` that fetches data using an axios call and the URL passed in to the HOC. setState with the returned data
    4.) the Anonymous class should return the component that was passed into the HOC with all props and state passed to the returned component

### part 2 Build a reusable display

Create a Display Class Component that will be wrapped by the HOC.

    1.) import the HOC into your class component
    2.) Export Default the Invoked HOC with the display class component passed in as the first argument and the URL of a swapi character as the second argument
