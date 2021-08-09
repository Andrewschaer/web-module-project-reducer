# Understanding Questions:
1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code excutes for each step.
* The user presses the 1 button.
* onClick property runs the handleAddOne function it is assigned to
* dispatch (within handleAddOne) references the addOne action function from the actions index file, which provides the action type for the dispatch to properly work with the reducer to locate which action should be run - in this case, that being the ADD_ONE action.
* The ADD_ONE action reads in the current state and returns an state with an updated total (with 1 being added)
* Dispatch receives this update in state, causing the page to rerender
* Display total reads the updated state.total and displays this to the user
...

* TotalDisplay shows the total plus 1.
