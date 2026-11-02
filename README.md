# FactoryPulse Dashboard

> Read-only operational dashboard for the FactoryPulse reference platform.

The dashboard visualises validated asset health, pipeline quality and explainable anomaly events from the FactoryPulse API. It ships with a static demo snapshot so it can be reviewed without infrastructure, and it can connect to a deployed API with `?api=https://your-api.example`.

## What it demonstrates

- Responsive, accessible operations UI with a deliberately read-only boundary.
- Clear data lineage from ingestion to lakehouse, intelligence and API.
- Explainable anomaly feed — reasons and scores instead of opaque alert labels.
- Static deployment with no API key, account or hidden back end.

## Run locally

Serve `dist/` with any static server, for example:

```bash
python -m http.server 8080 --directory dist
```

Open `http://127.0.0.1:8080`. To use a real FactoryPulse API, open:

```text
http://127.0.0.1:8080/?api=http://127.0.0.1:8000
```

## Safety boundary

This dashboard never issues commands to equipment and must not be used as a safety or control system. It is an observability and review interface for a simulated reference platform.

## Deployment

The repository is configured as a static Sites project. The published version uses the included demo snapshot; connect a production API only after adding authentication, CORS policy, access control and operational review.
