  def setup_env(env_type) {
    echo "Read env & app config"
    echo "Configure environment"  
    echo "Get binaries from Artifact Repository"
    echo "Deploy binaries"
    echo "Smoke test"
  }
node {
  stage ('Commit') {
    echo "Read version control"
    echo "Compile"
    echo "Unit test"
    echo "Assemble"
    echo "Code Analysis"
    echo "Store reports, binaries and metdata to Artifact Repository"
  }
}
node {
  stage ('Acceptance') {
    setup_env('Acceptance')
    echo "Acceptance test"
    echo "Store reports and metadata to Artifact Repository"
  }
}
parallel (
    "stream 1" : { 
        node {
            stage ('Capacity test') {
                setup_env('Capacity')
                echo "Capacity test"
                echo "Store reports and metadata to Artifact Repository"
            }
        }
    },
    "stream 2" : {
        node {
            stage ('UAC test') {
                setup_env('UAC')
                echo "ready for manual tests"  
            }
        }
    }
)
