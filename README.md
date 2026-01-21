# AEM Cloud Service Project - MyProject

Full-featured Adobe Experience Manager as a Cloud Service project.

## Modules

* **core**: Java bundle containing OSGi services, Sling Models, and business logic
* **ui.apps**: Contains components, templates, and client libraries
* **ui.content**: Contains content structures including Content Fragment Models
* **ui.config**: Contains OSGi configurations
* **all**: Assembly package for deployment to AEM Cloud Service

## Content Fragment Models

### Article
Location: `/conf/myproject/settings/dam/cfm/models/article`

**Fields:**
- **Title** (text, required, max 255 characters)
- **Description** (multiline text)
- **Publish Date** (date)

## Build

Build the entire project:
```bash
mvn clean install
```

Build and install to local AEM instance:
```bash
mvn clean install -PautoInstallPackage
```

## Deploy to AEM Cloud Service

Deploy the `all` package through Cloud Manager pipeline or upload to Package Manager.

## Requirements

* Java 11
* Maven 3.6+
* AEM as a Cloud Service SDK

## Structure

```
/conf/myproject/             - Project configuration container
/apps/myproject/             - Application code
/content/myproject/          - Content root
```