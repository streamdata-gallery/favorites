swagger: "2.0"
x-collection-name: Flickr
x-complete: 1
info:
  title: Flickr
  description: explore-upload-and-organize-photos-on-flickr
  version: 1.0.0
host: api.flickr.com
basePath: /services/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/?method=flickr.favorites.add:
    get:
      summary: Favorites Add
      description: Adds a photo to a user's favorites list.
      operationId: getRestMethodFlickr.favorites.add
      x-api-path-slug: restmethodflickr-favorites-add-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      - in: query
        name: photo_id
        description: The id of the photo to add to the users favorites
      responses:
        200:
          description: OK
      tags:
      - Favorites
      - Add
  /rest/?method=flickr.favorites.getList:
    get:
      summary: Favorites Get List
      description: Returns a list of the user's favorite photos. Only photos which
        the calling user has permission to see are returned.
      operationId: getRestMethodFlickr.favorites.getlist
      x-api-path-slug: restmethodflickr-favorites-getlist-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: extras
        description: A comma-delimited list of extra information to fetch for each
          returned record
      - in: query
        name: format
        description: Response format
      - in: query
        name: max_fave_date
        description: Maximum date that a photo was favorited on
      - in: query
        name: min_fave_date
        description: Minimum date that a photo was favorited on
      - in: query
        name: page
        description: The page of results to return
      - in: query
        name: per_page
        description: Number of photos to return per page
      responses:
        200:
          description: OK
      tags:
      - Favorites
      - GetList
  /rest/?method=flickr.favorites.getPublicList:
    get:
      summary: Favorites Get Public List
      description: Returns a list of favorite public photos for the given user.
      operationId: getRestMethodFlickr.favorites.getpubliclist
      x-api-path-slug: restmethodflickr-favorites-getpubliclist-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: extras
        description: A comma-delimited list of extra information to fetch for each
          returned record
      - in: query
        name: format
        description: Response format
      - in: query
        name: max_fave_date
        description: Maximum date that a photo was favorited on
      - in: query
        name: min_fave_date
        description: Minimum date that a photo was favorited on
      - in: query
        name: page
        description: The page of results to return
      - in: query
        name: per_page
        description: Number of photos to return per page
      - in: query
        name: user_id
        description: The user to fetch the favorites list for
      responses:
        200:
          description: OK
      tags:
      - Favorites
      - GetPublicList
  /rest/?method=flickr.favorites.remove:
    get:
      summary: Favorites Remove
      description: Adds a photo to a user's favorites list.
      operationId: getRestMethodFlickr.favorites.remove
      x-api-path-slug: restmethodflickr-favorites-remove-get
      parameters:
      - in: query
        name: api_key
        description: Your API application key
      - in: query
        name: format
        description: Response format
      - in: query
        name: photo_id
        description: The id of the photo to remove to the users favorites
      responses:
        200:
          description: OK
      tags:
      - Favorites
      - Remove