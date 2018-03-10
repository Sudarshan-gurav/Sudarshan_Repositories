
  
  
      CREATE DATABASE library_managment;

      USE library_managment ;

 
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
