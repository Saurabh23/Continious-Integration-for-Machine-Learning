def gitCommit() {
    sh "git rev-parse HEAD > GIT_COMMIT"
def gitCommit = readFile('GIT_COMMIT').trim()
    sh "rm -f GIT_COMMIT"
    return gitCommit
}

node {
    // Checkout source code from Git
    stage 'Checkout'
    //sh "python3 -m pip freeze"
    
    
    checkout scm

    // Build Docker image
   stage 'Train Model(s)'
   echo "$path" 
    
   echo 'Test accuracy and measure inference time.'
     

   //sh 'python --version'
   sh 'python3 --version' 
   
   //sh 'python3 wine_mlflow.py 0.11 0.10'
   
   sh 'sleep 10'

  stage 'Optimize Model(s)'
  echo 'Test accuracy and measure inference time.'
  sh 'sleep 5'

  // Test
  stage 'Test' 
  echo 'Test accuracy and measure inference time.'

  // Test
  stage 'Build Serving container'
  echo 'Build TensorFlow Serving Container.'
  //sh 'git clone https://github.com/mlflow/mlflow-example'
  sh 'cd mlflow-example/'
  //sh 'ls'
  //sh 'git clone https://github.com/mlflow/mlflow-example'
  
  
  
  
  sh 'python3 /home/sgawande/Documents/ci/mlflow/mlflow-example/train.py 0.43'
    //deploy to port 1235
  //sh 'python3 -m pip install mlflow'
  //sh 'mlflow pyfunc serve /var/lib/jenkins/workspace/ML Pipeline2/mlruns/0/9abd56d09e7740ff847f8de0fcdbac44/artifacts/model$  -p 1235'
  //sh "curl -X POST -H "Content-Type:application/json; format=pandas-split" --data [[1.8, 0.029, 0.48, 0.98, 0.2, 01, 0.33, 0.2, 0.01, 1, 0.11]]} http://127.0.0.1:1238/invocations"
}
