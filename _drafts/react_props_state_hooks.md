# React and Hooks

## Components is an isolated piece of interface. A blog website has sidebar and list of posts. Each post and list of posts are components. They are composed of other components.
Functional and Class components are there, first one is popular.

Example functional component:
```const BlogPostExcerpt = () => {
  return (
    <div>
      <h1>Title</h1>
      <p>Description</p>
    </div>
  )
}	 
```
Class based component
```
import React, { Component } from "react"

class BlogPostExcerpt extends Component {
  render() {
    return (
      <div>
        <h1>Title</h1>
        <p>Description</p>
      </div>
    )
  }
}

## Props They are way to pass properties to components from top component to its every child.
```
const BlogPostExcerpt = props => {
  return (
    <div>
      <h1>{props.title}</h1>
      <p>{props.description}</p>
    </div>
  )
}
```

We can pass props in similar to HTML ATTRIBUTES, when we initialize it.
```
const desc = 'A description'
//...
<BlogPostExcerpt title="A blog post" description={desc} />
```
### Children : A special prop. any value passed to body like something here
```
<BlogPostExcerpt title="A blog post" description="{desc}">
  Something
</BlogPostExcerpt>
```
```<ChildComponent />
<ChildComponent color=green />
class ChildComponent = props => {
  console.log(props.color)
}```
## State Management
useState(0)
and useEffect(); 
```useEffect(() => {
  getData()
})```
We can add into that array a list of variables,
```
We can add into that array a list of variables,
```
let name, address

useEffect(() => {
  getData()
}, [name, address])```
