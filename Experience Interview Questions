# Experience Interview Questions
Q1. Can you explain how you designed & implemented audit service using spring boot & Log4J?
Ans:- Purpose : Audit service was created to track user activity or system events.
- Store them so that we can later use it for debugging or analytics.
Components
1. Audit Event Model - represents the structure of an audit records.
2. Audit Service - responsible for capturing & storing audit events.
3. Audit Controller - responsible for capturing events & invokes audit service.
4. Storage - file system, database, syslog server
5. Logging - Log4J for writing audit logs 

Log4J (Logging for Java) - logging framework used in Java application
- Log4j is designed for high-speed logging with low latency.

Q2. How did you implemented server-side pagination in spring boot ? How did it improved performance by 90% ?
Ans:- Spring Data JPA(Java Persistent API) supports pagination (extends JpaRepository) we just need to pass a pageable object to your repository method.

- Before Pagination 
1. The API fetched all records at once because of that high memory usage, long response time -> UI slowdown 
- After Pagination 
1. Fetch only 20-50 records per request
2. Queries are faster(LIMIT & OFFSET in SQL)
3. Lower bandwidth & memory usage.
4. Response time dropped to under 500 ms.
5. Smooth user experience even with massive datasets.

Q3. How did you measure that the performance improved by 90% after pagination ?
Ans:- We use RestAssured for API testing. 
1. API response time 
2. Memory usage 
3. CPU usage
4. Query execution time
5. Network payload size

Q4. What strategies did you followed to maintain 90% unit testcases coverage ?
Ans : To get the unit testcase code coverage we use JaCoCo tool. It generates detailed reports showing which lines & classes are covered by your unit tests.
- Integrate JaCoCo + SonarQube for detailed dashboards and PR checks.

Q5. What is a RESTful API & its main principles ?
Ans : RESTful API (Representational State Transfer) 
1. Stateless Communication between client - server
2. Client-Server Architecture 
3. Uniform interface
HTTP Methods 
1. GET  - retrieve data from the server
2. POST - submit data to the server to create a new resource
3. PUT - update an existing resource on the server
4. DELETE - delete a resource on the server
5. PATCH - partially update a resource


@ControllerAdvice - to handle exceptions globally across our entire API.
HTTP Status Code 
200 - OK
201 - Created
204 - No Content [Request successful, but no content to display]
400 - Bad Request 
401 - Unauthorized
404 - Not Found 
409 - Conflict 
500 - Internal Server Error 
