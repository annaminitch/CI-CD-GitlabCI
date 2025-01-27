# CI-CD-GitlabCI
написание рабочего playbook

### Содержимое .gitlab-ci.yml

```yaml
stages:
  - build
  - test

build_job:
  stage: build
  tags:
    - netology
  script:
    - echo "Начало Building"
    - mkdir -p build
    - echo "Информация о сборке" > build/info.txt

test_job:
  stage: test
  tags:
    - netology
  script:
    - echo "Testing"
    - ls build/info.txt
