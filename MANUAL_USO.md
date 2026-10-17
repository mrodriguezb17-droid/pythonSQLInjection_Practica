
# Manual de uso
## Simulación y mitigación de SQL Injection

### 1. Requisitos
- Python instalado.
- PyCharm.
- Flask instalado en el entorno virtual.
- Los archivos de la práctica y la base de datos SQLite.

### 2. Ejecutar la aplicación vulnerable
1. Abrir el proyecto en PyCharm.
2. Ejecutar el archivo `app_vulnerable.py`.
3. Abrir el navegador y entrar a http://127.0.0.1:5000.
4. Probar el formulario de autenticación y la búsqueda de usuarios.

### 3. Ejecutar la aplicación segura
1. Abrir una segunda configuración de ejecución en PyCharm.
2. Ejecutar `app_segura.py`.
3. Abrir http://127.0.0.1:5001.
4. Comprobar el comportamiento del inicio de sesión y la búsqueda.

### 4. Ejecutar las pruebas SQL Injection
1. Mantener las dos aplicaciones en funcionamiento.
2. Ejecutar el archivo `ataque_sql_i.py`.
3. Revisar los resultados de autenticación y búsqueda en la consola.
4. Comparar las respuestas de la aplicación vulnerable y la segura.

### 5. Escanear los puertos
1. Ejecutar `escaneo_red.py`.
2. Revisar los puertos abiertos y cerrados.
3. Identificar los puertos 5000 y 5001 cuando las aplicaciones estén activas.

### 6. Revisar la base de datos
1. Ejecutar `endurecimiento_db.py`.
2. Comprobar que la copia de seguridad se haya creado.
3. Verificar que la comprobación de integridad muestre `ok`.

### 7. Resultados esperados
- La aplicación vulnerable puede permitir la alteración de consultas SQL.
- La aplicación segura debe rechazar los intentos probados mediante consultas parametrizadas.
- El escáner debe identificar los puertos que aceptan conexiones.
- El módulo de SQLite debe crear la copia de seguridad y comprobar la integridad.

### 8. Recomendaciones de seguridad
- Ejecutar las pruebas únicamente en el entorno local autorizado.
- No publicar la aplicación vulnerable en Internet.
- Utilizar consultas parametrizadas.
- Proteger las contraseñas mediante funciones de hash.
- Mantener copias de seguridad y restringir el acceso a los archivos.
