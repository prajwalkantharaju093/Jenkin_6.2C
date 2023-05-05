pipeline{
agent any
environment {NAME = "Prajwal K" 
DIRECTORY_PATH="path_URL"
TESTING_ENVIRONMENT="Luna"
PRODUCTION_ENVIRONMENT ="Airavata"
}
stages {
    stage('Build'){
    steps{
        echo "fetch the source code from the directory path $DIRECTORY_PATH"
echo "compile the code and generate any necessary artifacts"
    }
    post{
        always{echo "always"}
    success{ 
      mail to: "prajwalkantharaju@gmail.com",
      subject: "Build status",
      body: "Build success"}
failure{echo "Sorry failed"}}}

stage('Test'){
    steps{
        echo "unit tests" 
        echo "integration tests"
    }
}

stage('Code Quality Check'){
    steps{
        echo "check the quality of the code"
    }
}

stage('Deploy'){
    steps{
        echo "Deploy to $TESTING_ENVIRONMENT Successfull"
    }
}

stage('Approval'){
    steps{
        sleep 10
    }
}

stage('Deploy to Production'){
    steps{
        echo "Deploy to $PRODUCTION_ENVIRONMENT successfull"
    }
}
}
}
