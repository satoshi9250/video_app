# README

## users table​
|Column|Type|Options|
|------|----|-------|
|nickname|string|null: false|
|password|string|null:false|
|email|string|null:false|

### Association
- has_many :posts

## posts table
|Column|Type|Options|
|------|----|-------|
|body|integer|null:text|
|youtube_url|string|null:false|
|user_id|integer|null:fales|

### Association
- belongs_to :user
- has_many :comments


## comment table
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null:false|
|post_id|integer|null:false|
|text|text|null: false|

### Association
- belongs_to :post
- belongs_to :user