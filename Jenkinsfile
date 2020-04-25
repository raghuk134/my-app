node{
   stage('SCM Checkout'){
     git 'https://github.com/raghuk134/my-app'
      
   }
   stage('Build'){
      def mvnHome = tool name: 'm2', type: 'maven'
      sh  "${mvnHome}/bin/mvn clean package"
   }
   
   stage('email-notificaiton'){
      
      mail bcc: '', body: '', cc: '', from: '', replyTo: '', subject: 'jenskins build status ', to: 'k.r.rao@outlook.com'
      
      
      
   }
   
   
}
