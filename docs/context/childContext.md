## @childContext(childContext: Object)

Defines the result of component's [getChildContext](https://facebook.github.io/react/docs/context.html).

#### Example

```js
@childContext({
  theme: {
    primaryColor: 'blue',
    secondaryColor: 'green',
  },
})
class ThemeProvider extends React.Component {

  static contextTypes = {
    theme: PropTypes.object,
  }

  // needed to avoid readonly exception
  getChildContext() {}

  render() {
    return (
      <div>
        {this.props.children}
      </div>
    );
  }
}
```
