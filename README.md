
# Simulación y Mitigación de SQL Injection

## 1. Descripción del proyecto

Este proyecto académico demuestra una vulnerabilidad de inyección SQL y una forma de prevenirla mediante consultas parametrizadas. Se desarrolló utilizando Python, Flask y SQLite.

El proyecto también incluye un escáner básico de puertos TCP y un módulo para realizar una copia de seguridad y comprobar la integridad de la base de datos.

## 2. Objetivos

- Simular una vulnerabilidad de SQL Injection en un entorno local.
- Comparar una aplicación vulnerable con una aplicación segura.
- Identificar puertos abiertos y cerrados en el equipo local.
- Realizar una copia de seguridad y verificar la integridad de SQLite.

## 3. Tecnologías utilizadas

- Python
- Flask
- SQLite
- PyCharm
- Biblioteca socket
- Biblioteca urllib

## 4. Archivos del proyecto

- `app_vulnerable.py`: aplicación de demostración vulnerable.
- `app_segura.py`: aplicación que utiliza consultas parametrizadas.
- `ataque_sql_i.py`: script de pruebas de SQL Injection.
- `escaneo_red.py`: escáner básico de puertos TCP.
- `endurecimiento_db.py`: copia de seguridad y comprobación de SQLite.
- `MANUAL_USO.md`: instrucciones de uso.
- `usuarios.db`: base de datos del laboratorio.

## 5. Instalación

1. Instalar Python.
2. Abrir el proyecto en PyCharm.
3. Activar el entorno virtual del proyecto.
4. Instalar Flask desde la terminal:

   `python -m pip install flask`

## 6. Ejecución

Ejecutar los siguientes archivos desde PyCharm:

1. `app_vulnerable.py`
2. `app_segura.py`
3. `ataque_sql_i.py`
4. `escaneo_red.py`
5. `endurecimiento_db.py`

Las aplicaciones web utilizan las direcciones locales:

- Aplicación vulnerable: http://127.0.0.1:5000
- Aplicación segura: http://127.0.0.1:5001

Las dos aplicaciones deben estar ejecutándose antes de iniciar las pruebas de `ataque_sql_i.py`.

## 7. Resultados

En las pruebas realizadas, la aplicación vulnerable permitió el acceso mediante una entrada manipulada y devolvió varios registros durante la búsqueda. La aplicación segura rechazó el intento de autenticación y no devolvió registros en la búsqueda manipulada.

El escáner revisó seis puertos locales e identificó abiertos los puertos 5000 y 5001. El módulo de SQLite creó una copia de seguridad y obtuvo `ok` en la comprobación de integridad.

## 8. Seguridad

Este proyecto tiene fines educativos y debe ejecutarse únicamente en un entorno local autorizado. No se debe publicar la aplicación vulnerable en Internet.

Las consultas parametrizadas son una medida importante para prevenir la inyección SQL. También se recomienda proteger las contraseñas mediante funciones de hash y restringir el acceso a los archivos de la base de datos.

## 9. Autora

Grupo: [Escribe tu nombre completo]

Carrera: Tecnologías de la Información y Comunicación TICS

Asignatura: Seguridad Informática

Profesor: Alex Armando Avila

