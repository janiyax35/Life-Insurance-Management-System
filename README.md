<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:005f40,100:00bf80&height=200&section=header&text=Life%20Insurance%20Management%20System&fontSize=40&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Comprehensive%20Insurance%20Policy%20Management%20Solution&descAlignY=60&descAlign=50" width="100%">
</div>

<p align="center">
  <a href="https://www.java.com"><img src="https://img.shields.io/badge/Java-17-orange.svg?style=for-the-badge&logo=java&logoColor=white" alt="Java 17"></a>
  <a href="https://spring.io/projects/spring-boot"><img src="https://img.shields.io/badge/Spring%20Boot-3.5.4-brightgreen.svg?style=for-the-badge&logo=spring-boot" alt="Spring Boot"></a>
  <a href="https://www.mysql.com"><img src="https://img.shields.io/badge/MySQL-8.0-blue.svg?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL"></a>
  <a href="https://www.thymeleaf.org"><img src="https://img.shields.io/badge/Thymeleaf-Latest-green.svg?style=for-the-badge&logo=thymeleaf&logoColor=white" alt="Thymeleaf"></a>
</p>

<div align="center">
  <h3>
    <a href="#overview">Overview</a> •
    <a href="#key-features">Features</a> •
    <a href="#system-architecture">Architecture</a> •
    <a href="#installation">Installation</a> •
    <a href="#usage">Usage</a> •
    <a href="#tech-stack">Tech Stack</a> •
    <a href="#contributor">Contributor</a> •
    <a href="#license">License</a>
  </h3>
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&duration=2000&pause=1000&color=00EEFF&center=true&vCenter=true&random=false&width=600&lines=Role-Based+Access+Control;Policy+Management;Claims+Processing;Risk+Assessment;Payment+Handling;Customer+Service" alt="Project Features"/>
</div>

<hr>

## Overview

Life Insurance Management System is a comprehensive web-based platform designed to streamline insurance policy management, claims processing, and customer service operations. It provides a unified solution for insurance companies to manage their entire workflow from policy creation through claims settlement and customer support.

The system features dedicated modules for various stakeholders:
- 👤 **Customers**: View and manage policies, submit claims
- 👨‍💼 **Customer Service Executives (CSE)**: Handle customer inquiries and policy updates
- 🔍 **Senior Insurance Advisors (SIA)**: Assess risks and review claims
- 💰 **Finance Officers (FO)**: Process payments and manage financial transactions
- 👨‍💼 **HR/Admin Managers**: System administration and staff management
- 👨‍💻 **IT System Analysts (ISA)**: Technical system maintenance

## Key Features

<table>
  <tr>
    <td width="50%">
      <h3>📋 Policy Management</h3>
      <ul>
        <li>Create and manage insurance policies</li>
        <li>Policy renewal and modification</li>
        <li>Premium calculation and updates</li>
        <li>Beneficiary management</li>
      </ul>
    </td>
    <td width="50%">
      <h3>⚖️ Claims Processing</h3>
      <ul>
        <li>Claims submission and tracking</li>
        <li>Multi-stage approval workflow</li>
        <li>Document management</li>
        <li>Payout processing</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3>💵 Payment Management</h3>
      <ul>
        <li>Premium collection</li>
        <li>Payment scheduling</li>
        <li>Transaction tracking</li>
        <li>Financial reporting</li>
      </ul>
    </td>
    <td width="50%">
      <h3>🔍 Risk Assessment</h3>
      <ul>
        <li>Policy risk evaluation</li>
        <li>Risk score calculation</li>
        <li>Assessment recommendations</li>
        <li>Coverage determination</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td width="50%">
      <h3>👥 User Management</h3>
      <ul>
        <li>Role-based access control</li>
        <li>User authentication</li>
        <li>Activity logging</li>
        <li>Profile management</li>
      </ul>
    </td>
    <td width="50%">
      <h3>📊 Reporting System</h3>
      <ul>
        <li>Policy performance analytics</li>
        <li>Claims statistics</li>
        <li>Financial reports</li>
        <li>Audit trails</li>
      </ul>
    </td>
  </tr>
