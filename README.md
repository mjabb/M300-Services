# M300-Services

# Plattformübergreifende Dienste in ein Netzwerk integrieren

![mmdblayout](images/mmdblayout.png)

#### Übersicht des Projekts

Eine Datenbank kann über ein Web-Frontend angesprochen werden mittels Admirer

#### Voraussetzungen

* MySQL Datenbankserver 
* Apache2 Webserver
* Clientmaschine zum ansprechen

### Inhaltsverzeichnis

* **10 Umgebung**
* **20 Codebeschreib**
* **30 Fazit**

### 10 Umgebung

Vagrant 2.2.19 und VirtualBox 6.1 Umgebung mit Hostonly- und NAT-Netzwerkschnittstellen auf einem Windows Host:

- **Webserver: web-srv-01**
  - **_Ubuntu Xenial64_**
  - **_Memory 1024MB_**
  - **_Apache2 webserver_**
  - **_IP & Port 192.168.2.100:80_**
  - **_NAT 8080 (für den Client Zugriff)_**

- **Datenbankserver: db-srv-01**
  - **_Ubuntu Xenial64_**
  - **_Memory 1024MB_**
  - **_MySQL DB_**
  - **_IP & Port 192.168.2.99:3306_**

### 20 Codebeschreib
- Webserver aufbauen:
  - Folgende Prerequisites mussen installiert werden: 

<tab>    | <tab>
--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------
**debconf-utilsapache2**   | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**nmap**        | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**php**        | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**libapache2-mod-php** | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**php-curl** | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**php-cli** | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**php-mysql** | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**php-gd** | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
**mysql-client** | Konfigurieren und betreiben von PCs. Servern und Peripherie (Multiusersysteme) Erfahrung im Aufbau von lokalen Netzwerken
  
  - Als MySQL Client muss noch adminer installiert werden.
  - Fixer DNS Eintrag für den DB Server im Hosts ergänzen.

- Datenbank Server aufbauen:
  - Das db.sh Script wird ausgeführt
