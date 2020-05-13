@Library('jenkinsfile-shared-library') _

def config = readYaml text: """
  APP: 'Demo'
  VERSION: 'v2'
  DOCKER_IMAGE: 'manu756/app_for_demo'
  DOCKERFILE_LOCATION: 'app/.'
"""

config.keySet().each {
    env."${it}" = config[it]
}

"${pipelineSelector(env)}"(env)