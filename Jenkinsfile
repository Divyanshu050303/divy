pipeline {
    agent any 
            stages{
                stage('One'){
                    steps{
                        echo 'Hi, this is divyanshu singh from sasni'
                    }
                }
                stage('Two'){
                    steps{
                        input('do you wnat to proceed?')
                    }
                }
                stage('Three'){
                    when{
                        not{
                            branch 'master'
                        }
                    }
                    steps{
                        echo 'hello'
                    }
                }
                stage('Four'){
                    parallel{
                        stage('Unit Test'){
                            steps{
                                echo "Running the unit test..."
                            }
                        }
                        stage('Integration test'){
                            steps{
                                echo 'Running the integration test...'
                            }
                        }
                    }
                }
            }
}
