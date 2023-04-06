#!/bin/bash

# Установите AWS CLI
pip install awscli --upgrade --user

# Получите код из репозитория
git clone https://github.com/ваш-репозиторий.git

# Загрузите файлы в S3
aws s3 sync . s3://ваш-bucket
