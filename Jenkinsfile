node {
  stage ('Commit') {
    echo "Read version control"
    echo "Compile"
    echo "Unit test"
    echo "Assemble"
    echo "Code Analysis"
    echo "Store reports, binaries and metdata to Artifact Repository"
  }
  stage ('Acceptance') {
    echo "Read env & app config"
    echo "Configure environment"  
    echo "Get binaries from Artifact Repository"
    echo "Deploy binaries"
    echo "Smoke test"
    echo "Acceptance test"
    echo "Store reports and metadata to Artifact Repository"
  }
  stage ('Capacity test') {
    echo "Read env & app config"
    echo "Configure environment"  
    echo "Get binaries from Artifact Repository"
    echo "Deploy binaries"
    echo "Smoke test"
    echo "Capacity test"
    echo "Store reports and metadata to Artifact Repository"
 }
}
