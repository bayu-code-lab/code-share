# API Specification

- - -
## Car Favorite
- - -
*  **Method** : `POST`
*  **Endpoint** : `/favorite`
*  **Request Body Parameter**:
```
{
  "sku_id": "33c18e25-a5bd-4f1c-af15-e6449fb2d7f1"
}
```
*  **Response** : 

On Success Adding:
```
{
  "status_code": 201,
  "data": {},
  "message": "Success Add to Favorite!"
}
```
On Success Removing
```
{
  "status_code": 200,
  "data": {},
  "message": "Success Remove from Favorite!"
}
```

- - -
## Car Model
- - -
*  **Method** : `GET`
*  **Endpoint** : `/model`
*  **Query Parameter** :
    *  brand_id: `optional`
*  **Response** :
```
{
  "status_code": 200,
  "data": [
    {
      "id": "70030aba-c0e4-43e4-aa19-33609a32b4b7",
      "desc": "KONA",
      "type_id": "f7b7c03d-4e2f-46e2-824b-e11f49fb261b"
    },
    {
      "id": "45c8fa44-7115-4cc4-b2f4-909b8d5fb426",
      "desc": "NEW TUCSON",
      "type_id": "8d7753c5-43b1-478c-8bde-80ff49ddc638"
    }
  ],
  "message": "Success Get Car Model Data!"
}
```

- - - 
## Car Brand
- - -
* **Method** : `GET`
* **Endpoint** : `/brand`
* **Response**:
```
{
  "status_code": 200,
  "data": [
    {
      "id": "392b0918-0983-4a81-a1b2-de2f258fcef7",
      "desc": "BMW"
    },
    {
      "id": "de256adc-504c-4d74-b593-57d165297d9a",
      "desc": "DFSK"
    }
  ],
  "message": "Success Get Brand Data!"
}
```

- - - 
## Car Location
- - -
* **Method** : `GET`
* **Endpoint** : `/location`
* **Response**:
```
{
  "status_code": 200,
  "data": [
    {
      "id": "fcffd444-40ff-4e56-b915-6fc937c30a81",
      "desc": "Bekasi"
    },
    {
      "id": "d04c230c-0edb-4107-8aa6-c551131d5596",
      "desc": "Bogor"
    }
  ],
  "message": "Success Get Car Location Data!"
}
```

- - - 
## Car Model-Type
- - -
* **Method** : `GET`
* **Endpoint** : `/model-type`
* **Query Parameter**:
    * type_id: `optional`
* **Response**:
```
{
  "status_code": 200,
  "data": [
    {
      "id": "46220e68-f2dc-4d3f-a84d-cb8d5f92763c",
      "desc": "City Car"
    },
    {
      "id": "4e5c11aa-61a2-4ffc-b062-5def025aa2bd",
      "desc": "Coupe"
    }
  ],
  "message": "Success Get Car Model Type Data!"
}
```

- - - 
## Car Fuel
- - -
* **Method** : `GET`
* **Endpoint** : `/fuel`
* **Response**:
```
{
  "status_code": 200,
  "data": [
    {
      "id": "1a5fe2f9-aaea-4275-acc0-df4c0aacff55",
      "desc": "Bensin"
    },
    {
      "id": "8a5138a8-c93c-46af-a629-b4f3172a5980",
      "desc": "Diesel"
    }
  ],
  "message": "Success Get Car Fuel Data!"
}
```

- - - 
## Car Transmission
- - -
* **Method** : `GET`
* **Endpoint** : `/transmission`
* **Response**:
```
{
  "status_code": 200,
  "data": [
    {
      "id": "e0dbf596-43c5-42c8-a0e7-4bc070339c3e",
      "desc": "Automatic"
    },
    {
      "id": "91a6e09f-afcd-4be9-a328-9d3633918d39",
      "desc": "Manual"
    }
  ],
  "message": "Success Get Car Transmission Data!"
}
```

- - -
## Car List
- - -
*  **Method** : `GET`
*  **Endpoint** : `/list`
*  **Query Parameter** :
    *  price_from: `optional`
    *  price_to: `optional`
    *  brand_id: `optional`
    *  model_id: `optional`
    *  type_id: `optional`
    *  year_from: `optional`
    *  year_to: `optional`
    *  odometer_from: `optional`
    *  odometer_to: `optional`
    *  transmission_id: `optional`
    *  fuel_id: `optional`
    *  location_id: `optional`
    *  sort_by: `optional`
    *  sort_value: `optional`
    *  skip: `optional`
    *  keyword: `optional`
