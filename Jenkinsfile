pipeline { 
agent any 
environment { 
VERSION = "1.0-feature-login" 
} 
stages { 
stage('Build') { 
steps { 
echo "Building login feature" 
} 
} 
stage('Test') { 
steps { 
script { 
if (isUnix()) { 
sh 'echo Testing login feature...' 
} else { 
bat 'echo Testing login feature...' 
} 
} 
} 
} 
stage('Deploy') { 
when { branch 'main' } // won't run for feature branch steps
{ 
echo "Deploying login test build" 
echo "Current version is ${env.VERSION}" 
} 
}
} 
} 

