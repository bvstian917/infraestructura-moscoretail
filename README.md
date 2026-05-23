# 🚀 Infraestructura Cloud - MoscoRetail (AWS CLI)

Este repositorio contiene el script de comandos en AWS CLI equivalentes para automatizar la creación de la infraestructura requerida en la Evaluación Parcial Nº3.

## 1. Creación de la VPC y Subredes
```bash
# Crear la VPC principal
aws ec2 create-vpc --cidr-block 10.0.0.0/16 --tag-specifications 'ResourceType=vpc,Tags=[{Key=Name,Value=VPC-MoscoRetail}]'

# Crear Subred Pública Zona A
aws ec2 create-subnet --vpc-id vpc-xxxxxx --cidr-block 10.0.1.0/24 --availability-zone us-east-1a

# Crear Subred Privada Zona A (Para Servidor Linux)
aws ec2 create-subnet --vpc-id vpc-xxxxxx --cidr-block 10.0.2.0/24 --availability-zone us-east-1a

# Crear Subred Pública Zona B
aws ec2 create-subnet --vpc-id vpc-xxxxxx --cidr-block 10.0.3.0/24 --availability-zone us-east-1b

# Crear Subred Privada Zona B (Para Servidor Windows)
aws ec2 create-subnet --vpc-id vpc-xxxxxx --cidr-block 10.0.4.0/24 --availability-zone us-east-1b
