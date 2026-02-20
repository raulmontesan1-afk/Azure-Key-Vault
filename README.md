# Azure-Key-Vault
En este repositorio explico que es y como se crea una Key Vault en Azure y que se puede hacer con ella

Una key Vault es un servicio que ofrece Azure para almacenar de forma segura contraseñas, claves de cifrados, certificados y secretos

# Creacion de Key Vault

Desde el portal de Azure buscamos Key Vaults (en español almacenes de claves) y le damos a crear

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/3b65ac15-29bb-4f02-bf20-4a281f81ef13" />
<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/f2b3a822-9070-4f46-8783-bbbe7bb4ba12" />

Indicamos la suscripcion y el grupo de recurso que lo llamare por mi apellido y key. Despues llamare a la key primera-key y todo lo demas por defecto y siguiente

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/f38895db-098b-4174-b4ab-8d001bb73615" />

En configuracion de acceso, en modelo de permisos podemos elegir entre control de acceso basado en roles y por directivas, yo elijo directivas, pero en ambiente corporativo habria que elegir basado en roles

En acceso a los recursos no marcaremos nada, ya que esto es una practica. De todas maneras, os explico que significa cada opcion:

La primera opcion de Azure Virtual Machines permite que la Key Vault pueda usarse al desplegarse

La segunda opcion de Azure Resource Manager permite que cuando crees recursos con plantillas (ARM), puedan acceder a secretos del Key Vault

Y la tercera opcion de Azure Disk Encryption permite usar claves del Key Vault para cifrar discos de máquinas virtuales

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/2319ec00-031c-404c-9ad4-21a9f3a484f5" />

En redes hay un aparatado que se llama habilitar el acceso publico (a internet). Dejar todo como esta

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/8d3d14ed-20ec-4066-9401-f997daf94325" />

En etiquetas podemos elegir la etiquetas que necesitemos, pero daremos siguiente

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/911de907-9441-42a4-9886-44498b5e5c28" />

Revisamos que este todo correcto y le damos a crear

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/ea208bf1-059c-4e6e-a016-3311a3e429b7" />
