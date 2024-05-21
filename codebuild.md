# AWS CodeBuild

## Find AmazonLinux 2023 images for aarch64

```shell
$ aws --region ap-southeast-1 codebuild list-curated-environment-images | \
   jq '.platforms[].languages[] | select(.language == "STANDARD") | .images[] | select(.description | contains("Amazon Linux 2023") and contains("aarch64"))'
{
  "name": "aws/codebuild/amazonlinux2-aarch64-standard:3.0",
  "description": "AWS CodeBuild - Docker image based on Amazon Linux 2023 (aarch64) with multiple language support",
  "versions": [
    "aws/codebuild/amazonlinux2-aarch64-standard:3.0-23.04.25",
    "aws/codebuild/amazonlinux2-aarch64-standard:3.0-24.01.29",
    "aws/codebuild/amazonlinux2-aarch64-standard:3.0-24.03.06",
    "aws/codebuild/amazonlinux2-aarch64-standard:3.0-24.03.21"
  ]
}
```
