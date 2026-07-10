# CSolutions.Platform

![Target](https://img.shields.io/badge/.NET-Framework%20%2F%20Core-blue)
![Platform](https://img.shields.io/badge/nopCommerce-Plugin%20Extension-brightgreen)

**CSolutions.Platform** es una suite de librerías y abstracciones en .NET diseñada específicamente para extender la funcionalidad base de **nopCommerce** mediante la creación y gestión eficiente de plugins.

Este repositorio provee el núcleo de utilidades, inyección de dependencias compartidas y lógica de persistencia que homogeneiza la arquitectura de todos los módulos adicionales implementados en el ecosistema de comercio electrónico.

---

## 🚀 Características Principales

- **Arquitectura Modular Desacoplada:** Provee clases base e interfaces comunes para evitar la duplicación de lógica redundante en el desarrollo de nuevos plugins de nopCommerce.
- **Inyección de Dependencias Simplificada:** Registros genéricos y auto-descubrimiento de servicios adaptados al ciclo de vida del contenedor nativo de nopCommerce.
- **Data & Migration Helpers:** Capas de abstracción preparadas para mapear entidades personalizadas, builders de FluentMigrator y contextos de datos aislados sin alterar el core del CMS.
- **Utilidades del Ecosistema:** Métodos de extensión listos para interactuar de forma ágil con las configuraciones del sitio (`ISettingService`), tiendas múltiples, layouts de vistas compartidas y contextos de clientes.

---

## 📁 Estructura del Repositorio

Una vez inicializado el código base, se sugiere mantener la siguiente jerarquía de proyectos:

```text
CSolutions.Platform/
├── src/
│   ├── CSolutions.Core/				# Interfaces globales, extensiones y lógica agnóstica
│   ├── CSolutions.Infrastructure/		# Mapeos de entidades, configuración DB y Fluent Migrations
│   └── CSolutions.Services/			# Implementación de servicios compartidos multiplug-in
│	└── CSolutions.PluginBase			# Clase base para implementacion de plugins
├── tests/                              # Suite de pruebas unitarias y de integración
├── .gitignore
└── README.md