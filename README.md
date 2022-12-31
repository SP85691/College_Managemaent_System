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
  #### First is to make table by running the query. <br>
    **< CREATE TABLE >**
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
  
    **< INSERT TABLE >**
      INSERT INTO `college_management_system`.`login` (`user_id`, `email`, `passw`) VALUES ('121009', 'surya.prata@asb.edu.in', 'Surya@1234');
      INSERT INTO `college_management_system`.`login` (`user_id`, `email`, `passw`) VALUES ('121010', 'prashant.bhat@asb.edu.in', 'Prashant@4321');
      SELECT * FROM college_management_system.login;

    **< SELECT TABLE >**
      SELECT user_id, name, login.email, passw 
      FROM college_management_system.login, college_management_system.student 
      WHERE user_id = student_id;
 
  #### Second is to make table by commands. 
    ![image](https://user-images.githubusercontent.com/86033489/210123596-88bbbb04-aa2e-4a0c-8f92-68a91ad197ff.png)
  
  ## Output
  ![image](https://user-images.githubusercontent.com/86033489/210123803-b4bff3ad-9fe9-4b8c-bf9f-a3c4f3dd536f.png)
 
## Student Table
  #### QUERY 
    **< CREATE TABLE >**
      CREATE TABLE `college_management_system`.`student` (
      `student_id` INT NOT NULL AUTO_INCREMENT,
      `name` VARCHAR(45) NOT NULL,
      `dob` VARCHAR(45) NOT NULL,
      `enrollment_no` VARCHAR(45) NOT NULL,
      `course` VARCHAR(45) NOT NULL,
      `semester` INT NOT NULL,
      `email` VARCHAR(45) NOT NULL,
      PRIMARY KEY (`student_id`),
      UNIQUE INDEX `student_id_UNIQUE` (`student_id` ASC) VISIBLE);
  
    **< INSERT TABLE >** 
      INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121009, 'Surya Pratap', '03-06-2002', 'ASB/BCA/20/043', 'BCA', '6', 'surya.pratap@asb.edu.in'), 
      INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121010, 'Prashant Bhatt', '20-12-2002', 'ASB/BCA/20/030', 'BCA', '4', 'prshant.bhatt@asb.edu.in'), 
      INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121011, 'Alok Chaurasia', '10-10-2000', 'ASB/BCA/20/012', 'BCA', '6', 'alok.chaurasia@asb.edu.in'), 
      INSERT INTO `college_management_system`.`student` (`student_id`, `name`, `dob`, `enrollment_no`, `course`, `semester`, `email`) VALUES (121007, 'Salena Gomez', '25-08-1999', 'ASB/BCA/20/033', 'BCA', '5', 'salena.gomez@asb.edu.in');
      
    **< SELECT TABLE >**
      SELECT * FROM college_management_system.student;
  
  #### TABULER 
  ![image](https://user-images.githubusercontent.com/86033489/210123676-b85382fc-1395-4371-b8e5-cae1cf87c0ab.png)
  
  ## Output
  ![image](https://user-images.githubusercontent.com/86033489/210123785-a9439e90-5fb3-416e-a43e-80b741d3ade7.png)

## Faculty Table
  #### QUERY 
    **< CREATE TABLE >**
      CREATE TABLE `college_management_system`.`faculty` (
      `faculty_id` INT NOT NULL AUTO_INCREMENT,
      `faculty_name` VARCHAR(45) NOT NULL,
      `dob` VARCHAR(45) NOT NULL,
      `department` VARCHAR(45) NOT NULL,
      `designation` VARCHAR(45) NOT NULL,
      `email` VARCHAR(45) NOT NULL,
      PRIMARY KEY (`faculty_id`),
      UNIQUE INDEX `faculty_id_UNIQUE` (`faculty_id` ASC) VISIBLE);
  
    **< INSERT TABLE >** 
      INSERT INTO `college_management_system`.`faculty` (`faculty_id`, `faculty_name`, `dob`, `department`, `designation`, `email`) VALUES (256121, 'Prof. Shyla', '11-09-1992', 'DBMS', 'Assistant Professor', 'shyla@asb.edu.in'), 
      INSERT INTO `college_management_system`.`faculty` (`faculty_id`, `faculty_name`, `dob`, `department`, `designation`, `email`) VALUES ('256102', 'Prof. Upesh Bhatnagar', '21-03-1978', 'Computer Network', 'Assistent Professor', 'upesh.bhatnagar@asb.edu.in');
      INSERT INTO `college_management_system`.`faculty` (`faculty_id`, `faculty_name`, `dob`, `department`, `designation`, `email`) VALUES ('256122', 'Prof. Nehu Gumber', '21-03-1991', 'OOPS', 'Assistent Professor', 'nehu.gumber@asb.edu.in');
      INSERT INTO `college_management_system`.`faculty` (`faculty_id`, `faculty_name`, `dob`, `department`, `designation`, `email`) VALUES ('256127', 'Prof. Nupur Sharma', '31-05-1985', 'PDCC', 'CSW', 'nupur.sharma@asb.edu.in');
      
    **< SELECT TABLE >**
      SELECT * FROM college_management_system.faculty;
  
  #### TABULER
  ![image](https://user-images.githubusercontent.com/86033489/210124086-d2c554db-a723-4242-8982-52f23229a573.png)
  
  ## Output
  ![image](https://user-images.githubusercontent.com/86033489/210124068-7e95a174-3771-4ca8-912e-7c92804ac584.png)
  
  ## Courses Table
  #### QUERY 
    **< CREATE TABLE >**
      CREATE TABLE `college_management_system`.`course` (
      `course_code` INT NOT NULL,
      `course_name` VARCHAR(45) NOT NULL,
      `course_type` VARCHAR(45) NOT NULL,
      `lecturer` VARCHAR(45) NOT NULL,
      `semester` VARCHAR(45) NOT NULL,
      PRIMARY KEY (`course_code`),
      UNIQUE INDEX `course_code_UNIQUE` (`course_code` ASC) VISIBLE);
  
    **< INSERT TABLE >** 
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('302', 'Object Oriented Programming', 'Technical', 'Prof. Nehu Gumber', '3');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('301', 'Data Structure', 'Technical', 'Prof. Shyla', '3');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('501', 'JAVA', 'Technical', 'Prof. Suvidha Agarwal', '5');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('302', 'Object Oriented Programming', 'Technical', 'Prof. Nehu Gumber', '3');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('301', 'Data Structure', 'Technical', 'Prof. Shyla', '3');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('501', 'JAVA', 'Technical', 'Prof. Suvidha Agarwal', '5');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('502', 'Database Management System', 'Technical', 'Prof. Shyla', '5');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('508', 'German', 'Non-Technical', 'Prof. Rajni', '5');
      INSERT INTO college_management_system.course (`course_code`, `course_name`, `course_type`, `lecturer`, `semester`) VALUES ('602', 'E-Commerce', 'Technical', 'Prof. Upesh Bhatnagar', '6');

      
    **< SELECT TABLE >**
      SELECT * FROM college_management_system.course;
  
  #### TABULER
  ![image](https://user-images.githubusercontent.com/86033489/210124167-1c826155-6826-4359-8de7-dd9fb5f4ebae.png)
  
  ## Output
  ![image](https://user-images.githubusercontent.com/86033489/210124183-2d59bab5-067f-42ab-b926-b172182f38b5.png)
  
  ## Exams Table
  #### QUERY 
    **< CREATE TABLE >**
      CREATE TABLE `college_management_system`.`exams` (
      `student_id` INT NOT NULL AUTO_INCREMENT,
      `exam_name` VARCHAR(45) NOT NULL,
      `exam_date` VARCHAR(45) NULL,
      `grade` INT NOT NULL,
      PRIMARY KEY (`student_id`),
      UNIQUE INDEX `student_id_UNIQUE` (`student_id` ASC) VISIBLE);
  
    **< INSERT TABLE >** 
      INSERT INTO college_management_system.exams (`student_id`, `exam_name`, `exam_date`, `grade`) VALUES ('121009', 'Numerical Methods', '02-01-2023', '85');
      INSERT INTO college_management_system.exams (`student_id`, `exam_name`, `exam_date`, `grade`) VALUES ('121011', 'Database Management System', '03-01-2023', '92');
     
    **< SELECT TABLE >**
      SELECT * FROM college_management_system.course;
  
  #### TABULER
  ![image](https://user-images.githubusercontent.com/86033489/210124268-6a6d8d41-3f97-457d-8aca-2f9d50413a9c.png)
  
  ## Output
  ![image](https://user-images.githubusercontent.com/86033489/210124278-c0b27f11-2ed1-4ddd-99f2-18435bbfb0f2.png)

