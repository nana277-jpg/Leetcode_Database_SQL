--Bài này sử dung left join vì đề bài yêu cầu lấy bên person address ko có thì bỏ trống 
create table Person(
    personId int primary key, 
    lastName varchar(30), 
    firstName varchar (30)
);

create table Address(
    addressId int primary key, 
    personId int references Person(personId), 
    city varchar(30), 
    state varchar(30)
);
insert into Person values (1, 'Wang', 'Allen'); 
insert into Person values (2, 'Alice', 'Bob'); 
insert into Person values (3, 'Minh', 'Thuy');
insert into Address values (1, 2, 'New York City', 'New York');
--Left join: sử dụng để truy xuất toàn bộ dữ liệu từ bảng bên trái và các bản ghi khớp từ bảng bên phải.
select 
    Person.firstName, 
    Person.lastName, 
    Address.city, 
    Address.state
from Person
left join Address
on Person.personId = Address.personId;
