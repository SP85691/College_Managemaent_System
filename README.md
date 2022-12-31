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
    **< CREATE TABLE >** <br>
    <code>CREATE TABLE `college_management_system`.`login` (
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
    </code>
    <br>
    **< INSERT TABLE >** <br>
    <code>INSERT INTO `college_management_system`.`login` (`user_id`, `email`, `passw`) VALUES ('121009', 'surya.prata@asb.edu.in', 'Surya@1234');
      INSERT INTO `college_management_system`.`login` (`user_id`, `email`, `passw`) VALUES ('121010', 'prashant.bhat@asb.edu.in', 'Prashant@4321');
      SELECT * FROM college_management_system.login;
    </code>
    <br>
    **< SELECT TABLE >** <br>
    <code>SELECT user_id, name, login.email, passw 
      FROM college_management_system.login, college_management_system.student 
      WHERE user_id = student_id;
    </code>
    <br>
    ## Output
    <output>![image](https://user-images.githubusercontent.com/86033489/210123518-c7cf8c73-f8b0-4f0c-8842-31f569313a69.png)</output><br>
  - Second is to make table by commands. <br>
    ![image](https://user-images.githubusercontent.com/86033489/210123565-9195c5a6-36e7-488d-8b4a-2242b064fd20.png)

