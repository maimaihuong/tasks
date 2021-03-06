## Hoạt động của EasyWeb

### Tính năng cho End-users (người sử dụng)

1. Đăng nhập EasyWeb | Đăng ký miễn phí 
   
2. Tạo mới website từ các mẫu có sẵn 

3. Nhập liệu cho từng trang đang có 

4. Public website trên easyweb sub-domain

4. Cho phép đổi sang domain riêng 

## Yêu Cầu thực hiện hệ thống  

### Đăng nhập | Đăng ký
 - [ ] quản lý account bởi identity server, cho phép chứng thực trên easywebhub.com hoặc software (EasyBuider)
    - [ ] `user-name`: bắt đầu bởi a-z, cho phép 0-9, cho phép kí tự đặc biệt  để ảnh hưởng tới tạo subdomain sau này 
 - [ ] cho phép đăng ký bằng Facebook, Github, Google+

### EasyMarket: website mẫu
- websites mẫu tuân theo các quy định của EasyWeb, được kiểm tra trước khi cung cấp
- restful API danh sách 
   - [ ] tạm thời sử dụng `easymarket.json` trên github để tiện thay đổi, cập nhật
   - sau này chuyển sang api động, cho phép thay đổi theo account và loại khách hàng (có nhiều market dành riêng cho từng cộng đồng)

### Tạo mới websites
- [ ] kiểm tra đặt tên website `website-name`:  a-z, 0-9,  không có kí tự đặc biệt
- [ ] tự động tạo sub-domain  `xxx.easywebhub.com` 
   - [ ] `xxx` :   `{website-name}-{user-name}`, không thuộc các keywords đang sử dụng : `blog, guide, book, ...` 
   - [ ] cho phép sử dụng github Pages hoặc dùng VPS riêng để hosting 
   - [ ] sử dụng cloudflare tự động add CNAME và thiết lập `easywebhub.github.io` 
 
- tạo mới và đồng bộ phần `source` và `gh-pages` từ `source.easywebhub.com`

### Nhập liệu cho website
- [ ] Lựa chọn giữa sử dụng `xxx.easywebhub.com/admincp` theo từng websites hoặc tạo domain chung `easywebhub.com/admincp` 

- luôn luôn đồng bộ với `source.easywebhub.com` bao gồm source và cả build (gh-pages) 

### Cho phép dùng domain riêng

- [ ] tài liệu hướng dẫn `xxx.easywebhub.com`  => `user-domain.xxx`
  
- [ ] CMS Url cũng đổi theo domain riêng này, ví dụ `user-domain.xxx/admincp` 

- [ ] việc thay đổi phải cập nhật vào thông tin websites quản lý bởi EasyWeb




