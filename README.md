# docker-sample-pj

## imageの作成
`$ docker build -t hello-world .`
Issueにlog記載

## ECSにpush
`$ aws ecr create-repository --repository-name sawa-test`
`$ docker tag hello-world aws_account_id.dkr.ecr.us-east-1.amazonaws.com/sawa-test`
`$ aws ecr get-login --no-include-email`
`$ docker login -u AWS -p {token}`
`$ docker push aws_account_id.dkr.ecr.us-east-1.amazonaws.com/hello-world
