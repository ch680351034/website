pipeline{
    
    agent{
        label "test-node"
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }

         stage('application code containerlization') {
            steps {
               docker build -t websiteapp .
               docker run -d -p 8088:80 websiteapp
            }
        }

    }

    post{
        always{
            echo "pipeline has been ran"
        }
        
    }
}
