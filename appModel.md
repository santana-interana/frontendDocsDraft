App State

The application state is instantiated in App.jsx and it defines model as UserInterfaceModel.defaultValue.



App.jsx

updateModel

```
onWhateverModelChange(whateverModel) {
    return this.updateModel({
        whateverModel,
    });
}
```

UserInterface.jsx
{onWhateverModelChange} = this.props;


