pipeline {

    agent {

        node {

            label 'master'

        }

    }



    stages {



        stage('terraform intro') {

            steps {

                sh 'echo "Hakuna Matata" '

            }

        }

        stage('git clone') {

            steps {

                sh 'sudo rm -r *;sudo https://github.com/satyamuralidhar/tf-integrate.git'

            }

        }

        stage('tfsvars create'){

            steps {

                sh 'sudo cp /home/ubuntu/terraform/vars.tf ./jenkins/'

            }

        }

        stage('terraform init') {

            steps {

                sh 'sudo /home/ubuntu/terraform/terraform init ./jenkins'

            }

        }

        stage('terraform plan') {

            steps {

                sh 'ls ./jenkins; sudo /home/ubuntu/terraform/terraform plan ./jenkins'

            }

        }

        stage('terraform The End') {

            steps {

                sh 'echo "simba roar"'

            }

        }



        

    }

}
