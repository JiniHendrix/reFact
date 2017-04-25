# reFact
React component performance optimizer

ReFact parses through your React components and tells you what components can be refactored into either Pure Components or Stateless Functional Components for performance boosts.

How to use:
npm install refact --save-dev
or 
yarn add -D refact

Then in CLI use command
refact path_to_component_directory

How it works:
Node fs to read each file, then check for lifecycle methods. If none are present and it's not a Stateless Functional Component ie React.Component is present, log that User should change it to a Stateless Functional Component

What about Pure Components?
Might need to use enzyme or something to mount components and test them for different results?
Should I just do both at the same time?
Idea 2: Replace React.Component with React.PureComponent and check if any errors are thrown?


I'm not too worried about performance as it's something users will run once or twice to check if they need to convert.