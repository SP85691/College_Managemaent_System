# College_Managemaent_System
In this Project, I have created a College Management System using MySQL. It is used for handle the data of following entities such as, Students, Faculty, Books, Exams and many more.

### Process to Create `CMS` Database
- Open Your Local Instance MySQL 80 <br> <br>
![image](https://user-images.githubusercontent.com/86033489/210123204-9ed15252-8d97-401b-93c0-3697294ef93b.png)

- Create Your New Schema Named as <b>College_Management_System <br> <br>
![image](https://user-images.githubusercontent.com/86033489/210123244-359b6ce5-87c2-411e-bd32-907ecb7b06fe.png)

- Now You Can Create Multiple Table as per your Requirements. 
- I Have Create Some Type of Tables, such as
<ol>
  <li> Login </li>
  <li> Student </li>
  <li> Faculty </li>
  <li> Courses </li>
  <li> Exams </li>
</ol>

## Login Table
There are Two Ways to Create any table in Workbench.
  - First is to make table by running the query. <br>
    <code>
      CREATE TABLE `college_management_system`.`login` (
      `user_id` INT NOT NULL,
      `email` VARCHAR(45) NOT NULL,
      `passw` VARCHAR(45) NOT NULL,
      PRIMARY KEY (`user_id`),
      UNIQUE INDEX `user_id_UNIQUE` (`user_id` ASC) VISIBLE,
      CONSTRAINT `user_id`
      FOREIGN KEY (`user_id`)
      REFERENCES `college_management_system`.`student` (`student_id`)
      ON DELETE NO ACTION
      ON UPDATE NO ACTION);
    </code
    
    <br>
      
  - Second is to make table by commands. <br>
