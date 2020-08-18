# Push ECR Action

![GitHub](https://img.shields.io/github/license/hands-lab/push-ecr-action)

Push Docker or OCI image to AWS ECR

<!-- TOC depthFrom:2 -->

- [Feature](#feature)
- [Usage](#usage)
- [Inputs](#inputs)

<!-- /TOC -->

## Feature

- Login AWS ECR
- Change image tag
  - Add AWS ECR registry to the beginning of the image name
- Push Docker or OCI image

## Usage

```yaml
steps:
  - uses: hands-lab/push-ecr-action@v1
    with:
      image: demo
      aws-access-key-id: ${{ secret.AWS_ACCESS_KEY_ID }}
      aws-secret-access-key: ${{ secret.AWS_SECRET_ACCESS_KEY }}
      aws-region: ${{ secret.AWS_REGION }}
      aws-account-id: ${{ secret.AWS_ACCOUNT_ID }}
```

## Inputs

|Name|Type|Required|Default|Description|
|:--:|:--:|:--:|:--:|:--|
|image|string|true||image name|
|aws-access-key-id|string|true||AWS Access Key ID|
|aws-secret-access-key|string|true||AWS Secret Access Key|
|aws-region|string|true||AWS Region|
|aws-account-id|string|true||AWS Account ID|
