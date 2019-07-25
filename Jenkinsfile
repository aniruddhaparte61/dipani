pipeline{
	agent any
	stages{
	stage('Clone Repo') {
		steps {
			sh "export AWS_DEFAULT_REGION=us-east-1"
			sh "aws cloudformation create-stack --stack-name ${params.stackname} --template-body file://s3anicft.json --region ${params.region} --parameters params.json
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
