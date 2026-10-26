# Apolonia — versiones

Este repositorio público contiene las versiones publicadas de **Apolonia**, un sistema de escritorio para consultorios odontológicos de Argentina. Acá solo se publican los instaladores y la información de cada versión; el código fuente es privado.

> **Estado:** el sistema está en desarrollo y todavía no hay versiones publicadas.

## Qué se publica

| Qué | Dónde |
|---|---|
| Instalador de Windows de cada versión | En la sección **Releases**, como archivo adjunto |
| Suma de verificación (SHA-256) del instalador | En la misma versión, junto al instalador |
| `latest.json` | En la raíz de la rama `main`: la última versión del canal estable |
| `latest-beta.json` | En la raíz de la rama `main`: la última versión del canal beta |
| `latest.json.sig` y `latest-beta.json.sig` | La firma de cada archivo anterior |

`latest.json` y `latest-beta.json` indican la última versión disponible, la versión mínima compatible y las notas del cambio. Están **firmados**: el sistema solo acepta información que tenga una firma válida, así que un archivo alterado se rechaza.

## Versiones y canales

Las versiones siguen el [versionado semántico](https://semver.org/lang/es/) y se identifican con una etiqueta `vX.Y.Z`.

- **Estable** (`v1.2.3`): para los consultorios en uso.
- **Beta** (`v1.2.3-beta.1`): versiones previas para probar. Se marcan como versión previa en **Releases**.

## Requisitos

- Windows 10 u 11 de 64 bits.
- Una licencia válida: sin ella el sistema no opera, aunque el instalador sea público.

## Cómo comprobar un instalador

Antes de instalar, calculá la suma SHA-256 del archivo descargado y compará con la publicada en la misma versión. En PowerShell:

```powershell
Get-FileHash .\<instalador> -Algorithm SHA256
```

Si no coincide, no lo instales.

## Soporte

La instalación y la configuración de cada consultorio las realiza el proveedor del sistema.
