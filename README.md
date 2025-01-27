# CI-CD-GitlabCI
написание рабочего playbook

### Содержимое .gitlab-ci.yml

```yaml
stages:
  - build
  - test

build:
  stage: build
  tags:
    - netology
  script:
    - echo "Начало Building"
    - mkdir -p build
    - touch build/info.txt

test:
  stage: test
  tags:
    - netology
  script:
    - echo "Testing"
    - ls build/info.txt
