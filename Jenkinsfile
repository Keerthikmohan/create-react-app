pipeline{
agent any 
stages{
stage ('source code')
 {
steps {
echo "clone repo"
git branch: 'main', changelog: false, credentialsId: '0438ba22-1885-4389-b8e8-d1fddd91da56', poll: false, url: 'https://github.com/Keerthikmohan/create-react-app.git'
}
}
stage('install')
{
steps{
echo "install dependencies"
sh npm install
}
     }
     stage ('TEST') {
     steps{
     echo "TESTING"
     sh 'npm run test'
     }
     }
     stage ('build'){
     steps{
     sh ''' 
     echo "buiding application"
     npm run start
     '''
     }
     }
    }
}
