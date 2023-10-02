insert into college values(&roll,'&name','&prog');
program char(10) not null check (program in('baf','bscit','bcom')),
marks float (8,2) check (marks between 1 and 100),
insert into college(roll_no,name)values(4,'mohan');

alter table college rename rj_college;
alter table college add subject char (10);
alter table college drop column program;
alter table college rename column subject to course;
alter table works add p_id varchar(7) primary key;

update rj_college set subject='CG' where roll_no=2;
update rj_college set subject ='IP' where roll_no in(1,3);
update rj_college set marks =65 where subject in('WP','IOT');
update rj_college set marks = marks +5 where subject='IP';
update rj_college set marks=60 where f_name='Rohan';
update college set result ='PASS' where marks > 80;

select roll_no,marks from demo where subject in ('DBMS','DS');
select roll_no,program from college;
select * from demo where name like '%z';
delete from demo where marks >= 85 and subject in ('DBMS','DS');
select * from donar where age between 18 and 30;
select *from donar name where DOD= 02-jan-24 and address='dadar';
select *from demo order by name desc;
select *from demo where subject in('DBMS','CN') order by marks;
select name,contact,dept from personal inner join  proffessional on personal.id=proffessional.id;
select *from lives where city='Mumbai' order by p_name asc;


