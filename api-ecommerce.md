--- Featured Categories
Hiển thị các categoy đặc trưng
•GET /categories
req: { }
res:
{
	“statuscode”: 200,
	“message”: “success”,
	“data”: [
            {
			        “id”: number,
			        “name”: “string”,
              "urlImg": "string",
			        "totalProduct": number,
            },
          ]
}
•Post /products/search
req: 
{ 
  "keyWord": "string",
  "pageSize": number,
  "categoryId": number[],
  "brandId": number[],
  "weight": number,
  "priceFrom": number,
  "priceTo": number,
  "conditionSort": number,
  "rating": number,
}
res:
{
  "statuscode": 200,
  "message": "success",
  "data": [
            "id": number,
            "name": "string",
            "urlImg": "string",
            "product": [
                          {
                            "id": number,
                            "description: "string",
                            "name": "string",
                            "brand": "string",
                            "weight": float,
                            "price" number,
                            "discount": number,
                            "quantity": number,
                            "categoryId": number,
                            "isDeleted": number,
                            "mainUrl": "string",
                            "vendorId": number,
                            "brandId": number,
                          },
                        ],
          ]
}
•GET /products/id
req: {}
res:  {
        "id": number,
        "description: "string",
        "name": "string",
        "brand": "string",
        "weight": float,
        "price" number,
        "discount": number,
        "quantity": number,
        "categoryId": number,
        "isDeleted": number,
        "mainUrl": "string",
        "images": [
          {
            "id": number,
            "url": "string",
            "productId": number
          },
        ]
        "vendorId": number,
        "brandId": number,
      }
•POST /cart
req: {
  "productId": number,
  "quantity": number, 
  "customerId": number
}
res:
Thêm thành công:
{
  “statuscode”: 200,
	“message”:  “success”,
}
Thêm thất bại:
{
  "statuscode": 401,
  "message": "failed when add to cart"
}
--- Popular Products
•GET /categories/popular
req: {}
res: 
{
	“statuscode”: 200,
	“message”:  “success”,
	“data”: [
            {
			        “id”: number,
			        “name”: “string”,
              "urlImg": "string",
			        “product”: [
                            {
                              "id": number,
                              "description: "string",
                              "name": "string",
                              "brand": "string",
                              "weight": float,
                              "price" number,
                              "discount": number,
                              "quantity": number,
                              "categoryId": number,
                              "isDeleted": number,
                              "mainUrl": "string",
                              "vendorId": number
                            },
                          ]
            },
          ],
}
•GET /products/popular
req: {}
res: 
{
  "statuscode": 200,
  "message": "success",
  "data": [
            {
              "id": number,
              "description: "string",
              "name": "string",
              "brand": "string",
              "weight": float,
              "price" number,
              "discount": number,
              "quantity": number,
              "categoryId": number,
              "isDeleted": number,
              "mainUrl": "string",
              "vendorId": number
            },
         
          ]
}
•GET /products/id
Giống ở trên
--- Daily Best Sells

--- Deal Of The Day
Lấy ra những product đang trong thời gian sale
•GET /products/on-sale
req: {}
res: 
{
  "statuscode": 200,
  "message": "success",
  "data": [
            {
              "id": number,
              "description: "string",
              "name": "string",
              "brand": "string",
              "weight": float,
              "price" number,
              "discount": number,
              "quantity": number,
              "categoryId": number,
              "isDeleted": number,
              "mainUrl": "string",
              "vendorId": number,
              "discountStartedTime": Date,
              "discountEndedTime": Date
            },
         
          ]
}
--- Top Selling 
Lấy ra 3 sản phẩm được sắp xếp giảm dần theo số lượng bán được 
•GET /products/top-selling
req: {}
res: 
{
  "statuscode": 200,
  "message": "success",
  "data": [
            {
              "id": number,
              "description: "string",
              "name": "string",
              "brand": "string",
              "weight": float,
              "price" number,
              "discount": number,
              "quantity": number,
              "categoryId": number,
              "isDeleted": number,
              "mainUrl": "string",
              "vendorId": number,
              "discountStartedTime": Date,
              "discountEndedTime": Date
            },
         
          ]
}
--- Trending Products
Lấy ra 3 sản phẩm có số lượng bán được nhiều nhất trong 3 ngày + lượt đánh giá > 4,5 sao
•GET /products/trending
req: {}
res: 
{
  "statuscode": 200,
  "message": "success",
  "data": [
            {
              "id": number,
              "description: "string",
              "name": "string",
              "brand": "string",
              "weight": float,
              "price" number,
              "discount": number,
              "quantity": number,
              "categoryId": number,
              "isDeleted": number,
              "mainUrl": "string",
              "vendorId": number,
              "discountStartedTime": Date,
              "discountEndedTime": Date
            },    
          ]
}
--- Recently added 
Lấy ra 3 sản phẩm mới nhất (đc thêm vào gần đây nhất)
•GET /products/recently-added
req: {}
res: 
{
  "statuscode": 200,
  "message": "success",
  "data": [
            {
              "id": number,
              "description: "string",
              "name": "string",
              "brand": "string",
              "weight": float,
              "price" number,
              "discount": number,
              "quantity": number,
              "categoryId": number,
              "isDeleted": number,
              "mainUrl": "string",
              "vendorId": number,
              "discountStartedTime": Date,
              "discountEndedTime": Date
            },
          ]
}
--- Top rated
Lấy ra 3 sản phẩm có lượt rate cao nhất
•GET /products/top-ratedreq: {}
res: 
{
  "statuscode": 200,
  "message": "success",
  "data": [
            {
              "id": number,
              "description: "string",
              "name": "string",
              "brand": "string",
              "weight": float,
              "price" number,
              "discount": number,
              "quantity": number,
              "categoryId": number,
              "isDeleted": number,
              "mainUrl": "string",
              "vendorId": number,
              "discountStartedTime": Date,
              "discountEndedTime": Date
            },
         
          ]
}
************************************************
--- Wishlist
• POST /wishlist
req: 
{
  "productId": number,
  "customerId": number
}
res:
Thêm thành công:
{
  “statuscode”: 200,
	“message”:  “success”,
}
Thêm thất bại:
{
  "statuscode": 401,
  "message": "failed when add to wishlist"
}
********************************************