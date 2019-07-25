pipeline{
	agent any
	parameters(
		[string(description: 'Select a unique name stack name', name: 'Stackname', trim: false)],
		[string(description: 'Select a region', name: 'Region', trim: false)],
		[string(description: 'Select a unique Bucket name', name: 'BucketName', trim: false)]
		 )
	stages{
	stage('Clone Repo') {
		steps {
			sh "export AWS_DEFAULT_REGION=us-east-1"
			sh "aws cloudformation create-stack --stack-name ${params.stackname} --template-body file://s3cft.json --region ${params.region} --parameters-overrides ParameterKey=LambdaSourceBucket,ParameterValue=fghjkl"
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
