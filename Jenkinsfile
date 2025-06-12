pipeline {
    agent any
    environment {
        REST_ENDPOINT = 'https://pkc-ldvr1.asia-southeast1.gcp.confluent.cloud:443' // Replace with your actual REST endpoint
        SCHEMA_REGISTRY_URL = 'https://psrc-qzvrm.asia-southeast1.gcp.confluent.cloud'
        API_KEY = credentials('BASE64_API_KEY')
        SCHEMA_API_KEY = credentials('BASE64_SCHEMA_API_KEY')
        CLUSTER_ID = 'lkc-yjvgnk' // replace with your cluster 
    }
    parameters {
        text(name: 'message', defaultValue: '''{
   "topic": "default-name",
   "message": [
      { 
         "key" : "kfg-106",
         "value" : "2"
      },
      { 
         "key" : "fkd-258",
         "value" : "6"
      }
   ]
}''', description: 'Produce all the message from json format')
    }
    stages {
        stage('Set Parameters') {
            steps {
                script {
                    env.MESSAGE_JSON = params['message']
                }
            }
        }
        
        stage('Produce') {
            steps {
                echo 'Produce $MESSAGE_JSON'
            }
        }
    }
}
