## ERD (논리 구조)

- dim_brand (1) --- (N) fact_car_listing
- brand_id → brand_name
- fact_car_listing은 브랜드를 FK로 참조

```mermaid
erDiagram
  DIM_BRAND ||--o{ FACT_CAR_LISTING : has
  DIM_BRAND {
    INT brand_id PK
    VARCHAR brand_name
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
  }
