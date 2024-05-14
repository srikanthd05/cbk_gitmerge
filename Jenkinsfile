pipeline {
    agent any 

    stages {
        stage('Import Build'){
            steps {
                echo "${env.JAVA_HOME}"
                bat "${env.SAG_HOME}/common/lib/ant/bin/ant -DSAGHome=${env.SAG_HOME} -DprojectName=${env.JOB_NAME} -DpackageName=${PACKAGE_NAME} copyPackage"
            }
        }
        
		
	
	
    }
}
