pipeline {
    agent {label "linux"} 
    stages {
        stage('build only on main branch') {
            when{
                branch "main"
            }
            steps {
               echo "Hello micro 1" 
            }
        }
        stage("run on branch that begins with change-"){
            when{
                branch "change-*"
            }
            steps{
               sh ``` 
                cat README.md 
                ```
            }
        }
    }
}
