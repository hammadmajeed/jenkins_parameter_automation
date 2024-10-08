pipeline{
    agent any
    parameters{
        string(name: 'VERSION', defaultValue: '1.0', description: 'added for demo to the class')
        choice(name: 'BUILD_VERSION', choices:['1.0','1.1','1.2'], description: 'this is drop down list')
        booleanParam(name: 'DEPLOY', defaultValue: true, description: 'added to enable or disable test cases')
    }
    stages{
        stage('Build'){
            steps{
                echo 'Building the project'
            }
        }
        stage('Test'){
            steps{
                echo 'Testing the project'
            }
        }
        stage('Deploy'){
            when{
                expression{
                    return params.DEPLOY == true
                }
            }
            steps{
                echo 'Deploying the project'
            }
        }
    }
}
