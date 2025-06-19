# RestBase

**RestBase** is a Python-based tool that allows you to fetch data from any REST API and sync it directly into a PostgreSQL database. It intelligently infers the schema from JSON responses and creates tables dynamically. Designed with automation, flexibility, and developer ease-of-use in mind, RestBase is perfect for data ingestion, analytics, or prototyping workflows.

---

## 🚀 Features

- ✅ Interactive config builder (no manual YAML editing)
- 🌐 Supports query parameters per endpoint
- 🔍 Auto-infers table schema from API JSON responses
- 📦 Inserts nested JSON as `JSONB` fields in PostgreSQL
- 🛠 Creates tables automatically, only if they don't exist
- ⚡ Fast and simple CLI usage

---

## 📦 Installation

### Install from source
```bash
pip install .
```

### Install in editable (dev) mode
```bash
pip install -e .
```

---

## 🔧 Usage

### Run as CLI
```bash
restbase
```

### Or use as Python module
```bash
python -m restbase
```

### First time?
The tool will automatically prompt you to configure:
- API base URL and endpoints (with query params)
- PostgreSQL connection credentials

A `config.yaml` file will be generated.

---

## 🧪 Example `config.yaml`
```yaml
api:
  base_url: https://api.openbrewerydb.org/v1
  headers: {}
  endpoints:
    - path: /breweries
      params:
        by_city: san_diego
postgres:
  host: localhost
  port: 5432
  dbname: restbase_db
  user: postgres
  password: secret
```

---

## 🧰 Tech Stack
- Python 3.7+
- PostgreSQL
- `requests`, `psycopg2-binary`, `PyYAML`

---

## 📝 License
This project is licensed under the [MIT License](LICENSE).

---

## 🙋 Contributing
Pull requests are welcome. If you'd like to contribute new features or improve the project, feel free to fork and submit a PR.

---

## 📫 Contact
Made with ❤️ by Soumyadeep. Reach me at [soumyadeep.das423@gmail.com].
