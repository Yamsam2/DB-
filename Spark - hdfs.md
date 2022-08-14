SaveMode 사용시 

쓰기
import org.apache.spark.sql._ 입력해줘야됨

 connectionDataframe.write.mode(SaveMode.Overwrite).csv("hdfs:///output/testgiss.csv")




저장 파일 읽기<br>
import org.apache.spark.sql.SparkSession 
val sparkSession = SparkSession.builder().appName("example-spark-scala-read-and-write-from-hdfs").getOrCreate()

val df_csv = sparkSession.read.option("inferSchema", "true").csv("hdfs:///output/testgiss.csv") 

참고site<br> 
https://saagie.zendesk.com/hc/en-us/articles/360030094231-Spark-Scala-Read-Write-files-from-HDFS
 
 
 
