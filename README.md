# retropie_bgm
Retropie Backgroud Music

## 1. Instalar pygame

(sólo si aún no está instalado)
```
sudo apt-get install python-pygame
```

## 2. Instalar el script de música

Descargar el archivo bgmusic.py
```
wget -q -O /hope/pi/bgmusic.py https://raw.githubusercontent.com/egrueda/retropie_bgm/master/bgmusic.py
```

Hacer el script ejecutable
```
chmod +x /hope/pi/bgmusic.py
```

## 3. Instalar el script de inicio

Descargar e instalar el script de inicio
```
wget -q -O bgmusic.service https://raw.githubusercontent.com/egrueda/retropie_bgm/master/bgmusic.service
mv bgmusic.service /etc/systemd/system/bgmusic.service
```

Iniciar el script
```
sudo systemctl daemon-reload
sudo systemctl start bgmusic.service
```

Si ha funcionado el paso anterior, habilitar el arranque automático
```
sudo systemctl enable bgmusic.service
```
