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

En redes hay un apartado que se llama habilitar el acceso publico (a internet). Dejar todo como esta

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/8d3d14ed-20ec-4066-9401-f997daf94325" />

En etiquetas podemos elegir la etiquetas que necesitemos, pero daremos siguiente

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/911de907-9441-42a4-9886-44498b5e5c28" />

Revisamos que este todo correcto y le damos a crear. Despues ya estaria creado

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/ea208bf1-059c-4e6e-a016-3311a3e429b7" />

# Creacion de Key Vault Secreto

Nos dirigimos al recurso y en la Key Vault vamos al apartado objetos y ahi vemos todas las opciones que tenemos, le damos a secretos y generar

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/e539a72d-3282-49e9-b695-5a6f35c3c82e" />

Lo dejamos en manual, despues pondremos un nombre al secreto, yo le he puesto Contraseña1, luego un secreto, el mio es SoyLaContraseña. Depues dejamos todo igual y crear, ya que es para establecer una fecha de activacion y expiracion

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/c1fa089d-4cb8-48a3-b6af-676f3f654ceb" />

Para mostrar el secreto desde la interfaz del Portal de Azure tenemos que darle sobre el secreto y la version en el recurso. Por ultimo, le damos a mostrar valor secreto y nos saldra la que os comente antes

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/00ed62f4-ccef-408f-8a43-21617be6faca" />
<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/c2fb1113-d809-415f-b440-b009cc3db8ba" />

Para mostrar ver la configuracion de la key y el secreto desde Cloud Shell tenemos que poner los siguientes comandos que se muestran en la captura

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/1233c931-2e90-4756-a5bb-ee7368f5a233" />

# Creacion de Key Vault Claves de Cifrado

La clave es para cifrar y descifrar datos como firmar digitalmente documentos o tambien cifrar discos de maquinas virtuales. En este caso sera para cifrar documentos

Vamos a clave y le damos a generar y version

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/41472b0b-505c-451d-8a4a-80efa223a9a7" />

Le damos a clave por RSA, cifrar y a crear. Con esto ya tenemos una clave que podemos usar para cifrar un documento y estara guardada en Azure

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/2d3969fc-53f9-4d5c-9fde-54b93a7434be" />

# Creacion de Key Vault Certificados SSL

Un certificado digital es para cifrar comunicaciones, identifica un servidor o aplicacion o garantiza que algo es automatico.

En la practica en Azure se pueden usar para activar el protocolo HTTPS de una pagina web, una API que necesita autentificarse con otra o firmar aplicaciones

Ahora os explico como se crea. Le damos a certificados y la version en el recurso de la key

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/3003ba6b-0270-4b32-a2f4-d906f5039c31" />

Ahora en el menu del certificado nos pedira un nombre para el y un nombre comun (CN=), que es el nombre del servidor al que pertenece el certificado

<img width="1920" height="1040" alt="image" src="https://github.com/user-attachments/assets/2f8eba9d-62ed-4362-bc7b-bcd9409dc2ba" />

# Conclusion

Esta practica de uso de Key Vault es un resumen de que se puede hacer con ella, pero sobre todo, como hay que llevarlo a cabo para crearlo