</table>

## System Architecture

The Life Insurance Management System follows a modern, layered architecture:

```
┌─────────────────────────────────────────────────┐
│                  Web Interface                  │
│             (Thymeleaf + HTML/CSS)             │
└───────────────────────┬─────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────┐
│              Spring MVC Controllers             │
└───────────────────────┬─────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────┐
│                Service Layer                    │
│       (Business Logic & Process Workflows)      │
└───────────────────────┬─────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────┐
│           Spring Data JPA Repositories          │
└───────────────────────┬─────────────────────────┘
                        │
┌───────────────────────▼─────────────────────────┐
│                  MySQL Database                 │
│    (Policies, Claims, Users, Payments)          │
└─────────────────────────────────────────────────┘
```

## Installation

### Prerequisites

- Java JDK 17 or higher
- Maven 3.6+
- MySQL 8.0+
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/janiyax35/Life-Insurance-Management-System
   cd Life-Insurance-Management-System
   ```

2. **Configure MySQL database**
   ```bash
   mysql -u root -p
   ```
   ```sql
   CREATE DATABASE v1_16_thuli_life_insurance;
   exit;
   ```

3. **Run the database schema script**
   ```bash
   mysql -u root -p v1_16_thuli_life_insurance < "Correct Working SQL code.sql"
   ```

4. **Update database configuration**
   
   Edit `src/main/resources/application.properties` with your MySQL credentials:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/v1_16_thuli_life_insurance
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   ```

5. **Build the project**
   ```bash
   mvn clean install
   ```

6. **Run the application**
   ```bash
   mvn spring-boot:run
   ```

7. **Access the application**
   
   Open your browser and navigate to: `http://localhost:8080`

## Usage

### Login Credentials

The system comes pre-configured with the following sample users:

| Username  | Password | Role                        |
|-----------|----------|----------------------------|
| customer1 | pass123  | Customer                   |
| cse1      | cse123   | Customer Service Executive |
| sia1      | sia123   | Senior Insurance Advisor   |
| fo1       | fo123    | Finance Officer            |
| admin1    | admin123 | HR/Admin Manager           |
| isa1      | isa123   | IT System Analyst         |

### Workflow Example

1. **Customer** applies for a new insurance policy
2. **CSE** reviews application and forwards to SIA
3. **SIA** performs risk assessment and approves policy
4. **FO** calculates and sets up premium payments
5. **Customer** makes premium payments
6. **CSE** handles policy updates and inquiries
7. **SIA** processes any claims
8. **FO** manages claim payouts

## Tech Stack

- **Backend**: Java 17, Spring Boot 3.5.4, Spring Data JPA
- **Frontend**: Thymeleaf, HTML5, CSS3, JavaScript
- **Database**: MySQL 8.0
- **Build Tool**: Maven
- **Version Control**: Git

## Contributor

<div align="center">
  <a href="https://github.com/janiyax35">
    <img src="https://avatars.githubusercontent.com/u/138566861?v=4" width="100px" style="border-radius:50%;" alt="Janith Deshan"/>
    <br />
    <b>Janith Deshan Mihijaya Samaratunga</b>
    <br />
    BSc (Hons) Information Technology Specialized in Cyber Security
    <br />
    <sub>Sri Lanka Institute of Information Technology (SLIIT)</sub>
    <br />
    <a href="https://github.com/janiyax35">
      <img src="https://img.shields.io/badge/GitHub-janiyax35-00eeff?style=flat-square&logo=github&logoColor=white&labelColor=black" alt="GitHub"/>
    </a>
  </a>
</div>

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:005f40,100:00bf80&height=120&section=footer&text=Secure%20Your%20Future&fontSize=20&fontColor=ffffff&animation=fadeIn&fontAlignY=70" width="100%">
</div>
