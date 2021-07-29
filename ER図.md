```uml
@startuml







package "ECサイト" as target_system {

  entity "顧客マスク" as Entity01 <m_customers> {
  
  + customer_code [PK]
  
  --
  
  pass
  
  name
  
  address
  
  tel
  
  mail
  
  del_flag
  
  req date
  
  }
  
  
  
  
  
  
  
  entity "購入テーブル" as Entity02 <d_purchase> {
  
    + order_id [PK]
    
    --
    
    # customer_code [FK]
    
    purchase_date
    
    total_price
    
}





entity "購入詳細テーブル" as Entity03 <d_purchase_detail> {

  + order_id [PK]
  
  + datail_id [PK]
  
  --
  
  # item_code [FK]
  
  price
  
  num
  
}



entity "商品マスタ" as Entity04 <m_items> {

  +item_code [PK]
  
  --
  
  item_name
  
  price
  
  # category_id [FK]
  
  image
  
  detail
  
  del_flog
  
  reg_date
  
}



entity "カテゴリマスタ" as Entity05 <m_category> {

  +category_id [PK]
  
  --
  
  name
  
  reg_date
  
 }



}



Entity01 |o-ri-o{ Entity02

Entity02 ||-ri-|{ Entity03

Entity03 }-do-|| Entity04

Entitiy04 }o-le-|| Entity05







@enduml
```
