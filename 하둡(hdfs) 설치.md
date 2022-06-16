https://www.youtube.com/watch?v=g7Qpnmi0Q-s

hadoop 3.3.2version + jdk-11.0.15.1
hdfs/datanode
hdfs/namenode 경로로 설정

bin 폴더에서 명령어
start-all.cmd
stop-all.cmd
hdfs namenode -format

http://localhost:9870 - 하둡 웹 인터페이스

http://localhost:9864 - 데이터 노드 

http://localhost:8088 - 클러스터

데이터노드 구동 오류시 
VERSION 파일 내용의 아이디를 일치시켜주거나 파일내용 모두 삭제, 포맷 후 다시 실행 

- 환경변수 경로 설정시 띄어쓰기 인식함 
- properties 파일 설정시 폴더 경로 C:\ 형식으로 해야 작동  
