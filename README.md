# TravelTip

A simple web app for saving and managing favorite travel locations on a map.

## Description
TravelTip lets users keep a list of locations, view them on a map, and manage them easily.

## Main Features
- Save and manage locations
- Search for an address and move the map to that place
- Find the user's current location
- View the creation and update time for each location
- Filter locations by time range: last day, last week, last month, or last year
- Sort and filter locations by text and rating

## Location Actions
- Create: click on the map and enter a name and rating
- Read: view the selected location details
- Update: change the location rating
- Delete: before removing a location, the app asks: "Are you sure you want to remove this location?"
- List: see all saved locations with filtering, sorting, and grouping

## Selected Location
When a location is selected, the app shows:
- the location name
- the address
- the rating
- a marker on the map
- the current URL in the clipboard area
- sharing options through the browser

## Location Object Example
```js
{
  id: 'GEouN',
  name: 'Dahab, Egypt',
  rate: 5,
  geo: {
    address: 'Dahab, South Sinai, Egypt',
    lat: 28.5096676,
    lng: 34.5165187,
    zoom: 11
  },
  createdAt: 1706562160181,
  updatedAt: 1706562160181
}
```

## Services
```js
export const locService = {
  query,
  getById,
  remove,
  save,
  setFilterBy,
  setSortBy,
  getLocCountByRateMap
}

export const mapService = {
  initMap,
  getPosition,
  setMarker,
  panTo,
  lookupAddressGeo,
  addClickListener
}
```

## Controller
```js
window.app = {
  onRemoveLoc,
  onUpdateLoc,
  onSelectLoc,
  onPanToUserPos,
  onSearchAddress,
  onCopyLoc,
  onShareLoc,
  onSetSortBy,
  onSetFilterBy
}
```

## Example Usage
```html
<button onclick="app.onCopyLoc()">Copy location</button>
<button onclick="app.onShareLoc()">Share location</button>
```


