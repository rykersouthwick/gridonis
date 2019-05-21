# Gridonis (experimental)
#### [Gridsome](https://gridsome.org/ "Gridsome") / [Adonis](https://adonisjs.com/ "Adonis") / [Apollo](https://www.apollographql.com/ "Apollo")

Gridonis is a new way to create full-stack progressive web apps. Front-end is staticly generated and can be deployed on a static host like [netlify](https://www.netlify.com/ "netlify") for free. Back-end uses the amazing [adonis framework](https://adonisjs.com/ "adonis framework") and can be deployed on a [vps](https://www.ssdnodes.com/manage/aff.php?aff=803 "vps").

### Get Up and Running in 5 Minutes 
1. Clone the repo
2. Run ``npm install`` in  /gridsome and /adonis folder.
3. Run ``adonis serve --dev`` inside /adonis folder
4. Run ``gridsome develop`` inside /gridsome folder
5. localhost:8080/__explore to make querys to apollo server from gridsome

### Gridsome plan
The plan for Gridonis is to fully integrate gridsome with apollo. 

### Current issues 
- [Generating static routes / templates from the remote graphql schema](https://github.com/gridsome/gridsome/issues/80 "Generating static routes from the remote graphql schema")

#### Credits
- Adonis Apollo GraphQL https://scotch.io/tutorials/build-a-graphql-server-with-apollo-server-and-adonisjs
- Gridsome Remote Apollo https://gist.github.com/jakedohm/e5736245f35e9b32b29733b2dd37d2c1
