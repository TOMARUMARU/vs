## *Theme*

### association

` has_one :FirstPosition,dependent: :destroy `
` has_one :SecoundPosition, dependent: :destroy `
` has_many :Likes, dependent: :destroy `


### table

|カラム名|型|オプション|
|:--|--:|:--:|
|name|string|null false|
|likes_count|integer|default: 0|


## *FirstPosition*

### association

` has_many :Likes, dependent: :destroy `
` has_many :Bads, dependent: :destroy `
` belongs_to :Theme`


### table

|カラム名|型|オプション|
|:--|--:|:--:|
|comment|text|null false|
|theme_id|references|foreign_key true|
|likes_count|integer|default: 0|
|bads_count|integer|default: 0|

## *SecoundPosition*

### association

` has_many :Likes, dependent: :destroy `
` has_many :Bads, dependent: :destroy `
` belongs_to :Theme`


### table

|カラム名|型|オプション|
|:--|--:|:--:|
|comment|text|null false|
|theme_id|references|foreign_key true|
|likes_count|integer|default: 0|
|bads_count|integer|default: 0|

## *Like*

### association

` belongs_to :Theme`
` belongs_to :FirststPosition`
` belongs_to :SecuondPosition`
` counter_cache: likes_count `

### table

|カラム名|型|オプション|
|:--|--:|:--:|
|theme_id|references|foreign_key true|
|first_position_id|references|foreign_key true|
|secound_position_id|references|foreign_key true|

## *Bad*

### association

` belongs_to :Theme`
` belongs_to :FirststPosition`
` belongs_to :SecuondPosition`
` counter_cache: bads_count `

### table

|カラム名|型|オプション|
|:--|--:|:--:|
|theme_id|references|foreign_key true|
|first_position_id|references|foreign_key true|
|secound_position_id|references|foreign_key true|
