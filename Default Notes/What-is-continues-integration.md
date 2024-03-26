WHat is continues integration in Devops??
 Continues integration is an automated process in devops, which generates software and its features quickly and efficiently.

 Example.
 Devlopers writes several lines of codes while creating a software, working in a team its an ideal practice to store the code in a centeralized space.

 This centeralized repository is called  as version control system like github.
 Every day developer push and pull the code from the repository several time a day.
 Code changes /commit happened continuesly.

 Commited code will be moved to build servers where
  on code server this code will be 
  build
  tested and 
  evaluated

  which generated the artifact
  artifact willbe stored on the artifact repository
  from repository it'll be moved to server for further testing
  here tester conduct testing after tester approved it ,it’ll move to deployment server.


  To avoid bugs conflict build failure the problem should be detected much earlier.

  # What is continuess Process
    For every commit  there should be continuous process of building,testing.
    So when the devlopers commit the code an automated process fetch the code build it test it evaluate it if failurte occurs devs are notified, if build test passed artifact will bestored in a artifact repostoty.
     This automation process is called a continuess integration.
     the goal of CI is to detedct  any issue early so that fix can be done quickly