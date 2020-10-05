# Building a pipeline for test and production stacks
* Original - https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline-basic-walkthrough.html
* Remove WordPress specific configuration. This pipeline create just simple web server.

## How to deploy
1. Modify parameter file (*.json)
* KeyName = KeyPair name you have

2. Zip your artifacts
* zip website-single-instance.zip website-single-instance.yaml prod-stack-configuration.json test-stack-configuration.json

3. Upload zip to your bucket

4. Create pipeline stack with basic-pipeline.yaml
* Specify parameters suitable for your environment
  * Email required

5. Trigger your pipeline
