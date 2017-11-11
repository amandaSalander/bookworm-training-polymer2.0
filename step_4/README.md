# STEP 4

Polymer provide custom CSS properties that you can use to style the appearance of the element in your application.

it's really a powerful tool that enable us to use an element fully without having to know what does it do inside to style it like we want. One the most common use cases is to use custom properties to build a UI so that the user can style it.

1. In the terminal write the following command line


```bower install PolymerElements/paper-styles --save```

It will add paper-styles in the bower_components folder and add paper-styles to your dependencies in the bower.json file.

*paper-styles* is a Shared styles for Material Design elements ([see more](https://www.webcomponents.org/element/PolymerElements/paper-styles))

2. Import the color.html

Why Color ? well it's a complete list of the colors defined in the Material Design palette ([see more](https://material.io/guidelines/style/color.html)) . We can directly use it in our codelab

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/2.png)

3. Open todo-list-element.html

4. Wrap your element template in a div 
![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/4.png)
5. Add the following style to your div in the style tag 

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/5.png)

### Take time and look at what we added

the background-color of the div tag has the value ```var(--todo-list-element-background-color)``` so when we define ```--todo-list-element-background-color the background-color``` of the div tag will take the new color.


6. Go back to polymer-codelab-app.html and add the following lines in the style tag

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/6.png)

7. Reload the page, your app should look like this

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/7.png)

8. In the todo-list-element.html add a new property important (boolean) this property explain whether the todoList is important

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/8.png)

#### An important todo-list-elememt  must have the background-color set to a red color
...

..

.

that's what I have decided !


To achieve it we use custom css properties and observers

### to brief introducing to observer 
observer is a simple way to track when a property or sub property change.
we add observer in the propery and define a method

```javascript
	important:{
    	type:Boolean,
        value:false,
        observer:"_importantChanged"
    }
    ...
    _importantChanged(newVal,oldVal){
    	...
    }
```

9. Add an observer on important property

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/9.png)

10. Define the method _importantChanged so that when important is true we change the ```--todo-list-element-background-color``` to ```paper-red-500```

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/10.png)


11. Open polymer-codelab-app.html and add important to the second todo-list-element tag

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/11.png)

12. Reload the page, your page should look like this

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/12.png)


### shadow effect !

Now let’s add some shadow effect on  the todo-list-element

13. Import the shadow.html *shadow.html* is a Material Design elevation and shadow styles

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/13.png)

14.add a class to the div wrapping 

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/14.png)

15. Now let’s apply some shadow 

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/15.png)

16.Reload the page…..well this is some shadow

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_4/16.png)