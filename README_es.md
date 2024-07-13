# Dell PowerEdge R730 Family Fan Control Script

## Descripción

Este script de Bash ajusta automáticamente las velocidades de los ventiladores de los servidores Dell PowerEdge R730 en función de la temperatura ambiente y de los procesadores. El objetivo es reducir el ruido del servidor mientras se asegura que las temperaturas se mantengan en niveles seguros.

## Funcionalidades

- **Control automático de los ventiladores**: Ajusta la velocidad de los ventiladores según la temperatura ambiente.
- **Prioridad en la temperatura de los procesadores**: Si cualquiera de los procesadores alcanza una temperatura crítica, se activa el modo automático de los ventiladores independientemente de la temperatura ambiente.
- **Rangos de temperatura y velocidades**:
  - 0 a 14 grados: 20%
  - 15 a 19 grados: 40%
  - 20 a 26 grados: 60%
  - 27 a 30 grados: 80%
  - Más de 30 grados: Activación del modo automático

## Requisitos

- Servidor Dell PowerEdge R730
- Sistema operativo Linux (Probado y funciona perfectamente en Proxmox)
- `ipmitool` instalado

## Instalación

Instale `ipmitool` en su sistema:

```sh
sudo apt-get install ipmitool
