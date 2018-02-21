    pipeline {
            agent any

            stages {
                    stage('test') {
                            steps {
                                    sh 'echo hello'
                            }
                    }
                    stage('test1') {
                            steps {
                                    sh 'echo $TEST'
                            }
                    }
                    stage('test3') {
                            steps {
                                    script {
                                            if (env.BRANCH_NAME == 'master') {
                                                    echo 'Build'
													echo 'Deploy'
                                            }
											if (env.BRANCH_NAME == 'bugfix') {
                                                    echo 'Unit Test'
													echo 'Smoke Test'
                                            }
											if (env.BRANCH_NAME == 'feature') {
                                                    echo 'Unit Test'
													echo 'Integraton Test'
													echo 'Smoke Test'
                                            }
                                    }
                            }
                    }
            }
    }