*  **Response** :
```
{
  "status_code": 200,
  "data": {
    "total": 22,
    "skip": 0,
    "data": [
      {
        "sku_id": "f3f6befa-bf74-44e5-a143-9fbd2f0d5e88",
        "slug": "mercedes-benz-amg-e53-saloon-2018-d32121rwe",
        "title": "MERCEDES BENZ AMG E53 Saloon",
        "image_url": "staging/car/sku/image/f3f6befa-bf74-44e5-a143-9fbd2f0d5e88%20-%201/Xpander_exterior.png",
        "year": 2018,
        "odometer": 456,
        "location": "Bogor",
        "offering_price": 120000000,
        "monthly_installment": 120000,
        "is_certified": false,
        "is_booked": false,
        "is_sold": false,
        "is_favorite": false,
        "discount": 0,
        "whatsapp_url": "https://api.whatsapp.com/send?phone=62081218557236&text=Hallo, Sontoloyo Car"
      }
   ]
}
```

- - -
## Car Search
- - -
*  **Method** : `GET`
*  **Endpoint** : `/search`
*  **Query Parameter** :
    *  keyword: `optional`
*  **Response** :
```
{
  "status_code": 200,
  "data": [
    {
      "type": "brand",
      "data": [
        {
          "title": "MITSUBISHI",
          "brand_id": "674d7651-ffe3-4692-9869-2900f23d0528",
          "image_url": "sanity/car/brand/MTS/mitsubishi_144px.png"
        }
      ]
    },
    {
      "type": "variant",
      "data": [
        {
          "title": "MERCEDES BENZ AMG E53 Saloon",
          "slug": "mercedes-benz-amg-e53-saloon-2018-d32121rwe",
          "year_of_production": 2018,
          "odometer": 456,
          "location": "Bogor",
          "image_url": "sanity/dealer/branch/awderalt_144px.png"
        }
      ]
    }
  ],
  "message": "Success Get Car Suggestion Data!"
}
```

- - -
## Car Recommendation
- - -
*  **Method** : `GET`
*  **Endpoint** : `/search`
*  **Query Parameter** :
    *  type: `optional`
*  **Response** :
```
{
  "status_code": 200,
  "data": {
    "total": 22,
    "skip": 0,
    "data": [
      {
        "sku_id": "f3f6befa-bf74-44e5-a143-9fbd2f0d5e88",
        "slug": "mercedes-benz-amg-e53-saloon-2018-d32121rwe",
        "title": "MERCEDES BENZ AMG E53 Saloon",
        "image_url": "staging/car/sku/image/f3f6befa-bf74-44e5-a143-9fbd2f0d5e88%20-%201/Xpander_exterior.png",
        "year": 2018,
        "odometer": 456,
        "location": "Bogor",
        "offering_price": 120000000,
        "monthly_installment": 120000,
        "is_certified": false,
        "is_booked": false,
        "is_sold": false,
        "is_favorite": false,
        "discount": 0,
        "whatsapp_url": "https://api.whatsapp.com/send?phone=62081218557236&text=Hallo, Sontoloyo Car"
      }
    ]
  },
  "message": "Success Get Car List Data!"
}
```

- - -
## Car Detail
- - -
*  **Method** : `GET`
*  **Endpoint** : `/detail/`
*  **Query Parameter**:
    * slug: `required`
*  **Response** :
```
{
  "status_code": 200,
  "data": {
    "police_number": "ganjil",
    "offering_price": 120000000,
    "min_sales_price": 12000000,
    "discount": 0,
    "monthly_installment": 120000,
    "brand": "MERCEDES BENZ",
    "model": "AMG E53",
    "type_id": "abda94f6-1a6a-4376-bdd3-553d3af78359",
    "type": "LCGC",
    "variant": "Saloon",
    "year": 2018,
    "engine_capacity": 12314,
    "transmission": "Manual",
    "fuel": "Hybrid",
    "odometer": 456,
    "color": "ABU-ABU",
    "is_favorite": false,
    "is_certified": false,
    "is_certifcate_url": "",
    "branch_name": "Sontoloyo Car",
    "branch_whatsapp_url": "https://api.whatsapp.com/send?phone=62081218557236&text=Hallo, Sontoloyo Car",
    "branch_location_url": "https://goo.gl/maps/UWjS8WcwESrA8UzU9",
    "branch_city_desc": "Bogor"
  },
  "message": "Success Get Car Detail Data!"
}
```

