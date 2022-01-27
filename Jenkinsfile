pipeline{
        agent any
        stages{
            stage('Make Directory'){
                steps{
                    sh "mkdir ~/jenkins-tutorial-test"
                }
            }
            stage('Make Files'){
                steps{
                    sh "touch ~/jenkins-tutorial-test/file1 ~/jenkins-tutorial-test/file2"
                }
            }
             stage('Archive'){
                steps{
                    dir('/home/jenkins/jenkins-tutorial-test') {
                        sh "zip archive.zip file*"
                        archiveArtifacts artifacts: 'archive.zip', followSymlinks: false
                }
            }         
        }
     }
}
