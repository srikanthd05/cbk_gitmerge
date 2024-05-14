pipeline {
    agent any 

    stages {
	    stage('Pull from GitHub'){                         
         steps{  
                script{
				    bat '''cd C:\\Sreekanth\\git\\cbk 
					git pull'''
                                                  
            }                           
        }
		}
        stage('Copy Package to Local Git'){
            steps {
                echo "${env.JAVA_HOME}"
                bat "${env.SAG_HOME}/common/lib/ant/bin/ant -DSAGHome=${env.SAG_HOME} -DprojectName=${env.JOB_NAME} -DpackageName=${PACKAGE_NAME} copyPackage"
            }
        }
        stage('Push to GitHub'){
            steps {
			    script{
				    bat '''cd C:\\Sreekanth\\git\\cbk 
					git add .
					git commit -m "cbk demo"
					git push'''
                                                  
            }  
               
            }
        }
		
	
	
    }
}
