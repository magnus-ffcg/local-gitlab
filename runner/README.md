# Gitlab-runner

## Create or edit a group in gitlab-ui and create a runner 

* Create or edit a group
* Click build / runners under the group
* Register a runner with a tag
* Copy token from output and append it below

## Start runner

TOKEN=[TOKEN FROM UI] docker-compose up -d

## Create a project (repo) and build

* Create a blank project within your group
* Go to build and pipeline editor and add a pipeline
* Add same tag as you added when registered the runner by
  adding the following on top:
  
  ```yaml
  default:
    tags:
      - your_tag
  ```

* Click commit.
* It will now start building.
* Click on build / pipelines

