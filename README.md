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
  - Second is to make table by commands. 
    ![image](https://user-images.githubusercontent.com/86033489/210123596-88bbbb04-aa2e-4a0c-8f92-68a91ad197ff.png)
  
  ## Output
    ![image](https://user-images.githubusercontent.com/86033489/210123518-c7cf8c73-f8b0-4f0c-8842-31f569313a69.png)
 
## Student Table
There are Two Ways to Create any table in Workbench.
  - First is to make table by running the query. <br>
    **< CREATE TABLE >** <br>
    <code>CREATE TABLE `college_management_system`.`student` (
      `student_id` INT NOT NULL AUTO_INCREMENT,
      `name` VARCHAR(45) NOT NULL,
      `dob` VARCHAR(45) NOT NULL,
      `enrollment_no` VARCHAR(45) NOT NULL,
      `course` VARCHAR(45) NOT NULL,
      `semester` INT NOT NULL,
      `email` VARCHAR(45) NOT NULL,
      PRIMARY KEY (`student_id`),
      UNIQUE INDEX `student_id_UNIQUE` (`student_id` ASC) VISIBLE);
    </code>
    <br>
    **< INSERT TABLE >** <br>
    <code>INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121009, 'Surya Pratap', '03-06-2002', 'ASB/BCA/20/043', 'BCA', '6', 'surya.pratap@asb.edu.in'), 
      INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121010, 'Prashant Bhatt', '20-12-2002', 'ASB/BCA/20/030', 'BCA', '4', 'prshant.bhatt@asb.edu.in'), 
      INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121011, 'Alok Chaurasia', '10-10-2000', 'ASB/BCA/20/012', 'BCA', '6', 'alok.chaurasia@asb.edu.in'), 
      INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121007, 'Salena Gomez', '25-08-1999', 'ASB/BCA/20/033', 'BCA', '5', 'salena.gomez@asb.edu.in');
    </code>
    <br>
    **< SELECT TABLE >** <br>
    <code>SELECT * FROM college_management_system.student;</code>
    <br>
  - Second is to make table by commands. 
  ![image](https://user-images.githubusercontent.com/86033489/210123676-b85382fc-1395-4371-b8e5-cae1cf87c0ab.png)
  
  ## Output
    ![image](https://user-images.githubusercontent.com/86033489/210123681-778bf807-849d-470c-bbc4-29af26c74104.png)

