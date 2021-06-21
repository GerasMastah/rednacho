# **Resumen General de Configuración**
***
## General
* ### Router
    * Nombre de Host: R-Mor
    * Nombre de Dominio: r-mor.com
    * Timestamps: Habilitado
    * Reloj Configurado
    * Banners Personalizados
* ### Switches
    * Nombre de Hosts: Sw-A/Sw-B
    * Nombre de Dominio: r-mor.com
    * Timestamps: Habilitado
    * Reloj Configurado
    * Banners Personalizados
## Seguridad
* ### Acceso
    * Usuario SSH: moradmin
    * Contraseñas
    	* SSH: m0r4dm1n!
    	* Consola: r-m0rc0n!
        * Exec: r-m0r3x3c!
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
        * Sticky Address
        * Direcciones MAC Máximas: 2/1
        * Violación: Protect/Restrict
## Enrutamiento
* ### Router
    * Primer IP en Redes Internas
    * Enrutamiento IPv4
    * **OSPF**
        * Versión: 2
        * ID de Proceso: 100
        * ID de Router: 172.16.76.1 (Default)
        * Tipo de Área: Única (0)
        * Interfaces Pasivas: Gigabit Ethernet 0/0/0 - 0/0/1
        * **Redes Anunciadas**
            * 172.16.76.0/22 (Resumidas)
            * 10.10.5.0/30
            * 10.10.8.4/30
* ### Switches
    * Interfaz con Direccionamiento: VLAN 1
    * Segunda IP
