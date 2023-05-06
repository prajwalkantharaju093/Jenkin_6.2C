pipeline{
agent any
stages {
    stage('Build'){
    steps{
        echo "Build the code using maven and to compile and package code."
    }
    post{
        always{echo "always"}
    success{ 
        emailext attachLog: true, body: "Build success", subject: "Build status", to: "prajwalk930@gmail.com"
    }
failure{echo "Sorry failed"
       mail to: "prajwalkantharaju@gmail.com",
      subject: "Build status",
      body: "Build Fail"
       }}}
    
// stage('Unit and Integration Tests'){
//     steps{
//         echo "running unit tests using selenium" 
//         echo "running integration tests using selenium"
//     }
// }

// stage('Code Analysis'){
//     steps{
//         echo "check the quality of the code as per industry standards using CheckStyle"
//     }
// }

// stage('Security Scan'){
//     steps{
//         echo "performing a security scan on the code using a tool to identify any vulnerabilities using Acunetix"
//     }
//     post{
//     success{ 
//       mail to: "prajwalkantharaju@gmail.com",
//       subject: "Scan status",
//       body: "Scan completed no errors"}
// failure{echo "Sorry failed"
//        mail to: "prajwalkantharaju@gmail.com",
//       subject: "Scan status",
//            body: "Scan failure"}}}
        
// stage('Deploy to staging'){
//     steps{
//         echo "deploy the application to a staging server AWS EC2 instance server"
//     }
// }

// stage('Integration Tests on Staging'){
//     steps{
//         echo "testing on staging environment using selenium"
//     }
//     post{
//     success{ 
//       mail to: "prajwalkantharaju@gmail.com",
//       subject: "Test status",
//       body: "success"}
// failure{echo "Sorry failed"
//        mail to: "prajwalkantharaju@gmail.com",
//       subject: "Test status",
//            body: "Fail"}}
// }

// stage('Deploy to Production'){
//     steps{
//         echo "deploy the application to a production server AWS EC2 instance server"
//     }
// }
}
}
