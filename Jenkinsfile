@Library('jenkinsfile-shared-library') _

def config = readYaml text: """
  APP: 'Demo'
  VERSION: 'v2'
"""

config.keySet().each {
    env."${it}" = config[it]
}

"${pipelineSelector(env)}"(env)