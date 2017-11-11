# STEP 3

1. In the todo-list-element.html add the the name property
```javascript 
name:{
	type:String,
	value:"homeworks"
}
```
![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/0.png)

2. Change the ``` <h1>My First todo list</h1>``` to ``` <h1>[[name]]</h1> ``` and reload the page


![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/1.png)

### data binding 

#### to a host property
```<my-element my-property="[[hostProperty]]"></my-element>```


#### to a host property
``` <a href$="[[hostProperty]]">```

Double-curly brackets ( _{{ }}_ ) support both upward and downward data flow.
Double square brackets ( _[[ ]]_ ) are one-way, and support only downward data flow.

3. Add a new property todoList (Array) to the todo-list-element
![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/2.png)

4. In the template tag add the following code beneath the h1 tag 
![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/3.png)

5. In the polymer-codelab-app.html, create a new property a todoListCard (Object)
![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/4.png)


6. In the polymer-codelab-app.html change the following line 

```<todo-list-element></todo-list-element>``` 

to


```<todo-list-element name="[[todoListCard.name]]" todo-list="[[todoListCard.todoList]]"></todo-list-element>```

And reload the page

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/5.png)


7. The result should look like this

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/6.png)

8. Add the style tag on the top of the template tag
![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/7.png)
9. Add a checkbox to see if a task is complete ```<input type="checkbox" checked>```

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/8.png)

10. Your element should look like this by the way 

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/9.png)

11. Reload the page !

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/10.png)


12.  Change in polymer-codelab-app.html  the todoList property of the todoListCard object to see if a task is complete

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/11.png)

13. Update the dom-repeat template of the todo-list-element 

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/12.png)

14. Reload the page (we do like the F5 ...)
![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/13.png)

#### What if the todoList is still empty ?

Well the UI of our newly born element should at least handle the case of an empty array. When we create a new todo-list we know that the least is empty at the start time.

to achieve this we use a data binding helper, the *dom-if*

dom-if ensures that in the case of empty array we show the user the message
“The list is empty”

15. Add the following code at the end of the template tag in todo-list-element.html

![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/14.png)

16. Add the following line to polymer-codelab-app.html
```<todo-list-element name="Chores" todo-list="[]"></todo-list-element>```

17.Reload the page, the result should look like this :


![ ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_3/14.png)


### and with this we have seen what is data binding !