Structured Query Language (SQL)

SQL 
Structured Query Language is a programming language which allows us to communicate with and manipulate databases.
Earlies of 1970s, there were 2 young man who works at IBM; Donald Chamberlain and Raymond Boyce. These years, IBM really needs to get Access and do some modification data held in databases, because it means to reach goal easier and more important one : FASTER. So, Chamberlain and Boyce started to develop a new language. Their first attempt  was “Square”, but it was difficult to use according to its own subscript notation. Then in 1973, they tried a new work “SEQUEL”. It is first name of SQL because SEQUEL was a trademark of the UK-based Hawker Siddeley Dynamics Engineering Limited company. They investigated Datalog too much during the developing, because its typing discipline is perfect fits to SQL.

When/why shall we use it?
SQL has a lot of advantages which is given below but for me, it makes it easy to work with is that it hides the complexity of processing. It faces only with database objects.
Some Advantages of SQL :
1-	Requires no coding. (No need to complex codes,just basics.)
2-	Well Defined Standard (ANSI standart language.)
3-	Interactive Language(You can reach complex results within seconds.)
4-	Manipulating Database(That’s what we want)
5-	Extensibility(It can be integrated with other languages.)

In a nutshell, We should use it because, data is important for almost every application.

How to setup an environment?
There are many different versions of SQL available currently. The easiest one to use on your own computer is by using the application XAMPP. You can download XAMPP on it’s website and it’s available on Windows, Linux or Mac. You just simply download and go through the setup. After you launch it you have to start Apache and MySQL modules on it. It starts a SQL Database server named MariaDB on your localhost and it’s very easy to use with it’s UI Design. There are applications that allow you to install SQL to a server and then control it remotely. This is the most common use for SQL applications. You got Microsoft Windows SQL Server for Windows based databases or DBeaver for Linux based SQL applications for just one example. You can mostly go to the specific SQL based application for your needs and install it according to the developers’ guide on how to install them.

Things that are specific to SQL
SQL is very different from other programming languages in a lot of ways. It has its own syntax unlike another I have ever seen. It doesn’t necessarily have variable but instead since SQL is a programming language for storing data it has rows and columns that are inside a specific table. It has queries (commands that can create, store, change and manipulate data by your choosing) that you run inside the SQL database. It has keywords and a structure that consist of clauses, expressions, predicates, queries, and statements. Its keywords are very similar to the English language and so it makes it very clear and easy to both learn and write SQL in a lot of ways. Although it has its advanced uses, many people can understand the basic purpose of an SQL query just by looking at it. It introduced the concept of accessing many records with one single command and it eliminates the need to specify how to reach a record, e.g. with or without an index. SQL was one of the first commercial languages to utilize Edgar F. Codd’s relational model. The model was described in his influential 1970 paper, "A Relational Model of Data for Large Shared Data Banks". Despite not entirely adhering to the relational model as described by Codd, it became the most widely used database language. 

Example Queries for SQL
CREATE TABLE `studentdatabase`.`course` ( `courseID` VARCHAR(6) NOT NULL, `courseName` VARCHAR(50) NULL ,`section` INT(3) NOT NULL, `teacher` VARCHAR(30) NULL , `credit` INT(10) NULL , `AKTS` INT(10) NULL , `examType` VARCHAR(15) NULL , `weeklyHours` INT(15) NULL , `quota` INT(15) NULL , `assistant` VARCHAR(30) NULL)
This is for creating a table called studentdatabase.

ALTER TABLE `examenrollment` ADD FOREIGN KEY (`FK_examID`) REFERENCES `exam`(`examID`) ON DELETE CASCADE ON UPDATE RESTRICT;
This query is for adding a foreign key to an attribute.

INSERT INTO student
SELECT studentID,name,surname,faculty,program,tc,grade,email,address,phoneNumber,fatherName,motherName,gano,educationStatus,sex,marriageStatus,birthplace,disabilityStatus,bloodtype,licence
FROM unf
This query is for selecting some data from the table “unf” and inserting it into the table “student”

SELECT c.courseID , c.courseName , c.section , c.teacher , COUNT(c.courseID) AS StudentCount
FROM course c , courseenrollment ce
WHERE c.courseID = ce.FK_courseID AND c.section = ce.FK_section
GROUP BY c.courseID , c.courseName , c.section , c.teacher 
ORDER BY c.courseID
This query is for selecting data by filtering it according to the given requirements and ordering them by defined in the query.
