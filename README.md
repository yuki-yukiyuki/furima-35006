# README


## usersテーブル  
|Column|Type|Options|  
|------|----|-------|  
|email|string|null: false|  
|password|string|null: false|  
|name|string|null: false|  
|nickname|string|null: false|  

### Association

- has_many :items

## itemsテーブル  
|Column|Type|Options|  
|------|----|-------|  
|item_name|string|null: false|  
|description|text|null: false|   
|category|string|null: false|  
|status|string|null: false|  
|price|string|null: false|
|burden|string|null: false|
|aria|string|null: false|
|day|string|null: false|

### Association

- has_one :shopping_adress
- belongs_to :user

## buyersテーブル
|Column|Type|Options|  
|------|----|-------|  
|card_info|string|null: false|  

### Association

- belongs_to :shopping_adress

## shopping_adressesテーブル  
|Column|Type|Options|  
|------|----|-------|  
|post|string|null: false|  
|prefectures|string|null: false|  
|city|string|null: false|  
|number|string|null: false|  
|tel|string|null: false|  

### Association

- has_one :buyer  
- belongs_to :shopping_adress

