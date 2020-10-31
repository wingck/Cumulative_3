# BlogProject_1
This is the first iteration of our blog project, which has a proof-of-concept to access our MySQL Database.

## How to Install:
- Step 1 : Download [MAMP](https://www.mamp.info/en/downloads/) or similar MySQL environment
- Step 2 : [Download "authors.sql", "articles.sql", "comments.sql", "tags.sql" from the datagenerator](http://sandbox.bittsdevelopment.com/humber/datagenerator/)
- Step 3 : Create a blog database 
    - PhpyMyAdmin -> new database -> blog
    - === or ===
    - `mysql> create database blog`
- Step 4 : Import Tables
  - PhpyMyAdmin -> Import -> Upload authors.sql
  - PhpMyAdmin -> Import -> Upload articles.sql
  - PhpMyAdmin -> Import -> Upload comments.sql
  - PhpMyAdmin -> Import -> Upload tags.sql
  - === or ===
  - `mysql> mysql -uroot -p blog < authors.sql`
  - `mysql> mysql -uroot -p blog < articles.sql`
  - `mysql> mysql -uroot -p blog < comments.sql`
  - `mysql> mysql -uroot -p blog < tags.sql`
- Step 5 : Access Connection String properties for your blog DB and change host, username, pass, port in "/Models/DbContext.cs"
