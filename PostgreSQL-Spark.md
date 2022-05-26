### 정형데이터 기준(테이블)

https://www.youtube.com/watch?v=rAeQ2k-C00o<br>
https://hevodata.com/learn/spark-postgresql/

spark3.1.3 준비<br>
postgresql.jar 연결 파일 준비(JDBC driver)<br>
스파크 셸 실행<br>

&#45; 명령어 -

패스설정<br>
:require c:/postgresql-42.3.5.jar

자바properties(파일입출력) 임포트<br>
import java.util.Properties

properties 선언<br>
val connectionProperties = new Properties()<br>
connectionProperties.setProperty("Driver", "org.postgresql.Driver")

user/password 입력<br>
connectionProperties.put("user", "postgres")<br>
connectionProperties.put("password", "test")

테이블 변수 선언(스키마)<br>
val pgTable = "public.map_26"

데이터프레임만들기   속성 : (url="db주소", 스키마 이름, connectionProperties)<br>
val connectionDataframe = spark.read.jdbc(url="jdbc:postgresql://localhost:5432/qgistest", pgTable, connectionProperties)

프레임보기<br>
connectionDataframe.show()

