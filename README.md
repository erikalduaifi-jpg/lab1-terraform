# Lab 1 – Terraform

## Vad projektet gör

Projektet använder **Terraform** och **GitHub Actions** för att skapa en Ubuntu-baserad VM i Google Cloud. Terraform används för att automatiskt skapa infrastrukturen, medan GitHub Actions kör olika kontroller när man pushar kod till GitHub.

När pipelinen körs i GitHub Actions kontrolleras Terraform-koden så att den är korrekt skriven, följer rätt struktur och inte innehåller några uppenbara säkerhetsproblem.

Projektet skapar också en **backup policy** så att VM-maskinen säkerhetskopieras dagligen.

När VM:n startar körs även ett **startup-script**. Scriptet gör några enkla säkerhetsåtgärder, till exempel installerar en brandvägg och andra säkerhetsverktyg. Scriptet skapar också en loggfil så att man kan se om något gick fel under installationen.

---

## Hur man kör projektet

För att kunna köra Terraform behöver man ha **Terraform installerat** och ha projektets `.tf`-filer i den mapp där man kör kommandona.

### 1. Kör Terraform-kommandon för att initiera, planera och sedan applicera koden
terraform init
terraform plan
terraform apply

#### Screenshot över terraform pipeline:
<p align="center">
  <img src="images/googlecloudvm1.png" width="600" title="Alt-text">
</p>

##### Screenshot på Google Cloud VM status:
<p align="center">
  <img src="images/googlecloudvm.png" width="600" title="Alt-text">
</p>
