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

"""for(int i=1; i < 5; i++){
     println i
 }
if( i == 4) {
    print "this is the number i am looking for"
} else{
    print "this is what i am not looking for"
}"""

string stars = ''
for (int i = 0; i < 5; i++) {
    stars = stars + "* "
    println stars
}