# Section 8 MLS Auto-Search — Miami-Dade

Herramienta para realtors que automatiza la búsqueda de propiedades en el MLS de Miami-Dade que califican para Sección 8, filtrando por Payment Standards 2024 de HUD.

## Estructura
```
scripts/scraper.py          ← Motor de búsqueda (configura en config.py)
dashboard/index.html        ← Dashboard web
data/payment_standards_2024.json  ← FMR HUD por ZIP
config.py                   ← Todos los filtros
```

## Instalación
```bash
git clone https://github.com/Esterfrndz/Section8-mls-miami-.git
cd Section8-mls-miami-
pip install -r requirements.txt
cp .env.template .env
# Edita .env con tus credenciales Spark API
python scripts/scraper.py
```

## Dashboard
```bash
python -m http.server 8080
# Abre: http://localhost:8080/dashboard/
```

## Cómo obtener acceso Spark API
1. Entra a mmls.com → Member Services → API Access
2. Solicita acceso a la Spark API (3–5 días hábiles)
3. Recibirás SPARK_CLIENT_ID y SPARK_CLIENT_SECRET

## Licencia
MIT — uso libre para fines personales y comerciales.
