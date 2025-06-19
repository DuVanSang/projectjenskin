pipeline {
    agent any 

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/DuVanSang/projectjenskin.git'
            }
        }

        stage('Publish') {
            steps {
                echo 'Copying all repo contents to D:\\myproject'

                // Copy toàn bộ nội dung thư mục hiện tại sang D:\myproject
                bat 'xcopy "%WORKSPACE%\\*" "D:\\myproject" /E /Y /I /R'
            }
        }
    }
}
