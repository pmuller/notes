# AWS EC2

## Find the latest Amazon Linux AMI for ARM64/Graviton

```bash
aws ec2 describe-images \
   --owners amazon \
   --filters "Name=name,Values=amzn2-ami-hvm-2.0.*-arm64-gp2" "Name=state,Values=available" \
   --query "Images | sort_by(@, &CreationDate) | [-1].[ImageId]" \
   --output text
```
