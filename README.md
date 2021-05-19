**AWS CloudFront Cache Invalidation**

1. Create a Lambda function with Python 3.8 runtime
2. Upload/paste in the python function and deploy
3. Give the function role the following permissions:
   * `cloudfront:CreateInvalidation`
   * `codepipeline:PutJobSuccessResult`
   * `codepipeline:PutJobFailureResult`
4. Add as an AWS Lambda action to the relevant stage of the CodePipeline
5. Within the action set `UserParameters` to the CloudFront Distribution ID
