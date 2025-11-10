pipeline { 
agent any 
environment { 
VERSION = "1.0-dev" 
} 
stages { 
stage('Build') { 
steps { 
echo "Building application from DEV branch" } 
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
when { branch 'main' } // won't run for dev steps 
{
echo "Deploying to development server" 
echo "Current version is ${env.VERSION}" 
} 
} 
} 
} 

