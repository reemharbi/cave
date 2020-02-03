# SuperSquad - Redux

## The store 
allowed us to represent the list of characters and selected heroes in one overall object. Ultimately, every component that needs to has access to this store, through the react-redux **connect** function.

## The action creators 
included **addCharacterById** and **removeCharacterById**. They returned actions - objects with a type, and data for the reducers to handle.

## Reducers 
provided guidelines on how to add and remove characters to the store. It did so by returning new instances of both the characters and heroes array through different **action.type** cases.

## MapStateToProps 
the first parameter of the connect function, described what parts of the redux store to make **accessible** within the component’s props object.

## MapDispatchToProps 
the second parameter of the connect function, described what **action creators to bind** to the component’s props object.
