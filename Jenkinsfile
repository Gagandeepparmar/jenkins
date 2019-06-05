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

                        stage('pythondownloadtest') {
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

    for (int i = 0; i < list.size(); i++) {
        sh "echo Hello ${list[i]}"
    }

