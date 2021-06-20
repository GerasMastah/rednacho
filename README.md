<div align="center"><img src="https://www.brandbucket.com/sites/default/files/logo_uploads/334406/large_devmonks.png"></div>

***
# **Proyecto-GitHub: Configuración de red**

  1. Realizar configuración básica y enrutamiento dinámico OSPF área única.
  2. Aplicar mejoras prácticas de seguridad en las configuraciones.
  3. Al final, debe haber comunicación entre todos los dispositivos.

## Datos generales.
  
  * 1a IP de cada red como Gateway.
  * 2da IP a Switches.
  * 3a IP a PC´s.
  
## Documentación
### Cálculos VLSM

| Subnet Name | Needed Size | Address | Mask | Dec Mask | Assignable Range |
| ------ | ------ | ------ | ------ | ------ | ------ |
| Reservada | 8300 | 172.16.0.0 | /18 | 255.255.192.0 | 172.16.0.1 - 172.16.63.254 |
| Sensores | 2000 | 172.16.64.0 | /21 | 255.255.248.0 | 172.16.64.1 - 172.16.71.254 |
| Producción | 1000 | 172.16.72.0 | /22 | 255.255.252.0 | 172.16.72.1 - 172.16.75.254 |
| Personal | 300 | 172.16.76.0 | /23 | 255.255.254.0 | 172.16.76.1 - 172.16.77.254 |
| Almacen | 100 | 172.16.78.0 | /25 | 255.255.255.128 | 172.16.78.1 - 172.16.78.126 |
| Contabilidad | 60 | 172.16.78.128 | /26 | 255.255.255.192 | 172.16.78.129 - 172.16.78.190 |
| TI | 60 | 172.16.78.192 | /26 | 255.255.255.192 | 172.16.78.193 - 172.16.78.254 |


### Tablas de direccionamiento... 

| Nom_dispositivo | Interfas | Address | Mask |
| ------ | ------ | ------ | ------ |
| R-Mor | Gi 0/0/0 | 172.16.76.1 | 255.255.254.0 |
| R-Mor | Gi 0/0/1 | 172.16.78.1 | 255.255.255.128 | 
| R-Mor | Gi 0/0/2 | 10.10.5.2 | 255.255.255.252 | 
| R-Mor | Se 0/1/1 | 10.10.8.5 | 255.255.255.252 |
| R-Chis | Se 0/1/1 | 10.10.8.6 | 255.255.255.252 |
| R-Chis | Gi 0/0/0 | 172.16.78.129| 255.255.255.192 |
| R-Chis | Gi 0/0/1 | 172.16.78.193 | 255.255.255.192 |
| R-Son | Gi 0/0/0| 172.16.72.1 | 255.255.252.0 |
| R-Son | Gi 0/0/1 | 172.16.64.1 | 255.255.248.0 |
| R-Son | Gi 0/0/2 | 10.10.5.1 | 255.255.255.252 |
| Sw1 | Gi0/1 | NULL | NULL |
| Sw1 | Fa 0/1 | 172.16.64.2 | 255.255.248.0 |
| Sw2 | Gi0/1 | NULL | NULL |
| Sw2 | Fa 0/1 | 172.16.72.2 | 255.255.252.0 |
| SwA | Gi0/1 | NULL | NULL |
| SwA | Fa 0/1 | 172.16.76.2 | 255.255.254.0 |
| SwB | Gi0/1 | NULL | NULL |
| SwB | Fa 0/1 | 172.16.78.2 | 255.255.255.128 |
| Sw10 | Gi0/1 | NULL | NULL |
| Sw10 | Fa 0/1 | 172.16.78.130 | 255.255.255.192 |
| Sw20 | Gi0/1 | NULL | NULL |
| Sw20 | Fa 0/1 | 172.16.78.194 | 255.255.255.192 |
| PC0 | Fa0 | 172.16.64.3 | 255.255.248.0 | 
| Laptop0 | Fa0 | 172.16.72.3 | 255.255.252.0 | 
| Laptop1 | Fa0 | 172.16.76.3 | 255.255.254.0 |
| Server 0 | Fa0 | 172.16.78.3 | 255.255.255.128 | 
| PC1 | Fa0 | 172.16.78.195 | 255.255.255.192 | 
| Laptop 2 | Fa0 | 172.16.78.31 | 255.255.255.192 | 


Por hacer:
* [ ] Documentación
- ✅ VLSM
- * [ ] Tablas de Enrutamiento
* [ ] Configuración
- * [ ] R - Son
   - * [ ] Red Sensores
      - * [ ] Configuración Básica
      - * [ ] Enrutamiento OSPFv2
   - * [ ] Red Producción
      - * [ ] Configuración Básica
      - * [ ] Enrutamiento OSPFv2
- * [ ] R - Mor
   - * [ ] Red Personal
      - * [ ] Configuración Básica
      - * [ ] Enrutamiento OSPFv2 
   - * [ ] Red Almacen 
      - *  [ ] Configuración Básica
      - * [ ] Enrutamiento OSPFv2 
- * [ ] R - Chis 
   - * [ ] Red Contabilidad/Legal
      - *  [ ] Configuración Básica
      - *  [ ] Enrutamiento OSPFv2 
    - * [ ] Red TI
      - * [ ] Configuración Básica
      - *  [ ] Enrutamiento OSPFv2 
