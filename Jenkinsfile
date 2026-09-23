pipeline {
agent any
stages{
stage('Hello World'){
steps{
echo 'Hello World from Jenkins Pipeline'
sh 'mkdir -p build && echo "Build successfull" > build/hello.txt'
}
}
}
post{
success{
archiveArtifacts artifacts: 'build/hello.txt',fingerprint: true
}
}
}
