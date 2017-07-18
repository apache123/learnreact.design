---
layout: post
last-modified: '2017-06-20'

title: "Components, props, states"
subtitle: "React terms in plain English and doodles🌴🎄⚛"

excerpt: "React terms explained in plain English and doodles🌴🎄⚛"

author:
  name: Linton Ye
  twitter: lintonye
  bio: Freelance full-stack developer in BC Canada (GMT-8). Android, React Native, Node.js, MongoDB, PostgreSQL. <a href="mailto:linton@jimulabs.com">Contact me.</a>
  image: linton.jpg
---

_This series of posts will be the very first part of the ["React for Designers" course](http://learnreact.design) I'm creating. Be sure to [sign up](http://learnreact.design) to receive exclusive updates!_

- _[What is React?](/2017/06/08/what-is-react/)_
- _What is React Native? (/2017/06/20/what-is-react-native)_
- _React Native vs. Hybrids (coming soon)_
- _Components, props, state etc. (this post)_

---
<div>
  <HatSwitcher />
  <Thinker />
</div>

HatSwitcher: ...

Thinker:
  <div>
    <DomoInPose />
    <Hat />
  </div>

DomoInPose:
  <img ... />

Hat:
  <img ... />

DomoInPose:
  <img src="https://..." />


<div>
  <HatSwitcher />
  <Thinker hat={hat}/>
</div>

ThinkerBody:
  <img ... />

Hat:
  cap
    <img src="cap.png" />
  pirate
    <img src="pirate.png" />
  ...

- props: animation frames

- prop: just like the prop in html tag, it's the configuration of a component


- what are Components
- what are props
  - accessible via: `this.props`
  - read only
- what are states?
  - it is private and fully controlled by the component
  - respond to user input, a server request or the passage of time. For this you use state.
  - State allows you to dynamically change many elements at once based on one variable. State encompasses the key parts of your UI that change basic on user input.
  - is it a state? Minimize state
    - Is it passed in from a parent via props? If so, it probably isn't state.
    - Does it remain unchanged over time? If so, it probably isn't state.
    - Can you compute it based on any other state or props in your component? If so, it isn't state.
  - which component should hold the state?
    - This is often the most challenging part for newcomers to understand,
    - how to find where the state should live?
      - which components render according to the state?
      - find a common owner
      - the owner or its (grand)owner should hold the state
      - create a new component simply for holding the state if no common owner is found
- when to use props, when to use states?
- revisit Domo's hat
- Unidirectional dataflow?
- States are things that change -- but props change too?
- Try to keep as many of your components as possible stateless. By doing this you'll isolate the state to its most logical place and minimize redundancy, making it easier to reason about your application.


<a name="learning-goals">

# Learning Goals

<a name="endofpost">
