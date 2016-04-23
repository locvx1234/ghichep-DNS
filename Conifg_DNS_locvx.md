

## 1. Cài đặt Bind9

Để cài đặt Bind9, bạn thực hiện các bước sau:

```
# sudo -i
# apt-get update
# apt-get install bind9
```

Ta sẽ làm việc với thư mục chính là: `/etc/bind`
Bên trong thư mục này, bạn sẽ cấu hình các file :

	/etc/bind/named.conf.local
	
	/etc/bind/db.local
	
	File CSDL DNS (/etc/bind/db.locvx1234.com)
	
## 2. Cấu hình 
Thêm một zone mới vào file : `/etc/bind/named.conf.local` 

```
zone "locvx1234.com" {
	type master;
		file "/etc/bind/db.locvx1234.com";
};

