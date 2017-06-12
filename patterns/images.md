# Images over the ChurchSuite API

A number of our API endpoints provide a means of accessing the images related to a resource, e.g. contact, child or small group images. A sample response when requesting the JSON response for a small group may contain the following:

```json
{
  "id":"1",
  "reference":"1",
  "name":"West Bridgford",
  
  ...
  
  "images":{
    "thumb":{
      "px":128,
      "square":true,
      "mtime":1491208583,
      "url":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_thumb.jpg"
    },
    "sm":{
      "px":256,
      "square":false,
      "mtime":1491208583,
      "url":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_sm.jpg"
    },
    "md":{
      "px":512,
      "square":false,
      "mtime":1491208583,
      "url":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_md.jpg"
    },
    "lg":{
      "px":1024,
      "square":false,
      "mtime":1491208583,
      "url":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_lg.jpg"
    },
  },
  
  ...
  
}
```

The images are sized/proportioned as follows:
* `thumb` 128x128px square image. A square cropped version of image that was originally uploaded.
* `sm` 256px wide image. A width-resized version of the image that was originally uploaded.
* `md` 512px wide image. A width-resized version of the image that was originally uploaded.
* `lg` 1024px wide image. A width-resized version of the image that was originally uploaded.

## Deprecated image properties

For backwards compatibility, we also provide the following properties against the images object. Support for these image properties was deprecated in March 2017 and they should no longer be used.

```json
{
  "id":"1",
  "reference":"1",
  "name":"West Bridgford",
  
  ...
  
  "images":{
    "original_16":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_thumb.jpg",
    "original_100":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_sm.jpg",
    "original_500":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_md.jpg",
    "original_1000":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_lg.jpg",
    "square_16":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_thumb.jpg",
    "square_100":"https:\/\/cdn.churchapp.org\/demo\/smallgroups\/groups\/1_ZqHg09Wp_thumb.jpg"
  },
  
  ...
  
}
```