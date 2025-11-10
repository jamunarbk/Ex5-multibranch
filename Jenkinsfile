pipeline { 
agent any 
environment { 
VERSION = "1.0" 
} 
stages { 
stage('Build') { 
steps { 
echo "Building application from MAIN branch" 
} 
} 
stage('Test') { 
steps { 
script { 
if (isUnix()) { 
sh 'echo Testing code...' 
} else { 
bat 'echo Testing code...' 
} 
} 
}
} 
stage('Deploy') { 
when { branch 'main' } // only main deploys steps 
{ 
echo "Deploying to production" 
echo "Current version is ${env.VERSION}" } 
} 
} 
}
