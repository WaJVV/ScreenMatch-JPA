
# 🎬 ScreenMatch

**ScreenMatch** es una aplicación desarrollada con Java y Spring Boot que permite consumir información sobre series de televisión desde una API externa, almacenar los datos localmente mediante JPA y realizar consultas inteligentes, incluyendo el uso de IA con ChatGPT para análisis de descripciones.

---

## 📌 Tabla de Contenidos

- [Características](#características)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Instalación](#instalación)
- [Uso](#uso)
- [Capturas de Pantalla](#capturas-de-pantalla)
- [Autor](#autor)
- [Licencia](#licencia)

---

## ✨ Características

- Consumo de una API externa para obtener información de series y episodios.
- Almacenamiento de series, temporadas y episodios en base de datos con JPA.
- Conversión de datos JSON a objetos Java utilizando una interfaz personalizada.
- Consultas avanzadas a través de `Spring Data JPA`.
- Integración con OpenAI (ChatGPT) para análisis o categorización de contenido.
- Proyecto estructurado y escalable con buenas prácticas.

---

## 🧰 Tecnologías Utilizadas

- Java 17+
- Spring Boot
- Spring Data JPA
- Maven
- API de series (OMDb u otra similar)
- OpenAI API (ChatGPT)
- H2 / MySQL / PostgreSQL (según configuración)
- Lombok (opcional)
- IntelliJ IDEA / Eclipse

---

## 📁 Estructura del Proyecto

```
src/
├── main/
│   ├── java/
│   │   └── com.aluracursos.screenmatch/
│   │       ├── model/             # Entidades: Serie, Episodio, etc.
│   │       ├── repository/        # Interfaces de acceso a datos (JPA)
│   │       ├── service/           # Lógica de negocio y consumo de API
│   │       ├── principal/         # Clase de prueba o ejecución manual
│   │       └── ScreenmatchApplication.java  # Clase principal Spring Boot
│   └── resources/
│       └── application.properties # Configuración del proyecto
└── test/
    └── ...                        # Pruebas automatizadas
```

---

## ⚙️ Instalación

1. Clona el repositorio:
   ```bash
   git clone https://github.com/tu-usuario/screenmatch.git
   cd screenmatch
   ```

2. Configura el archivo `application.properties` para tu base de datos y API Key si es necesario:
   ```properties
   spring.datasource.url=jdbc:h2:mem:testdb
   spring.datasource.driverClassName=org.h2.Driver
   spring.datasource.username=sa
   spring.datasource.password=
   spring.jpa.hibernate.ddl-auto=update

   # API externa y clave de ChatGPT (si aplica)
   api.chatgpt.key=tu_api_key
   ```

3. Ejecuta el proyecto:
   ```bash
   ./mvnw spring-boot:run
   ```

> También puedes ejecutar la clase `Principal.java` para pruebas específicas si no deseas iniciar el servidor completo.

---

## ▶️ Uso

- El sistema consume series desde una API externa mediante el servicio `ConsumoAPI`.
- Convierte los datos usando `ConvierteDatos` e interfaces `IConvierteDatos`.
- Almacena los datos utilizando `Spring Data JPA` y permite realizar búsquedas.
- Consulta descripciones mediante `ConsultaChatGPT` para obtener análisis adicionales.

---


## 👨‍💻 Autor

Proyecto realizado como parte del curso de Alura:  
**Desarrollador:** Wayner Jimenez Vega  
📧 Contacto: Waynerjive@gmail.com

---

## 📄 Licencia

Este proyecto está licenciado bajo los términos de la [MIT License](LICENSE).

---
