# **Resumen General de Configuración**
***
## General
* ### Router
    * Nombre de Host: R-Chis
    * Nombre de Dominio: r-chis.com
    * Timestamps: Habilitado
    * Banners Personalizados
* ### Switches
    * Nombre de Hosts: Sw10/Sw20
    * Nombre de Dominio: r-mor.com
    * Timestamps: Habilitado
    * Reloj Configurado
    * Banners Personalizados
## Seguridad
* ### Acceso
    * Usuario SSH: chisadmin
    * Contraseñas
    	* SSH: chis4dm1n!
    	* Consola: r-chisc0n!
        * Exec: rchis3x3c!
* ### Router
    * Longitud de Contraseñas: 8 Carácteres
    * Tiempo de Inactividad Máximo: 5 Mins
    * Cifrado de Contraseñas
    * **Login**
        * Intentos: 3
        * Dentro de: 15 segundos
        * Tiempo de Bloqueo: 2 Minutos
    * **Syslog**
        * Información registrada: Tabla de Enrutamiento
        * Servidor: 172.16.78.3
    * Modo Resiliente
    * **SSH**
        * Versión: 2
        * Longitud de Bits: 768
        * Acceso con Usuario y Contraseña
* ### **Switches** 
    * Tiempo de Inactividad Máximo: 5 Mins
    * Cifrado de Contraseñas
    * **Syslog**
        * Información Registrada: Paquetes ICMP
        * Servidor: 172.16.78.3
    * **SSH**
        * Versión: 2
        * Longitud de Bits: 768
        * Acceso con Usuario y Contraseña
    * **Port Security**
        * Puertos sin usar Deshabilitados
## Enrutamiento
* ### Router
    * Primer IP en Redes Internas
    * Enrutamiento IPv4
    * **OSPF**
        * Versión: 2
        * ID de Proceso: 100
        * Tipo de Área: Única (0)
        * Interfaces Pasivas: Gigabit Ethernet 0/0/0 - 0/0/1
        * **Redes Anunciadas**
            * 172.16.78.128/26
            * 172.16.78.192/26
            * 10.10.8.4/30
* ### Switches
    * Interfaz con Direccionamiento: VLAN 1
    * Segunda IP
