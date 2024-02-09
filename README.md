# GeoLookup
This API is designed to be integrated into your project, allowing you to retrieve geographical information of a client by placing their IP in the URL, as well as yours by omitting the IP. It is 100% free and is integrated into a free project without any limitations for the developer community.
#API Documentation

## Get User/Client Infos

### Get user/or client information by their IP address

- **Endpoint**: `GET /api-v1/<ip-adresse>`
- **Description**: Retrieves detailed user / client information based on their IP address.
- **Query parameters**:
  -None (The user's IP address is automatically detected in the URL and if missed it will return your own information)
- **Example query**:
- Example 1( provide an IP address)
  ```http
  GET https://api.ipgeolookup.jconceptiom.com/api-v1/181.174.87.53
  {
    "city": "Guatemala City",
    "continent_code": "NA",
    "continent_name": "North America",
    "country_code": "GT",
    "country_name": "Guatemala",
    "dma_code": null,
    "is_in_european_union": false,
    "latitude": 14.6343,
    "longitude": -90.5155,
    "postal_code": "01012",
    "region": "GU",
    "time_zone": "America/Guatemala"
  }
- Example 1( without an IP address)
   ```http
  GET https://api.ipgeolookup.jconceptiom.com/api-v1/
   {
      "city": "Lomé",
      "continent_code": "AF",
      "continent_name": "Africa",
      "country_code": "TG",
      "country_name": "Togo",
      "dma_code": null,
      "is_in_european_union": false,
      "latitude": 6.1316,
      "longitude": 1.224,
      "postal_code": null,
      "region": "M",
      "time_zone": "Africa/Lome"
   }
