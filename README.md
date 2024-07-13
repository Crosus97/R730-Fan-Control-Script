# Dell PowerEdge R730 Family Fan Control Script

## Descripción

Este script de Bash ajusta automáticamente las velocidades de los ventiladores del servidor Dell PowerEdge R730XD en función de la temperatura ambiente y la temperatura de los procesadores. El objetivo es reducir el ruido del servidor mientras se asegura que las temperaturas se mantengan en niveles seguros.

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

- Servidor Dell PowerEdge R730XD
- `ipmitool` instalado
- Acceso a la IPMI del servidor con las credenciales correspondientes

## Uso

1. Clone este repositorio:
    ```sh
    git clone https://github.com/Crosus97/r730-fan-control.git
    cd r730-fan-control
    ```

2. Modifique el script `fan_control.sh` con sus credenciales IPMI y dirección IP.

3. Haga el script ejecutable:
    ```sh
    chmod +x fan_control.sh
    ```

4. Ejecute el script:
    ```sh
    ./fan_control.sh
    ```

## Contribución

¡Las contribuciones son bienvenidas! Si tiene alguna mejora o encuentra un error, por favor abra un issue o envíe un pull request.
