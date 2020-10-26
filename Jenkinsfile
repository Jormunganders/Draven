pipeline {
    agent any
    stages {
        stage("停止服务") {
            steps {
                echo "ps -ef | grep "java -Xms512m -Xmx2048m -jar server.jar nogui""
            }
        }
        stage("备份地图文件")
        stage("启动服务") {
            steps {
                sh "nohup java -Xms512m -Xmx2048m -jar server.jar nogui &"
            }
        }
        stage("打印日志") {
            steps {
                sh "todo"
            }
        }
    }
}
