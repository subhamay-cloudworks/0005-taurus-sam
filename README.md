# Project Taurus : Lambda Layer Demo


## Description

This is demonstration of a creating a Lambda layer with a custom Python library and adding the same to a Lambda function. The entire stack is created using AWS SAM (Serverless Application Model) 


### Installing

* Clone the repository https://github.com/subhamay-cloudworks/0005-tarus-sam
* Create a S3 bucket to store the Lambda code zip file.
* Zip and Upload the following Python file  to taurus/code/python in the S3 bucket.
    * taurus_code.py (taurus_code.zip)
* From the Command line, zip the Python library code/python/my_lib.py including the python folder.
```
zip -r my_lib.zip python/my_lib.py
```
* Upload the file my_lib.zip to taurus/code/python in the S3 bucket.
* Execute the following SAM CLIcommands from the project directory to create the stack:
```
sam build
sam deploy --guided --capabilities "CAPABILITY_NAMED_IAM"
```

* To delete the stack either delete from CloudFormation console or execute the following command:
```
aws cloudformation delete-stack --stack-name <Stack Name> --region <AWS Region Name>
```

### Executing program

* Execute the Lambda function either from AWS Lambda console or AWS CLI.


## Help

Post message in my blog (https://blog.subhamay.com)


## Authors

Contributors names and contact info

Subhamay Bhattacharyya  - [subhamay.aws@gmail.com](https://blog.subhamay.com)

## Version History

* 0.1
    * Initial Release

## License

This project is licensed under Subhamay Bhattacharyya. All Rights Reserved.

