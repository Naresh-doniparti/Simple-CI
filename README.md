Simple CI Pipleline with GIT, GITHUB and Jenkins

Jenkinsfile - A simple pipeline which pulls the latest code from the GIT
              with maven CLI, it executes tests and package the application into a .jar file

Challenges faced:
Jenkins build was failing while running the maven command. It was due to missing execution priviliges on the file. Used the below command to solve it
  -  git update-index --chmod=+x mvnw


For github web hooks to work, the jenkins pipeline has to be available publicly. Since, I have a local setup, I have used ngrok to make my local jenkins publicly available.
  - Steps for that:
      1. Install ngrok, Register to it.
      2. Run the below command to mark a port and protocol to be publicly available
      ./ngrok http 8081
