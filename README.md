# querying-hierarchical-data

root-category
  - cat-01
    - cat-01-a
    - cat-01-b
    - cat-01-c
      - cat-01-c-001
      - cat-01-c-002
  - cat-02
    - cat-02-a
    - cat-02-b
    - cat-02-c    
      - cat-02-c-001
      - cat-02-c-002
    
    
```sql
create table category(
  id long,
  name varchar(30),
  parent_id long
  );
  
insert into category values(0, 'root-category', -1);

insert into category values(1, 'cat-01', 0);
insert into category values(2, 'cat-01-a', 1);
insert into category values(3, 'cat-01-b', 1);
insert into category values(4, 'cat-01-c', 1);

insert into category values(40, 'cat-01-c-001', 4);
insert into category values(41, 'cat-01-c-001', 4);

insert into category values(5, 'cat-02', 0);
insert into category values(6, 'cat-02-a', 5);
insert into category values(7, 'cat-02-b', 5);
insert into category values(8, 'cat-02-c', 5);

insert into category values(80, 'cat-02-c-001', 8);
insert into category values(81, 'cat-02-c-002', 8);
```
