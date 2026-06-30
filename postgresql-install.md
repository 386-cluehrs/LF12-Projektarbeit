# PostgreSQL

## Befehle Raspberry PI

```bash
sudo apt update
```

```bash
sudo apt install postgresql postgresql-contrib -y
```

```bash
sudo -u postgres psql
```

```bash
\password postgres (Passwort z.b. postgres)
\q
```

```bash
sudo -u postgres createdb raum_monitoring
```

```bash
sudo -u postgres psql -d raum_monitoring
```

```bash
psql -version
```

```bash
sudo nano /etc/postgresql/XX/main/postgresql.conf (XX durch versionsnr. ersetzen)
```


    # listen_addresses = 'localhost' 🡪 listen_addresses = '\*'


`Strg + S`
`Strg + X`

```bash
sudo nano /etc/postgresql/XX/main/pg_hba.conf (XX durch versionsnr. ersetzen)
```

```bash
ganz unten hinzufügen: host all all 0.0.0.0/0 md5
```

`Strg + S`
`Strg + X`

```bash
sudo ufw allow 5432/tcp
```

```bash
sudo systemctl restart postgresql
```

## Vorteile

- Einfach zu installieren
- nutzt SQL
- schnell mit daten

## Nachteile

- keine
- Ahnung