file 3
1.Chọn tên của tất cả các sản phẩm trong cửa hàng
select name from product;

2.Chọn tên và giá của tất cả các sản phẩm trong cửa hàng.
select name, value from product;

3.Chọn tên của các sản phẩm có giá nhỏ hơn hoặc bằng $ 200
select name frome product where value <= 200;

4.Select all the products with a price between $60 and $120
select * from product
where value >=60 and <=120;

5.Chọn tên và giá bằng xu (nghĩa là, giá phải được nhân với 100)
select name, value * 100 from product;

6.Tính giá trung bình của tất cả các sản phẩm
select AVG(value) from product;

7.Tính giá trung bình của tất cả các sản phẩm có mã nhà sản xuất bằng 2.
select AVG(value)  from product where manufacturer.code = 2;

8.Tính số lượng sản phẩm có giá lớn hơn hoặc bằng $ 180
select count() from product where >= 180;

9.Chọn tên và giá của tất cả các sản phẩm có giá lớn hơn hoặc bằng $ 180 và sắp xếp trước theo giá (theo thứ tự giảm dần), sau đó theo tên (theo thứ tự tăng dần)
select product
from name, value
where >=180
order by desc value, asc name;

10.Chọn tất cả dữ liệu từ các sản phẩm, bao gồm tất cả dữ liệu cho từng nhà sản xuất của sản phẩm.
select * from product, manufacturer
where product.manufacturer = manufacturer.code;

11.Chọn tên sản phẩm, giá và tên nhà sản xuất của tất cả các sản phẩm
select product.name, value, manufacturer.name
frome product, manufacturer
where product.manufacturer = manufacturer.code;

12.Chọn giá trung bình của mỗi sản phẩm của nhà sản xuất, chỉ hiển thị mã của nhà sản xuất
select AVG(value), manufacturer
from product
group by manufacturer.code;

13.Chọn giá trung bình của mỗi sản phẩm của nhà sản xuất, hiển thị tên của nhà sản xuất
select AVG(value), manufacturer.name
from product
group by manufacturer.name;

14.Chọn tên của nhà sản xuất có sản phẩm có giá trung bình lớn hơn hoặc bằng $ 150
select AVG(value) manufacturer.name
from product, manufacturer
where product.manufacturer = manufacturer.code
group by manufacturer.name
having AVG(value)>=150;

15.Chọn tên và giá của sản phẩm rẻ nhất
select name, value 
from product
where value = (select Min(value) from product);

16. Chọn tên của mỗi nhà sản xuất cùng với tên và giá của sản phẩm đắt nhất của nó
select manufacturer.name 


17.Thêm một sản phẩm mới: Loa, $ 70, nhà sản xuất 2
insert into product (name, value, manufacturer, code)
value (7,Loudspeakers,70,2);

18.Cập nhật tên của sản phẩm 8 thành "Máy in Laser"
update product
set name = Laser printers
where code = 8 ;

19.Áp dụng giảm giá 10% cho tất cả các sản phẩm
update product
set value = value - (value*0,1)

20.Áp dụng giảm giá 10% cho tất cả các sản phẩm có giá lớn hơn hoặc bằng $ 120
update product
set value = value - (value*0,1)
where value>=120;


test 2
1.Chọn tên cuối cùng của tất cả nhân viên

