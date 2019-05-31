pipeline {
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
                                steps {
                                        echo " hello"
                        }
                }
}