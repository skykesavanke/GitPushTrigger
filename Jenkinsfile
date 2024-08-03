pipeline{
    agent any

    environment{
         Git_Repo='https://github.com/skykesavanke/GitPushTrigger.git'
         Branch_One='main'
         Branch_two='develop'
    }

    stages{
        stage('checkout from first branch'){
            steps{
                script{
                    git branch :${env.Branch_One} , url:${env.Git_Repo}
                }
            }
        }

        
        stage('checkout from second branch'){
            steps{
                script{
                    git branch :${env.Branch_Two} , url:${env.Git_Repo}
                }
            }
        }


        }
    }




//pipeline {
    // agent any

    // environment {
    //     GIT_REPO = 'https://github.com/your-repo.git'
    //     BRANCH_ONE = 'branch-one'
    //     BRANCH_TWO = 'branch-two'
    //     TARGET_BRANCH = 'target-branch'
    // }

    // stages {
    //     stage('Checkout Branch One') {
    //         steps {
    //             script {
    //                 git branch: "${env.BRANCH_ONE}", url: "${env.GIT_REPO}"
    //             }
    //         }
    //     }
        
    //     stage('Checkout Branch Two') {
    //         steps {
    //             script {
    //                 git branch: "${env.BRANCH_TWO}", url: "${env.GIT_REPO}"
    //             }
    //         }
    //     }

    //     stage('Merge Branches') {
    //         steps {
    //             script {
    //                 sh """
    //                     git config user.name "your-username"
    //                     git config user.email "your-email@example.com"
    //                     git checkout ${env.TARGET_BRANCH}
    //                     git pull origin ${env.TARGET_BRANCH}
    //                     git merge ${env.BRANCH_ONE}
    //                     git merge ${env.BRANCH_TWO}
    //                 """
    //             }
    //         }
    //     }

    //     stage('Push to Target Branch') {
    //         steps {
    //             script {
    //                 withCredentials([usernamePassword(credentialsId: 'your-credentials-id', passwordVariable: 'GIT_PASSWORD', usernameVariable: 'GIT_USERNAME')]) {
    //                     sh """
    //                         git push https://${GIT_USERNAME}:${GIT_PASSWORD}@github.com/your-repo.git ${env.TARGET_BRANCH}
    //                     """
    //                 }
    //             }
    //         }
    //     }
    // }

    // post {
    //     success {
    //         echo 'Pipeline completed successfully!'
    //     }
    //     failure {
    //         echo 'Pipeline failed!'
    //     }
    // }
//}
