version 2.1

orbs:
 node: circleci/node@4.7.0
jobs:
  build:
   excutor:
    name: node/default
  tag: '10.4'
  steps:
   - checkout
   - node/with -cache:
      steps:
        - run: npm install
     -run: npm run test   
