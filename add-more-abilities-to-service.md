# Add more abilities to service

In this chapter, we'll improve our service by adding more abilities.

First, lets open our app's service file, which is available at `app/todo-list.service.ts`.

There we'll add a new method to the service, called `addItem`, like so:
```ts
addItem(item): void { 
    this.todoList.push( item );
}
```

This will allow us to call the same method from everywhere across the application, thus making our app easier to maintain.

And now we can change our code in `app/list-manager/list-manager.component.ts` to call the `addItem` method directly from the service like so:

```javascript
addItem(item): void {
    this.todoListService.addItem(item);
}
```

- There may be additional logic when calling these methods, i.e. saving the changes in a database (which we'll implement later).
- A better way to handle data is using *immutable objects*, but that's a bigger topic than we can cover in this tutorial at the moment.

