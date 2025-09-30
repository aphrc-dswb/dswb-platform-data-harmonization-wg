# Installation and Configuration Guide: WSL, Docker, OHDSI Broadsea, PgAdmin Container, and ATLAS WebAPI

[![WSL2](https://img.shields.io/badge/WSL2-Required-red)](https://learn.microsoft.com/en-us/windows/wsl/install)
[![Docker](https://img.shields.io/badge/Docker-20.10%2B-2496ED)](https://www.docker.com/)
[![OHDSI Broadsea](https://img.shields.io/badge/OHDSI_Broadsea-Required-red)](https://github.com/OHDSI/Broadsea)
[![PostgreSQL Container](https://img.shields.io/badge/PostgreSQL_Container-15%2B-336791)](https://www.pgadmin.org/docs/pgadmin4/latest/container_deployment.html)
[![ATLAS WebAPI](https://img.shields.io/badge/ATLAS_WebAPI-Required-red)](https://github.com/OHDSI/Atlas)

---

## Overview

This guide provides a step-by-step process for installing and configuring WSL, Docker, OHDSI Broadsea, and PgAdmin in a Dockerized environment. It is designed to help users deploy, manage, and troubleshoot these components efficiently. 

By following this guide, you will:

- Install WSL and configure it for your Windows system
- Install Docker and configure it for your system
- Deploy OHDSI Broadsea for running ATLAS and WebAPI
- Set up PgAdmin within Docker, Connect to ATLAS database and Perform database migrations and backups
- WebAPI configuration 

Whether you're a beginner or an advanced user, this guide will provide the necessary steps to get started and optimize your setup.

---

## Requirements

A laptop/desktop with the following specifications is recommended:

- **Processor:** Intel Core i5 or higher (higher core count is beneficial for parallel processing)
- **RAM:** 16GB (recommended for most OHDSI workloads) if you anticipate running multiple containers or handling large datasets, consider upgrading to 32GB.
- **Storage:** Minimum 500GB, but more is better with Solid-State Drive SSD
- **Operating System:** Windows 10 version 2004 and higher (Build 19041 and higher) or Windows 11

---
