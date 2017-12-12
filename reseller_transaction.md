# [Transaction](#transaction)
* [List](#danh-sách)
* [Detail](#chi-tiết)
## [List](#search)
Search Reseller's transaction
> **API:** /api/rms/v1/transaction/list  
> **Method:** POST  
> **Body should be a JSON object (JSON):**   
```
{
   "page": 0,
   "pageSize": 30,
   "onlyOrganization": true,
   "type": "invoice",
   "description": "querystring",
   "transactionKey": "register",
   "serviceType": "domain",
   "customerEmail": "customer@example.vn",
   "resourceId": 0,
   "fromCreatedDate": "01/01/2017 00:00",
   "toCreatedDate": "01/01/2017 00:00"
}
```
**page**: page, default 0  
**pageSize**: Number of customers to pick up, default 30  
**onlyOrganization**: Only transaction of Reseller, excluding sub-Reseller, the default is false  
**type**: Type of transaction [{'invoice': 'invoice'}, {'refund': 'refund'}, {'receipt': 'receipt'}, {'arrear': 'arrear'}]  
**description**: description  
**transactionKey**: mã giao dịch[{'register': 'đăng ký mới'},{'renew': 'duy trì'},{'change-registrant': 'đổi tên chủ thể'},
{'protect-privacy': 'ẩn thông tin'},{'transfer': 'chuyển nhà đăng ký'},{'registry-lock': 'registry lock'},{'registrar-lock': 'registrar lock'},
{'change-dns': 'đổi dns'},{'upgrade-plan': 'nâng cấp gói'},{'modify-plan': 'tùy chỉnh gói'},{'backorder': 'đặt chỗ'}]  
**serviceType**: dịch vụ[{'domain': 'tên miền'}, {'hosting': 'hosting'}, {'email': 'email'}, {'vps': 'Cloud VPS'}]  
**customerEmail**: email khách hàng  
**resourceId**: id của dịch vụ(id của tên miền, hosting...)  
**fromCreatedDate**: ngày tạo mới từ  
**toCreatedDate**: ngày tạo mới tới  

## [Chi tiết](#get)
Lấy thông tin chi tiết của giao dịch
> **API:** /api/rms/v1/transaction/detail
> **Phương thức:** POST  
> **Dữ liệu data body mẫu(JSON):**   
```
{
   "id": 0
}
```
**id (bắt buộc)**: id của giao dịch 

