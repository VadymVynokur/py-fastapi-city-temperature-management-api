# City & Temperature API

FastAPI project for managing cities and temperature history. Fully asynchronous and using the real [WeatherAPI](https://www.weatherapi.com/).


## Configuration

Create a `.env` file:

```env
WEATHER_API_KEY=your_weatherapi_key
```

## Run

```bash
uvicorn app.main:app --reload
```

API access: `http://127.0.0.1:8000`

## Endpoints

### Cities

* `POST /cities` — add a city
* `GET /cities` — list all cities
* `DELETE /cities/{city_id}` — delete a city

### Temperatures

* `POST /temperatures/update` — update temperatures for all cities
* `GET /temperatures` — get all temperature records
* `GET /temperatures?city_id={id}` — get temperature history for a specific city

## Features

* Fully asynchronous (`asyncio`, `httpx`, `SQLAlchemy Async`)
* Real WeatherAPI integration
* Lifespan used instead of deprecated `on_event`
* SQLite for simplicity
