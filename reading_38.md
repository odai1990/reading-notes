# Read 37

## React.js 2
[React - Conditional Rendering](https://reactjs.org/docs/conditional-rendering.html)

React - Lists & Keys

React - Forms

React - Lifting State

React - Composition vs Inheritance

Thinking in React

[React - Comprehensive Guide](https://ui.dev/reactjs-tutorial-a-comprehensive-guide-to-building-apps-with-react/)


- JSX — Allows us to write HTML like syntax which gets
transformed to lightweightJavaScript objects.

- Virtual DOM — A JavaScript representation of the actual
DOM.

- React.Component — The way in which you create a new component.

- render (method) — Describes what the UI will look like for
the particular component.

- ReactDOM.render — Renders a React component to a DOM node.

- state — The internal data store (object) of a component.

- constructor (this.state) - The way in which you establish
the initial state of a component.

- setState — A helper method used for updating the state of a component and re-rendering the UI

- props — The data which is passed to the child component
from the parent component.

- propTypes — Allows you to control the presence, or types of certain props passed to the child component.

- defaultProps — Allows you to set default props for your component.

- Component LifeCycle
  - componentDidMount — Fired after the component mounted
  - componentWillUnmount — Fired before the component will unmount
  - getDerivedStateFromProps - Fired when the component mounts and whenever the props change. Used to update the state of a component when its props change

- Events
  - onClick
  - onSubmit
  - onChange


```
class HelloUser extends React.Component {
  constructor(props) {
    super(props)

    this.state = {
      username: 'tylermcginnis'
    }

    this.handleChange = this.handleChange.bind(this)
  }
  handleChange (e) {
    this.setState({
      username: e.target.value
    })
  }
  render() {
    return (
      <div>
        Hello {this.state.username} <br />
        Change Name:
        <input
          type="text"
          value={this.state.username}
          onChange={this.handleChange}
        />
      </div>
    )
  }
}
```

```
class AddFriend extends React.Component {
  constructor(props) {
    super(props)

    this.state = {
      newFriend: ''
    }

    this.updateNewFriend = this.updateNewFriend.bind(this)
    this.handleAddNew = this.handleAddNew.bind(this)
  }
  updateNewFriend(e) {
    this.setState({
      newFriend: e.target.value
    })
  }
  handleAddNew() {
    this.props.addNew(this.state.newFriend)
    this.setState({
      newFriend: ''
    })
  }
  render() {
    return (
      <div>
        <input
          type="text"
          value={this.state.newFriend}
          onChange={this.updateNewFriend}
        />
        <button onClick={this.handleAddNew}> Add Friend </button>
      </div>
    )
  }
}
class ShowList extends React.Component {
  render() {
    return (
      <div>
        <h3> Friends </h3>
        <ul>
          {this.props.names.map((friend) => {
            return <li> {friend} </li>
          })}
        </ul>
      </div>
    )
  }
}
```

