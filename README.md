# SQL-Task-EduBridge
SQL Task

--Creating table as Class

The table contains enrollment no, student name, section, subject id, marks.

         create table class(Enrollment_No  int primary key,
                              Student_Name varchar(20),
                              Section varchar(3),
                              Subject_Id int ,
                              Marks int);
                              
--Inserting Values for the required attributes.

    insert into class values
     (1,"Tim","A",1,70),
     (2,"Jim","A",2,75),
     (3,"Kim","B",3,66),
     (4,"Tom","B",4,77),
     (5,"John","C",5,60),
     (6,"joe","C",1,82),
     (7,"James","B",2,76),
     (8,"Henry","C",5,68),
     (9,"Matt","B",3,71),
     (10,"paul","A",4,79);
--To display the Entire Table

  select * from class;
--To display the No of candidates greater than or equal to 75 marks

  select Section,count(section) as
  No_of_candidates_greater_than_or_equal_to_75_marks
  from class where Marks>=75 group by section;
