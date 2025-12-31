# Dotfiles

Configuraciones personales de:
- Zsh + Oh My Zsh
- Kitty
- Alacritty
- Zellij

## Restaurar
Copiar cada carpeta a `~/.config` y `.zshrc` al home.

## i3

### Instalación
~~~
sudo apt update
sudo apt install i3-wm i3status i3lock xbacklight feh
~~~

i3 te está diciendo:

“No tienes configuración todavía
¿Quieres que genere una en ~/.config/i3/config?”

Opciones:
- Enter → generar config básica
- Esc → usar defaults internos (NO recomendado)

#### QUÉ DEBES HACER (recomendado)
👉 PRESIONA Enter
✔️ Sí, genera el config

¿Por qué?
- Te crea un config base funcional
- Sirve como plantilla

Luego te preguntará la tecla MOD

Cuando salga esto:

> Select modifier key

Elige:
👉 Super (Windows key)

Es el estándar:
- Docs
- Videos

#### dmenu
Method 1: Using APT (Recommended for most users)
bash
~~~
sudo apt update
sudo apt install suckless-tools
~~~
This installs dmenu along with dwm, st, etc. from the Debian repositories, providing a stable, pre-configured version.         


## Nerdfont
1️⃣ Descomprime el zip

Ve a donde tengas el archivo:

cd ~/Descargas
unzip NombreDeLaNerdFont.zip


Si no tienes unzip:

sudo apt install unzip

2️⃣ Crea la carpeta de fuentes del usuario
mkdir -p ~/.local/share/fonts

3️⃣ Copia solo los .ttf / .otf
cp *.ttf ~/.local/share/fonts/
# o
cp *.otf ~/.local/share/fonts/


Si el zip trae subcarpetas:

find . -name "*.ttf" -exec cp {} ~/.local/share/fonts/ \;

4️⃣ Actualiza la caché de fuentes
fc-cache -fv

5️⃣ Verifica que esté instalada
fc-list | grep -i nerd

## Picom
Para instalar Picom en Debian 13 (Trixie), primero
actualiza tu sistema y luego usa sudo apt install picom
