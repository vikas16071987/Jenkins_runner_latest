pipeline{

    agent any

<<<<<<< HEAD
    parameters {
        choice choices: ['chrome', 'firefox'], description: 'Select the browser', name: 'BROWSER'
    }

=======
>>>>>>> a4e6dbc (test-suite.yaml)
    stages{

        stage('Start Grid'){
            steps{
<<<<<<< HEAD
                sh "docker-compose -f grid.yaml up --scale ${params.BROWSER}=2 -d"
=======
                sh "docker-compose -f grid.yaml up -d"
>>>>>>> a4e6dbc (test-suite.yaml)
            }
        }

        stage('Run Test'){
            steps{
                sh "docker-compose -f test-suites.yaml up --pull=always"
<<<<<<< HEAD
                script {
                    if(fileExists('output/flight-reservation/testng-failed.xml') || fileExists('output/vendor-portal/testng-failed.xml')){
                        error('failed tests found')
                    }
                }
=======
>>>>>>> a4e6dbc (test-suite.yaml)
            }
        }

    }

    post {
        always {
            sh "docker-compose -f grid.yaml down"
            sh "docker-compose -f test-suites.yaml down"
            archiveArtifacts artifacts: 'output/flight-reservation/emailable-report.html', followSymlinks: false
            archiveArtifacts artifacts: 'output/vendor-portal/emailable-report.html', followSymlinks: false
        }
    }

}