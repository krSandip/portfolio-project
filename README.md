# Personal Portfolio Website

A modern, responsive, and professional **Personal Portfolio Website** developed to showcase academic achievements, technical skills, and completed projects. The site is built with **Spring Boot** and **Thymeleaf** for backend and server-rendered views, and standard front-end technologies (HTML, CSS, JavaScript) for layout and interactivity.  

🌐 **Live Demo:** [Portfolio Website](https://portfolio-project-hqkh.onrender.com)     

---

## ⚙️ System Overview
- **Backend:** Spring Boot handles routing and lifecycle.  
- **Views:** Thymeleaf templates with reusable fragments.  
- **Static Assets:** CSS, JavaScript, and images served from resources.  
- **Deployment:** Deployable on cloud services like Render or Heroku.  

---

## 🛠️ Technology Stack
| Technology   | Description |
|--------------|-------------|
| **HTML5**       | Structuring web content. |
| **CSS3**        | Styling, responsive design, animations. |
| **JavaScript**  | Client-side interactivity, smooth scrolling, dynamic behavior. |
| **Thymeleaf**   | Template engine for server-rendered HTML views. |
| **Spring Boot** | Java-based framework for backend services and routing. |
| **Git**         | Version control for source code management. |
| **GitHub**      | Code hosting platform for version control and collaboration. |
| **Docker**      | Containerization tool used to package and deploy the application. |
| **Render**      | Cloud deployment platform for hosting Spring Boot applications. |

---

## 📂 Project Structure

```
src/main/java/com/sandip/portfolioproject -> Java controllers and app files
src/main/resources/templates -> Thymeleaf templates (home, fragments, etc.)
src/main/resources/static -> CSS, JS, images
PortfolioprojectApplication.java -> Entry point
HomeController.java -> Routing logic
templates/home.html -> Main UI template
```

---

## 🔨 Implementation Details
- **Reusable Thymeleaf fragments** for modular updates.  
- **Spring Boot controllers** to manage routes.  
- **Lightweight deployment-ready JAR/Docker** build.  

---

## 🚀 Testing & Deployment
### Run locally:
```bash
mvn clean package
mvn spring-boot:run
```
### Docker Deployment:
```bash
FROM maven:3.8.4-openjdk-17 AS build
WORKDIR /app
COPY pom.xml .
RUN mvn dependency:go-offline
COPY src ./src
RUN mvn clean package -DskipTests
FROM openjdk:17-jdk-slim
WORKDIR /app
COPY --from=build /app/target/portfolioproject-0.0.1-SNAPSHOT.jar .
EXPOSE 9090
ENTRYPOINT ["java", "-jar", "/app/portfolioproject-0.0.1-SNAPSHOT.jar"]
```

---

## 🔮 Future Enhancements

*  Admin dashboard for dynamic content updates.
*  Blog/articles section with markdown support.
*  SEO improvements & analytics integration.
*  CI/CD pipeline and automated testing.

---

## 📚 References

1. [Spring Boot Documentation](https://spring.io/projects/spring-boot)  
2. [Thymeleaf Documentation](https://www.thymeleaf.org/)  
3. [MDN Web Docs](https://developer.mozilla.org/)  

---

## 👨‍💻 Author
**Sandeep Kumar**  
- 🎓 B.E in Electronics & Communication Engineering  
- 📧 Email: [sink10704@gmail.com](mailto:sink10704@gmail.com)  
- 📱 Mobile: +91 7007935226  
- 🔗 LinkedIn: [linkedin.com/in/sandeep-kumar-842ab1256](https://www.linkedin.com/in/sandeep-kumar-842ab1256)  
- 💻 GitHub: [github.com/krSandip](https://github.com/krSandip)  
