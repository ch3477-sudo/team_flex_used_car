erDiagram
  DIM_BRAND ||--o{ FACT_CAR_LISTING : "has"

  DIM_BRAND {
    INT brand_id PK
    VARCHAR brand_name "UNIQUE"
  }

  FACT_CAR_LISTING {
    BIGINT listing_id PK
    INT brand_id FK
    VARCHAR model_name_raw
    INT year_int
    INT mileage_km
    INT price_manwon
    VARCHAR fuel_type
    VARCHAR region
    VARCHAR url
    BIGINT raw_id
    TIMESTAMP created_at
  }
