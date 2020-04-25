node{
   stage('SCM Checkout'){
     git 'https://github.com/raghuk134/my-app'
      
   }
   stage('Build'){
      def mvnHome = tool name: 'm2', type: 'maven'
      sh  "${mvnHome}/bin/mvn clean package"
   }
}
