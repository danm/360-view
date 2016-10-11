# 360-view
360 Proof of concept

## Development

There are a couple of things you need add to your code to integrate the 360 viewer

### Create API Key


### Add async defer
```html
<script async defer
  src="https://maps.googleapis.com/maps/api/js?key=9buwD14MW-Wj7J1sZs&callback=initialize">
</script>
```
### Add script
```html
<script>
  var panorama;
  function initialize() {
    panorama = new google.maps.StreetViewPanorama(
    document.getElementById('street-view'),
      {
        position: {lat: 51.5122851, lng: -0.212135},
        pov: {heading: 70, pitch: 0},
        zoom: 1,
        panControl: false,
        zoomControl: false,
        addressControl: false,
        fullscreenControl: false,
        motionTrackingControl: false,
        enableCloseButton: false,
        linksControl: false
      }
    );
  }
</script>
```

### Add to body
```html
<div id="street-view"></div>
```
