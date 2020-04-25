node{
   stage('SCM Checkout'){
     git 'https://github.com/raghuk134/my-app'
   }
   stage('Build'){
    sh  'mvn clean package'  
   }
}
