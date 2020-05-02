@Library('jenkinsfile-shared-library') _

def config = readYaml text: """
  APP: 'Demo'
"""

config.keySet().each {
    env."${it}" = config[it]
}

"${pipelineSelector(env)}"(env)