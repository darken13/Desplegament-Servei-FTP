# Servidor FTP corporatiu amb Docker i vsftpd

Aquest projecte desplega un servidor FTP utilitzant Docker i vsftpd. El servei permet la gestió d’usuaris autenticats, accés anònim controlat i suporta els modes de connexió actiu i passiu.

## Requisits previs
- Docker Desktop instal·lat
- Docker Compose
- PowerShell a Windows
- Connexió a Internet

## Estructura del projecte
```text
ftp-project/
├── config/
│   └── vsftpd.conf
├── data/
│   ├── public/
│   └── users/
├── logs/
├── Dockerfile
└── docker-compose.yml
```

## Desplegament del servei
**Accedeix al directori del projecte**

```text
cd ftp-project
```

**Construeix la imatge Docker amb el servidor FTP**

`docker-compose build`

**Inicia el servei FTP en segon pla**

`docker-compose up -d`

**Comprova que el contenidor està en execució i actiu**

`docker ps`

## Accés al servidor FTP

**Es recomana utilitzar un client FTP dedicat com FileZilla**

**Dades de connexió:**
- Host: 127.0.0.1
- Port: 21
- Usuari: empleat1
- Contrasenya: Emp2024!

## Aturar el servei

**Atura i elimina el contenidor FTP**

`docker-compose down`

## Notes finals
- L'accés anònim només permet la descàrrega de fitxers.
- El mode passiu és el més recomanat per evitar problemes de connexió.
- Per a entorns reals, és millor utilitzar protocols més segurs com FTPS o SFTP.
