```
/me/media
```

```
{
  "data": [
    {
      "id": "18072263594487931"
    }
  ],
  "paging": {
    "cursors": {
      "before": "QVFIUzJRUkJVSVRJOVhzd3Vra19OLUlaZAnphZAzQyVHA4NUIzMTk2a29YNHNvcnBsTW1HNzRYN3RabkdOelhjdVJuMnZAXN08teE02eTRIY2xXbXBsV0FlMFZA3",
      "after": "QVFIUzJRUkJVSVRJOVhzd3Vra19OLUlaZAnphZAzQyVHA4NUIzMTk2a29YNHNvcnBsTW1HNzRYN3RabkdOelhjdVJuMnZAXN08teE02eTRIY2xXbXBsV0FlMFZA3"
    }
  }
}
```

[https://developers.facebook.com/docs/instagram-platform/reference/instagram-media](https://developers.facebook.com/docs/instagram-platform/reference/instagram-media "https://developers.facebook.com/docs/instagram-platform/reference/instagram-media")

```
me/media?fields=comments_count,id,like_count,permalink,shortcode
```

```
{
  "data": [
    {
      "comments_count": 7,
      "id": "18072263594487931",
      "like_count": 1,
      "permalink": "https://www.instagram.com/p/DNVeA2es1al/",
      "shortcode": "DNVeA2es1al",
      "username": "sentilens.io"
    }
  ],
  "paging": {
    "cursors": {
      "before": "QVFIUzJRUkJVSVRJOVhzd3Vra19OLUlaZAnphZAzQyVHA4NUIzMTk2a29YNHNvcnBsTW1HNzRYN3RabkdOelhjdVJuMnZAXN08teE02eTRIY2xXbXBsV0FlMFZA3",
      "after": "QVFIUzJRUkJVSVRJOVhzd3Vra19OLUlaZAnphZAzQyVHA4NUIzMTk2a29YNHNvcnBsTW1HNzRYN3RabkdOelhjdVJuMnZAXN08teE02eTRIY2xXbXBsV0FlMFZA3"
    }
  }
}
```

## Istotne pola

### comments_count

Public

Count of comments on the media. Excludes comments on album child media and the media's caption. Includes replies on comments.

### id

Public

Media ID.

### like_count

Count of likes on the media, including replies on comments. Excludes likes on album child media and likes on promoted posts created from the media.

If queried indirectly through another endpoint or field expansion the like_count field is omitted if the media owner has hidden like counts.

### permalink

Public

Permanent URL to the media.

_Zawiera shortcode w sobie_

### shortcode

Public

Shortcode to the media.

```
me/media?fields=comments_count,id,like_count,permalink,shortcode,view_count,media_url,thumbnail_url
```