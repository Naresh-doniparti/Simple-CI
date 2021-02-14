Simple CI Pipleline with GIT, GITHUB and Jenkins

A simple pipeline which fetches 

Challenges faced:
Jenkins build is failing while running the maven command due to missing execution priviliges on the file. Used the below command to solve it
  -  git update-index --chmod=+x mvnw


For making github web hooks to work, the pipeline has to be available publicly. Since, I have a local setup, I have used ngrok to make my local jenkins publicly available.
  - Steps for making the jenkins publicly available
      1. Install ngrok, Register to it.
      2. Run the below command to mark a port and protocol to be publicly available
      ./ngrok http 8081
