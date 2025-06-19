pipeline {
    agent any 
    stages {
        stage ('clone') {
            steps 
                {
                    git branch: 'main', url: 'https://github.com/DuVanSang/projectjenskin.git'
                }
        }

        stage ('Publish') {
    		steps {
    			echo 'public 2 runnig folder'
    		//iisreset /stop // stop iis de ghi de file 
    			bat 'xcopy "%WORKSPACE%\\publish" /E /Y /I /R "D:\\myproject"'
     		}
    	}
    }
}
