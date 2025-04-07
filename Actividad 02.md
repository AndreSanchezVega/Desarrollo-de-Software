# A. Infraestructura como Código

## 1)Investigar una herramienta de IaC (p. ej. Terraform) y describir cómo organiza sus módulos.
Las herramientas de IaC se encargan tanto del aprovisionamiento de recursos como la gestión de configuraciones.  
En esta ocasión mi grupo eligio la herramienta Ansible . Es una herramienta de la IaC que permite automatizar la
configuración de sistemas, la gestión de aplicaciones y el aprovisionamiento de infraestructura. Su lenguaje de definición es YAML.
<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQhZqdh8uZdUtuh3Dpq5Fi7OPf3K0XCNUtxLw&s" alt="DevOps" width="200">
</p>  

- Los módulos de Ansible son piezas reutilizables de código que realizan tareas específicas . Se pueden
usar directamente en los playbooks, y Ansible los busca en su librería principal, aunque también se pueden crear y organizar módulos personalizados dentro del proyecto, en una carpeta llamada library/.

## 2) Proponer la estructura de archivos y directorios para un proyecto hipotético que incluya tres módulos: network, database y application. Justificar la jerarquía elegida.
plaintext
mi_proyecto_ansible/
├── inventory/
│   └── hosts               # Inventario de servidores
├── playbook.yml            # Playbook principal
├── roles/
│   ├── network/
│   │   └── tasks/
│   │       └── main.yml
│   ├── database/
│   │   └── tasks/
│   │       └── main.yml
│   └── application/
│       └── tasks/
│           └── main.yml

- roles/ : Tanto network , database y application se organizan por roles , esto nos permite reutilizar los componentes por separados en otros proyectos.
- tasks/ : Contiene las tareas principales para cada rol
- mail.yml : Paso que ejecutara Ansible cuando el rol se aplique a un host.

# B. Contenerización y despliegue de aplicaciones modernas

## 1) Describir un flujo simple de despliegue donde un desarrollador hace un cambio en el código, se construye una nueva imagen Docker y se actualiza un Deployment de Kubernetes.
1) Se modifica el código.
2) Se crea una nueva imagen de Docker a partir del DockerFile con el código actualizado.
3) La imagen se sube a un registro.
4) Se actualiza el Deployment en Kubernetes con la nueva imagen.
5) Kubernetes reemplaza los contenedores antiguos con los nuevos sin detener el servicio.

## 2) Explicar las ventajas de usar Kubernetes para escalar una aplicación en un evento de alto tráfico.
- Autoescalado dinámico (HPA y VPA):
  
Ejemplo: Si una tienda en línea tiene un pico de tráfico en Black Friday, HPA puede aumentar el número de réplicas de la aplicación sin intervención manual.
- Balanceo de carga automático:
  
Ejemplo: Un servicio de streaming puede repartir el tráfico entre varios servidores para evitar caídas por sobrecarga.
- Tolerancia a fallos:
  
Ejemplo: Si un servidor en la nube falla, Kubernetes redistribuye las cargas a otros servidores sin interrumpir el servicio.
- Optmizacion del uso de recursos:
  
Ejemplo: Una empresa de SaaS puede optimizar el costo en la nube asegurando que los recursos se usen de manera eficiente.

# C. Observabilidad y Troubleshooting

## 1) Investigar y describir cómo Prometheus y Grafana se integran con Kubernetes para monitorear los contenedores y el cluster.
- Prometheus recolecta métricas automáticamente desde Kubernetes.
- Grafana visualiza las métricas en paneles intuitivos.
- Ambos permiten alertas y monitoreo proactivo del cluster.

## 2) Proponer un set de métricas y alertas mínimas para una aplicación web (por ejemplo, latencia de peticiones, uso de CPU/memoria, tasa de errores).
### Métricas claves
1) Latencia de peticiones: Tiempo de respuesta (ms).
2) Tasa de errores: Porcentaje de errores.
3) Uso de CPU: Porcentaje de utilización de CPU.
4) Uso de memoria (RAM): Porcentaje de memoria usada.
5) Tasa de peticiones: Número de solicitudes por segundo.
6) Uptime: Tiempo de actividad o disponibilidad (%) de la aplicación.
7) Throughput: Operaciones o transacciones completadas por segundo.

### Alertas mínimas:
1) Alta latencia: Latencia > 500ms durante 5 minutos.
2) Errores 4xx: > 5% de errores 4xx en los últimos 5 minutos.
3) Errores 5xx: > 1% de errores 5xx en los últimos 5 minutos.
4) Uso elevado de CPU: > 85% durante 10 minutos.
5) Uso excesivo de RAM: > 80% durante 10 minutos.
6) Caída de la aplicación (Uptime): Si la aplicación está caída por > 5 minutos.
7) Baja disponibilidad de servicios clave: < 99.9% de disponibilidad en 24 horas.
   
# D. CI/CD (Integración continua / Despliegue continuo)

## 1) Explicar la diferencia entre entrega continua (continuous delivery) y despliegue continuo (continuous deployment).
- *CONTINOUS INTEGRATION (CI)*: Es la practica de fusionar cambios en el codigo de forma frecuente, subirlos a un repositorio central y ejecutar pruebas automatizadas
- *CONTINOUS DEPLOYMENT (CD)*: Consiste en automatizar el despliegue y garantizar que cada cambio se someta a una prueba

## 2) Describir la relevancia de implementar pruebas automáticas (unitarias, de integración, de seguridad) dentro del pipeline.
- Pruebas unitarias : Consiste en probar metodos y/o funciones dentro de una clase, modulo o componente.
- Pruebas de integración :Consiste en probar que los modulos y/o servicios que usa tu aplicación funcionen bien en conjunto.
- Pruebas de seguridad : Buscan debilidades de seguridad comunes, como ataques de inyección, configuraciones inseguras y mecanismos de autenticación débiles.