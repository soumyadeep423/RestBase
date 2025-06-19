# RestBase

[![Python](https://img.shields.io/badge/restbase-cli)](https://pypi.org/project/restbase-cli/)
[![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![GitHub Repo](https://img.shields.io/badge/github-repo-black?logo=github)](https://github.com/soumyadeep423/RestBase)

**RestBase** is a Python-based CLI tool that lets you fetch data from any REST API and sync it directly into a PostgreSQL database. It automatically infers table schemas from JSON responses, creates tables, and inserts data — no SQL or ORM required.

---

## 🚀 Features

- 🌐 Query parameter support per endpoint
- 🔍 Automatic schema inference from JSON
- 📦 Nested JSON handled as `JSONB` columns
- 🛠 Table creation only if not already present
- ⚡ Fast, minimal CLI
- ✅ Interactive config builder (no manual editing)

---

## 📦 Installation

Install directly from [PyPI](https://pypi.org/project/restbase-cli):

```bash
pip install restbase-cli
````

---


```bash
restbase
```

### Or via Python module

```bash
python -m restbase
```

---

## 🛠 First-Time Setup

When you first run `restbase`, it will ask you for:

* API base URL and endpoints
* Optional query parameters
* PostgreSQL credentials

This generates a `config.yaml` file used for syncing.

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

## 🔧 Tech Stack

* Python 3.7+
* PostgreSQL
* Libraries: `requests`, `psycopg2-binary`, `PyYAML`

---

## 🙋 Contributing

Pull requests are welcome!

To run the project locally:

```bash
git clone https://github.com/soumyadeep423/restbase-cli.git
cd restbase-cli
pip install .
pip install -e . #edit mode
restbase
```

---

## 📝 License

Licensed under the [MIT License](LICENSE).

---

## 📫 Author

**Soumyadeep Das**
GitHub: [@soumyadeep423](https://github.com/soumyadeep423)

---
