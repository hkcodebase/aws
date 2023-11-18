# AWS Commands

### List aws cli credentials 
```
cat ~/.aws/credentials
```

### List aws config 
```
cat ~/.aws/config
```

### Configure new profile 
```
aws configure --profile aws-profile-hemant-hkpt
```

### Get session token (while using MFA)
```
aws sts get-session-token
```

### List iam users
```
aws iam list-users
```

### List iam users using profile
```
aws iam list-users --profile [profileName]
```

### S3 Commands
```
aws s3api create-bucket \
    --bucket user-alert-bucket \
    --region us-east-1

aws s3api put-object --bucket user-alert-bucket --key initial-alert-registration-success --body user-registered-alert.html

aws s3 ls --bucket user-alert-bucket
```