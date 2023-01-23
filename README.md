# Instalacion-Open-Hab
Descripción de procedimiento para instalar Open Hab

En este repositorio se hace la instalación de openhab

Recomendaciones para el entendimiento del ejercicio

-Leer la documentación de openhab:

https://www.openhab.org/docs/installation/linux.html

Instalación de openhab
Se ejecutan lo siuientes comandos de manera ordenada:

-curl -fsSL "https://openhab.jfrog.io/artifactory/api/gpg/key/public" | gpg --dearmor > openhab.gpg

-sudo mkdir /usr/share/keyrings

-sudo mv openhab.gpg /usr/share/keyrings

-sudo chmod u=rw,g=r,o=r /usr/share/keyrings/openhab.gpg

Posteriormente se ejecuta el siguiente comando:

echo 'deb [signed-by=/usr/share/keyrings/openhab.gpg] https://openhab.jfrog.io/artifactory/openhab-linuxpkg stable main' | sudo tee /etc/apt/sources.list.d/openhab.list

Finalmente se actualiza y se intsala:

-sudo apt-get update

-sudo apt-get install openhab
