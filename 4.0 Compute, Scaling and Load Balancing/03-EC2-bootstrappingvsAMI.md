# Bootstrapping vs AMI

Creating a default EC2

- Base dependencies and app ( generic and installation  is slow)
- app updates ( generic and not very fast)
- App config (very specific and fast)

## Bootstrapping

- script is created as a part of userdata
- very flexible but takes time

## AMI baking

- time consuming tasks upfront

- all the software is installed

- AMI is created

- not very flexible

Best result will be combination of Bootstrapping + AMI baking