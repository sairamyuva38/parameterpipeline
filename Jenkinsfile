pipeline{
    agent any
    parameters{
        choice(name:'VERSION',choices:['1.0.1','1.3.4','1.6.7'],description:'')
        booleanParam(name:'executeTests',defaultValue:true,description:'')
    }
    stages{
        stage("built"){
            steps{
               echo "this is built application" 
            }
        }
        
        stage("test"){
            when{
                expression{
                    params.executeTests
                }
            }
            steps{
                echo "this is test application" 
            }
        }
        
        
        stage("deploy"){
            steps{
                 echo "deploying the application"
                 echo "deploying version ${params.VERSION }" 
            }
        }
        
    }
    
}
