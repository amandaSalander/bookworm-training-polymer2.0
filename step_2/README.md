# Step 2

your src/ folder
![src folder structure ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/0.png "src/ folder")

the polymer-codelab-app.html is your first element !

![polymer-codelab-app imported and used in index.html ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/1.png "polymer-codelab-app imported and used in index.html")

this is how a basic element look like

![polymer-codelab-app element ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/3.png "polymer-codelab-app element")

1. In the folder src/polymer-codelab-app create a new file todo-list-element.html
2. Add the following polymer import ```<link rel="import" href="../../bower_components/polymer/polymer.html">```
3. Add a dom-module tag with the id set to todo-list-element


![dom-module ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/4.png "dom-module")

4.within the dom-module tag add the template tag and the script tag

![add template and script ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/5.png "add template and script")

5. In the script tag define a class with the name TodoListElement that extends the Polymer.Element

![add template and script ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/6.png "add template and script")

6. Add the static is method that returns the name of our element
![Add the static is method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/7.png "Add the static is method")

7. Add the static properties method that returns all the attributes of our element
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/8.png "Add the static properties method")
8. Let’s add a header to our element with the title My First todo list
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/9.png "Add the static properties method")
9. And now let’s add the line that define our element at the bottom of the script tag
window.customElements.define(TodoListElement.is, TodoListElement);
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/10.png "Add the static properties method")
10. Your new element should look like this by now
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/11.png "Add the static properties method")
11. Let’s use our new element in the polymer-codelab-app.html
12. Firstly import our new element
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/12.png "Add the static properties method")

``` WARNING: NEVER FORGET TO IMPORT AN ELEMENT BEFORE USING IT ```

13. Use it in the template of the polymer-codelab-app
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/13.png "Add the static properties method")

14. Use Polymer serve to serve our application
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/14.png "Add the static properties method")

15. The result should look like this
![Add the static properties method ](https://github.com/amandaSalander/bookworm-training-polymer2.0/blob/master/images/step_2/15.png "Add the static properties method")