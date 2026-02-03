# Late::InstagramPlatformDataUserTagsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **username** | **String** | Instagram username (@ symbol is optional and will be removed automatically) |  |
| **x** | **Float** | X coordinate position from left edge (0.0 &#x3D; left, 0.5 &#x3D; center, 1.0 &#x3D; right) |  |
| **y** | **Float** | Y coordinate position from top edge (0.0 &#x3D; top, 0.5 &#x3D; center, 1.0 &#x3D; bottom) |  |

## Example

```ruby
require 'late'

instance = Late::InstagramPlatformDataUserTagsInner.new(
  username: friend_username,
  x: 0.5,
  y: 0.5
)
```

