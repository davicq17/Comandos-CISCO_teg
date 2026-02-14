# Comandos-CISCO_teg
comandos de cisco en el ciclo tecnológico de ingeniería telemática  
## Comandos de OSPF
- Hablitar OSPF en un router, el process-id {1 , 65.535}
```
R(config)#router ospf (process-id)
```
- Configurar explicitamente el router ID (dirección IPv4)
  ```
  R(config-router)#router-id (rid)
  ```
- Verificar informacion de los protocolos del router
    ```
    R# show ip protocols
    ```
- Restablecer el porceso ospf en el router
  ```
  R# clear ip ospf process
  ```
## OSPF punto a punto 
- Especificar interfaces que pertecen a una red punto a punto
  ```
  R(config-router)# network (network-address) (wildcard-mask) area (area-id)
  ```
  - EJEMPLO:
    ```
     R(config-router)#network 10.10.1.1 0.0.0.0 area 0
    ```
- Configurar directamente la interfaz del router
  ```
  R(config-if) ip ospf (process-id) area (area-id)
  ```
  - EJEMPLO
    ```
    R(config-router) interface g0/0/0
    R(config-if)ip ospf 10 area 0
    ```
- Configurar interfaz pasiva:
  ```
  R(config)#router ospf 10
  R(config-router)# passive-interface lo0
  ```
