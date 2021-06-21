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
- * ✅ R - Mor
   - * ✅ Red Personal
      - * ✅ Configuración Básica
      - * ✅ Enrutamiento OSPFv2 
   - * ✅ Red Almacen 
      - * ✅ Configuración Básica
      - * ✅ Enrutamiento OSPFv2 
- * [ ] R - Chis 
   - * [ ] Red Contabilidad/Legal
      - *  [ ] Configuración Básica
      - *  [ ] Enrutamiento OSPFv2 
    - * [ ] Red TI
      - * [ ] Configuración Básica
      - *  [ ] Enrutamiento OSPFv2 
