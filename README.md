Designed a DB model in the name of Zenclass.
Created following tables,
        -batch
        -class
        -course
        -dashboard
        -mentor
        -queries
        -sessions
        -task
        -user
	
1. course table - contains course id and details, and (course_id) is referenced as foreign key in user table.
2. user table - contains user details and (user_id) is referenced as foreign key in batch table.
3. batch table - batch details and foreign key(batch_id and user_id)
4. class table - total classes details based on course, foreign key as (course_id)
5. mentor table - mentor_id and details, class table, batch table, session table are referenced to mentor table
6. dashboard table - contains all the performance reports of the user referenced to user, class, task table.
                - foreign key as (user_id, course_id,task_id)
7. queries table - query details(like reason, topic, raised date etc) referenced to course table and mentor table
                -foriegn key as (user_id, course_id, mentor_id)
8. sessions table - sessions details., referenced to class and mentor table
                -foreign key as(course_id, mentor_id, batch_id)
9. additional_sessions table - referenced to course and sessions table,
                                - foreign key as (course_id, mentor_id)
10. task table - referenced to dashboard and sessions table,
          - foreign key as (user_id, course_id)
