# Retarus Cloud Fax REST APIs
Contains OpenAPI descriptions and documentation for Retarus Cloud Fax APIs.

## Directory Structure Explanation

### `/latest/` Directory

#### Purpose
- Contains the current, active versions of all APIs.

#### Redocly Integration
- Individual `openapi/` subdirectories are watched by **Redocly** for documentation generation.

#### Content
- Each API has its own subdirectory with **OpenAPI 3.x** specifications and additional content.

#### Format
- **OpenAPI 3.x only** — no Swagger 2.x files.

---

### `/latest/*/openapi/` Subdirectories

- **Redocly watched:** These specific folders are monitored by Redocly for changes.
- **Build trigger:** Changes to files in these directories trigger API documentation builds.

**Subdirectories:**
- `latest/sending-fax-api/openapi/`
- `latest/receiving-fax-api/openapi/`
- `latest/fax-status-push-api/openapi/`

---

### `/legacy/` Directory

#### Purpose
- Contains final **Swagger 2.x** specifications for legacy compatibility.

⚠️ **DEPRECATED**  
These files are in legacy maintenance mode and will not receive updates.

#### Redocly Integration
- Not watched by Redocly but available for download.

#### Maintenance
- **NO ACTIVE MAINTENANCE** — Use OpenAPI 3.x specifications in `/latest/` for all new development.

---

### `/versions/` Directory

#### Purpose
- Archives historical versions of APIs for reference.

#### Format & Content
- Contains only **OpenAPI 3.x** files and changelogs.

---

## Fax REST APIs Overview

**Retarus Cloud Fax** provides three main REST APIs:

### 1. Sending Fax API
- Handles fax transmission, scheduling, and delivery management.

  - **Current Version:** Located in `latest/sending-fax-api/` (**OpenAPI 3.x**)
  - **Legacy Version:** `legacy/sending-fax-api-swagger-2x.json` ⚠️ DEPRECATED
  - **Historical Versions:** `versions/sending-fax-api/v1.0/`...

### 2. Receiving Fax API
- Manages incoming fax reception, processing, and notification handling.

  - **Current Version:** Located in `latest/receiving-fax-api/` (**OpenAPI 3.x**)
  - **Legacy Version:** `legacy/receiving-fax-api-swagger-2x.json` ⚠️ DEPRECATED
  - **Historical Versions:** `versions/receiving-fax-api/v1.0/`...

### 4. Fax Status API
- Provides real-time status tracking and delivery confirmation for sent faxes.

  - **Current Version:** Located in `latest/fax-status-push-api/` (**OpenAPI 3.x**)
  - **Legacy Version:** `legacy/fax-status-api-swagger-2.x.json` ⚠️ DEPRECATED
  - **Historical Versions:** `versions/fax-status-api/v1.0/`...

---

## ⚠️ Important: Swagger 2.x Deprecation Notice

Swagger 2.x specifications in the `/legacy/` directory are **DEPRECATED** and in maintenance mode:

- **No updates:** Legacy Swagger 2.x files will not receive any updates, bug fixes, or new features.
- **OpenAPI 3.x only:** All future development will use OpenAPI 3.x format exclusively.
- **Legacy support:** Swagger 2.x files are maintained only for existing integrations that cannot be immediately upgraded.
- **End of life:** Swagger 2.x support will be completely removed in a future release.

---

## Working with This Repository

### Update Workflow

The current workflow for updating documentation is as follows:

- **Source repository:** OpenAPI descriptions are developed and maintained in Bitbucket.
- **Manual upload:** Updated OpenAPI description files are manually uploaded to this GitHub repository under the appropriate `latest/*/openapi/` directories.
- **Documentation updates:** Manual uploads to GitHub automatically trigger documentation updates via Redocly.
