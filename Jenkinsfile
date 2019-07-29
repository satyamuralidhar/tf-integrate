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
        stage('git ') {

            steps {

               sh label: '', script: 'cd /home/ubuntu'

            }

        }

        stage('git clone') {

            steps {

                 sh label: '', script: 'sudo git clone https://github.com/satyamuralidhar/tf-integrate.git'

            }

        }

        stage('tfsvars create'){

            steps {

                 sh label: '', script: 'sudo cp /home/ubuntu/terraform/vars.tf ./jenkins/'

            }

        }

        stage('terraform init') {

            steps {

                sh label: '', script: 'sudo /home/ubuntu/terraform/terraform init ./jenkins'

            }

        }

        stage('terraform plan') {

            steps {

                 sh label: '', script: 'ls ./jenkins; sudo /home/ubuntu/terraform/terraform plan ./jenkins'

            }

        }

        stage('terraform The End') {

            steps {

                 sh label: '', script: 'echo "simba roar"'

            }

        }



        

    }

}
