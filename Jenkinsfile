"""pipeline {
        agent any
                stages {
                        stage('One') {
                                steps {
                                        echo 'hi this is gagandeep'
                                       }
                        }
                        stage ('two') {
                                steps {
                                        input('do you want to proceed?')

                                }
                        }
                        stage('Three'){
                                when {
                                      not {
                                                branch "master"
                                      }
                                }
                                steps {
                                        echo " hello"
                                }
                        }
                        stage('four for parallel example') {
                                                               parallel {
                                                                     stage('unit test') {
                                                                                        steps {
                                                                                                echo "Running the unit test"
                                                                                        }
                                                                     }
                                                                     stage('Integration test') {
                                                                                        agent {
                                                                                                docker {
                                                                                                        reuseNode false
                                                                                                        image 'ubuntu'
                                                                                                }
                                                                                        }

                                                                                        steps {
                                                                                                echo ' Running the integration testing'
                                                                                              }
                                                                     }
                                                               }
                        }

                        stage('pythoncreating_an_image') {
                                agent {
                                        docker {
                                                reuseNode false
                                                image 'python'
                                        }
                                }
                                steps {
                                        echo ' Running the integration testing'
                                         }
                        }
                }
}"""

"""for(int i=1; i < 5; i++){
     println i
 }
    if( i == 4) {
        println "this is the number i am looking for"
}   else{
        println "this is what i am not looking for"
}"""

"""string stars = ''
for (int i = 0; i < 5; i++) {
    stars = stars + "* "
    println stars
}"""

"""pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 3000:3000 -p 5000:5000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}"""



pipeline {
agent any
stages {
    stage('build') {
        agent any
        steps {
            script {
                showMavenVersion('mvn version')
            }
        }
    }
}

}

def showMavenVersion(String a) {
        bat 'mvn -v'
        echo a
}