pipeline {
    agent any 
    stages {
        stage ('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/DuVanSang/projectjenskin.git'
            }
        }

        stage ('Publish') {
            steps {
                echo 'public 2 running folder'

                // Nếu muốn stop IIS để ghi đè file, bỏ comment dòng dưới:
                // bat 'iisreset /stop'

                // Copy nội dung trong thư mục publish sang D:\myproject
                bat 'xcopy "%WORKSPACE%\\publish\\*" "D:\\myproject" /E /Y /I /R'
            }
        }
    }
}
