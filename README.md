version: 2
jobs:
  one:
    docker:
      - image: cimg/ruby:2.6.8
        auth:
          username: mydockerhub-user
          password: $DOCKERHUB_PASSWORD
    steps:
      - checkout 
      - run: echo "A first hello"
      - run: sleep 25
  two:
     docker:
       - image: cimg/ruby:3.0.2
         auth:
