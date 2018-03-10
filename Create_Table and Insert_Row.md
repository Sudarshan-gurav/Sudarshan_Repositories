
  ### CREATE TABLE FOR LIBRARY_MANAGEMENT
  
  **CREATE TABLE FOR LIBRARY_MANAGEMENT**
  
      CREATE DATABASE library_managment;

   **USE DATABASE**
   
      USE library_managment ;

   **CREATE TABLES FOR LIBRARY_MANAGEMENT**
   
    CREATE TABLE member_details  
    (
       id INT PRIMARY KEY,
       first_name VARCHAR(255),
       last_name VARCHAR(255),
       mobile INT,
       email VARCHAR(255),
       address VARCHAR(255)
    ) ;

    CREATE TABLE book_stock
    (
       id INT PRIMARY KEY,
       name VARCHAR(255),
       quantity INT
    ) ;


    CREATE TABLE author
    (
        id INT PRIMARY KEY,
        name VARCHAR(255)
    ) ;

    CREATE TABLE book_authors
    (
        author_id INT,
        book_id INT,
    
        foreign key (author_id) references member_details(id),
        foreign key (book_id) references book_stock(id)
    ) ;


    CREATE TABLE log_table
    (
       mem_id INT,
       book_id INT,
       issue_date DATE,
       return_date DATE,

       foreign key (mem_id) references member_details(id),
       foreign key (book_id) references book_stock(id)
    ) ;

    CREATE table monthly_subscription
    (
    mem_id INT,
    date_of_payment DATE NULL,
    amount INT,
    
    foreign key (mem_id) references member_details(id)
    ) ;
    
   **INSERT VALUES IN TABLES**
   

                 INSERT INTO
                   member_details 
                VALUES
                   ( 1 , 'pratik', 'bali', 7757, 'pb@g', 'swarge ),
                   ( 2, 'aakash' , 'hadawle', 8793, 'ah@g', 'yerwada') ,
                   ( 3, 'sudarshan', 'gurav', 8765, 'sg@g', 'kothrud'),
		   ( 4, 'swapnil' , 'ingle', 8877, 'si@g', 'kothrud') 
  		   (5, 'raj', 'rao', 7788, 'ro@g', 'yerwada'), 
                   (6, 'ram', 'kumar', 9977, 'rk@g', 'swarget'), 
                   (,7, 'rajan', 'sathe', 9988, 'rs@g', 'swarget'), 
                   (8, 'jasprit', 'bumrah', 5544, 'jb@g', 'kothrud'),
                   (9, 'sachin', 'tendulkar', 3366, 'st@g', 'yerwada'),
                   (10, 'krishna', 'pawar', 2233, 'kp@g', 'vimannagar'),
                   (11, 'gautom', 'nayar', '1144', 'gn@g', 'vimannagar' )
                   
                ;      



           INSERT 
              	INTO book_stock 
              VALUES 
                    ( 1,'c',10 ) ,
                    ( 2,'c++',20 ) ,
                    ( 3,'java',100 ) ,
                    ( 4,'database',50 ) , 
                    ( 5,'cs',20 ) ,
                    ( 6,'linux',40 ) ,
                    ( 7,'unix',60 ) ,
                    ( 8,'win',35 ) ,
                    ( 9,'python',80 ) ,
                    ( 10,'dotnet',70 ) ,
                    ( 11,'',90 ) ,
                    ( 12 ,'Autumn' ,20  ) ,
                    (13 , 'How to Win Friends and Influence People', 30  ),
                    (14 , 'Think and Grow Rich',  25 ),
                    (15  ,'Laws of Success' ,35 ),
                    (16 , 'The 7 Habits of Highly Effective Teens' ,  35 ),
                    (17 , 'As a Man Thinketh'  , 45 ),
                    (18 , 'See You at the Top' , 45 ),
                    (19 , 'Rich Dad Poor Dad' , 10 ),
                    (20 , 'The 80/20 Principle' , 20 ),
                    (21 , 'How to Get from Where You Are to Where You Want to Be' , 24 ),
                    (22 , 'The Power Of Less'  ,21 ),
                    (23 , 'Brain Rules' ,  40 ),
                    (24 ,'48 laws of power', 40 ),
                    (25 ,'Mastery',   40 );



                INSERT 
                  INTO author 
                  VALUES
                      ( 1,'brian kernighan' ) ,
                      ( 2,'dennis ritchie' ) ,
                      ( 3,'bjarne stroustrup' ) ,
                      ( 4,'james gosling' ) ,
                      ( 5,'korth' ) ,
                      ( 6,'alan turung' ) ,
                      ( 7,'linus torvalds') ,
                      ( 8,'kirk bauer' ) ,
                      ( 9,'bill' ) ,
                      ( 10,'nageshwar rao' ) ,
                      ( 11,'aakash' ) ,
                      (12,'ali smith'),
                      (13,'Dale Carnegie'),
                      (14,'Napoleon Hill'),
                      (15,'Napoleon Hill '),
                      (16,'Sean Covey'),
                      (17,'James Allen'),
                      (18,'Zig Ziglar'),
                      (19,' Robert T. Kiyosaki '),
                      (20,'Richard Kosh'),
                      (21,'Jack Canfield'),
                      (22,'Leo Babauta'),
                      (23,'John Medina '),
                      (24,'Robert Greene'),
                      (25,'Robert Greene');


                  INSERT 
                  INTO book_authors 
                  VALUES 
                     ( 1,1 ) ,
                     ( 2,1 ) ,
                     ( 3,2 ) ,
                     ( 4,3 ) ,
                     ( 5,4 ) ,
                     ( 6,5 ) ,
                     ( 7,6 ) ,
                     ( 8,7 ) ,
                     ( 9,8 ) ,
                     ( 10,9 ) ,
                     ( 11,10 ) ;


            INSERT
            INTO log_table
            VALUES  
                   ( 1 , 1 , '2018/01/10' , '2018/01/20' ) ,
                   ( 2 , 3 , '2018/01/05' , '2018/01/15' ) ,
                   ( 3 , 2 , '2017/12/10' , '2017/12/20' ) ,
                   ( 4 , 4 , '2017/08/10' , '2017/08/20' ) ,
                   ( 5 , 5 , '2018/01/04' , '2018/01/14' ) 
                   ( 6 , 6 , '2018/01/15' , '2018/01/25' ) ,
                   ( 7 , 7 , '2018/01/25' , '2018/02/04' ) ,
                   ( 8 , 8 , '2017/09/10' , '2017/09/20' ) ,
                   ( 9 , 9 , '2017/10/01' , '2017/10/11' ) ,
                   ( 10 , 10 , '2018/01/10' , '2018/01/20') ,
                   ( 11 , 4 ,  '2018/01/20'  ,  '2018/01/30' ) ,
                   ( 11 , 4 , '2018-01-10' , NULL )
                   ( 4 , 6  , '2018/01/06' , '2018/01/16' ),
                   ( 5 , 7 , '2018-01-08' , NULL ),
                   ( 8, 9, '2018/01/08', '2018/01/21' ),
                   ( 3, 6, '2018/01/05' ,'2018/01/20' ),
                   ( 10, 7, '2018/01/02' , '2018/01/20' ),
                   ( 2,  4, '2018/01/08' , '2018/01/21' ),
                   ( 2, 10, '2018/01/14' , '2018/01/26' ),
                   ( 4, 7, '2018/01/24' , '2018/02/10' ),
                   ( 4, 5, '2018/02/04' , '2018/02/17' );





                    INSERT INTO monthly_subscription 
                      VALUES
                      (1,'2018/01/01',500),
                      (2,'2018/01/01',500),
                      (3,'2017/12/01',500),
                      (4,'2017/08/01',500),
                      (5,'2018/01/01',500),
                      (6,'2018/01/01',500),
                      (7,'2018/01/01',500),
                      (8,'2017/09/01',500),
                      (9,'2017/10/01',500),
                      (10,'2018/01/01',500),
                      (11,'2018/01/01',500),
                      (4,null,0),
                      (5,'2018/01/01',500);

