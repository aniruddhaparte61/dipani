pipeline{
	agent any
	stages{
	  parameters {
       		string(name: 'Stackname', description: 'Enter Stack Name')
		
		string(name: 'Region', description: 'Enter Region')
		
		string(name: 'Bucketname', description: 'Enter Your Bucket Name')

    }
	stage('Clone Repo') {
		steps {
			sh "export AWS_DEFAULT_REGION=us-east-1"
			sh "aws cloudformation create-stack --stack-name ${params.Stackname} --template-body file://s3cft.json --region ${params.Region} --parameters ParameterKey='LambdaFunctionName',ParameterValue=${params.Bucketname}" 
			}
	}
		stage('Test'){
			steps{
				sh "ls"
			}
		}
		stage('Deploy'){
			steps{
				sh "ls"
			}
		}
	
	}
}
