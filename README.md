# nuclei-template-Lab
# CVE-2025-1025 — Plantilla demo para Nuclei

**Descripción**  
Plantilla **sanitizada** y de demostración (CVE-2025-1025) para uso educativo con Nuclei. Esta plantilla simula un flujo *login → upload → verify* y **no** contiene PoC explotables. Pensada para entornos de prueba o laboratorios.

**Advertencia / Uso responsable**  
Ejecuta esta plantilla **solo** contra sistemas que tengas permiso para evaluar (laboratorio, máquinas propias o programas de bug bounty autorizados). No escanees sistemas ajenos. No publiques evidencia sensible ni URLs reales.

## Contenido del repositorio

## Requisitos (Kali / Ubuntu / WSL)
- Nuclei instalado (v3.x recomendado)
- Plantillas clonadas (si quieres usar otras)
- Conexión a terminal con permisos adecuados

## Cómo ejecutar (ejemplo)
```bash
# instalar nuclei si no lo tienes
curl -sSfL https://raw.githubusercontent.com/projectdiscovery/nuclei/v3/cmd/nuclei/install.sh | bash
sudo mv nuclei /usr/local/bin/

# ejecutar la plantilla contra un objetivo de PRUEBA (reemplaza por tu target autorizado)
echo "https://anon.example" | nuclei -t templates/http/cves/2025/CVE-2025-1025-prueba.yaml -silent
Qué hace la plantilla (resumen)

Simula petición de login y verificación de csrf.

Simula subida de archivo con un marker aleatorio y comprueba que sea accesible luego.

Devuelve coincidencia si el servidor responde con los indicadores definidos en matchers.

Buenas prácticas antes de ejecutar

Revisa el YAML para entender requests, matchers y extractors.

Anonimiza o elimina cualquier host real antes de commitear/subir al repo.

Acompaña la plantilla con un SECURITY.md si vas a mantener el repo público.

Licencia

Este proyecto se publica bajo la MIT License. Consulta el archivo LICENSE para detalles.
