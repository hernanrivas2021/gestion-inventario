FROM python:3.11-slim

WORKDIR /app

RUN apt-get update && apt-get install -y \
    default-libmysqlclient-dev \
    gcc \
    pkg-config \
    && rm -rf /var/lib/apt/lists/*

COPY requirements.txt .
RUN pip install -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["python", "main.py"]
```

**5.** Clic en **"Commit changes"** → **"Commit directly to master"**

---

## También creá requirements.txt si no existe

**"Add file"** → **"Create new file"** → nombre: `requirements.txt`
```
Django>=4.2
gunicorn
Pillow
python-dotenv
mysqlclient