- - -
## Car Condition
- - -
*  **Method** : `GET`
*  **Endpoint** : `/detail/condition`
*  **Query Parameter**:
    * slug: `required`
*  **Response** :
```
{
  "status_code": 200,
  "data": {
    "flood_free": true,
    "accident_free": true,
    "service_book": true,
    "manual_book": true,
    "bpkb_on_behalf": "Pribadi",
    "bpkb_address": "lipo",
    "kir_expired": "2001-04-01",
    "ownership_total": 2,
    "vehicle_registration_expired": "2021-04-29",
    "one_month_guarantee": false,
    "one_week_guarantee": false,
    "damage_free_engine": "aman",
    "engine_vibration": "aman",
    "exhaust_smoke": "aman",
    "power_steering_condition": "aman",
    "rpm_stable": "aman",
    "temperature": "aman",
    "accu_condition": "aman",
    "cable_condition": "aman sekali",
    "radiator_condition": "aman",
    "computer_diagnosed": "aman",
    "abnormal_sound": "aman",
    "steering_weight": "aman",
    "transmission": "aman",
    "brake": "aman",
    "suspension": "aman",
    "steering_balance": "aman",
    "ac_system": "aman",
    "air_bag": "aman",
    "test_drive_availability": false,
    "unit_availability": false,
    "is_certified": false,
    "certificate_url": ""
  },
  "message": "Success Get Car Condition Data!"
}
```

- - -
## Car Specification
- - -
*  **Method** : `GET`
*  **Endpoint** : `/detail/specification`
*  **Query Parameter**:
    * slug: `required`
*  **Response** :
```
{
  "status_code": 200,
  "data": {
    "air_bag": "Driver, Front Passenger & Curtain Airbag",
    "cruise_control": false,
    "antilock_breaking_system": true,
    "power_seat": false,
    "power_window": true,
    "air_conditioner": false,
    "layar_tv": false,
    "power_steering": false,
    "sunroof": false
  },
  "message": "Success Get Car Specification Data!"
}
```

- - - 
## Car Image
- - -
*  **Method** : `GET`
*  **Endpoint** : `/detail/image`
*  **Query Parameter**:
    * slug: `required`
*  **Response** :
```
{
  "status_code": 200,
  "data": [
    {
      "original": "staging/car/sku/image/f3f6befa-bf74-44e5-a143-9fbd2f0d5e88%20-%201/Xpander_exterior.png",
      "thumbnail": "staging/car/sku/image/f3f6befa-bf74-44e5-a143-9fbd2f0d5e88%20-%201/Xpander_exterior.png"
    },
    {
      "original": "staging/car/sku/image/f3f6befa-bf74-44e5-a143-9fbd2f0d5e88%20-%202/Xpander_exterior.png",
      "thumbnail": "staging/car/sku/image/f3f6befa-bf74-44e5-a143-9fbd2f0d5e88%20-%202/Xpander_exterior.png"
    }
  ],
  "message": "Success Get Car Image Data!"
}
```

- - -
## Car Similar
- - -
*  **Method** : `GET`
*  **Endpoint** : `/detail/similar`
*  **Query Parameter**:
    * model_type_id: `required`
*  **Response** :
```
{
  "status_code": 200,
  "data": {
    "total": 1,
    "skip": 0,
    "data": [
      {
        "sku_id": "82885e89-1d11-420e-a4cf-5bf927dd38e4",
        "slug": "suzuki-karimun-wagon-r-gs-r-gs-2020-m8734jgh",
        "title": "Suzuki KARIMUN WAGON R GS R GS",
        "image_url": "sanity/car/sku/image/82885e89-1d11-420e-a4cf-5bf927dd38e4%20-%201/Xpander_exterior.png",
        "year": 2020,
        "odometer": 34562,
        "location": "Tangerang Selatan",
        "offering_price": 100000000,
        "monthly_installment": 1000000,
        "is_certified": false,
        "is_booked": false,
        "is_sold": false,
        "is_favorite": false,
        "discount": 0,
        "whatsapp_url": "https://api.whatsapp.com/send?phone=62081218557236&text=Hallo, Tanggerang Car Show"
      }
    ]
  },
  "message": "Success Get Similar Car Data!"
}
```
