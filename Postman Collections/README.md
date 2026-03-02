OpenAPI 1.0 Voyage JTTest
---

## 📋 Collection Overview

| Field | Details |
|---|---|
| **Name** | Jobtrain - OpenAPI 1.0 Voyage JTTest |
| **ID** | `15420825-ab4e69a4-b25d-43fd-b892-093bf8a23f9e` |
| **Auth** | Bearer Token (JWT) |

### 📝 Description / README
> Jobtrain's OpenAPI based on the OpenAPI 3.0 specification. You can find out more about Jobtrain at [https://jobtrain.co.uk](https://jobtrain.co.uk).
>
> **Contact Support:** Email: apiteam@jobtrain.co.uk

### ⚙️ Collection-Level Pre-Request Script
```javascript
pm.sendRequest("https://postman-echo.com/get", function (err, response) {
    console.log(response.json());
});
```

---

## 🗂️ Folder Structure (55 folders total)

The collection has **2 top-level folders**, with deep nesting:

### 1. `connect` → `token`
- **`/connect/token`** — POST `{{baseUrl}}/connect/token`

### 2. `api` → `v{version}` → *(20 sub-resource folders)*

#### 📁 candidate (lowercase)
- `{Id}` → **Retrieve candidate applications by ID** — GET `{{baseUrl}}/api/v{{version}}/candidate/:Id`

#### 📁 GetCandidateApplicationById
- `{Id}` → **Retrive Candidate Application by Id** — GET `{{baseUrl}}/api/v{{version}}/GetCandidateApplicationById/:Id`

#### 📁 Candidate (uppercase)
- **GetCandidateApplicationDetailByJobId** → `{candidateId}` → `{jobId}` → **Get Candidate Application Detail By JobId and CandidateId** — GET
- **GetRecentlyUpdatedApplications** → **Get Recently Updated Candidate Application Details** — GET
- **DirectApplyData**:
  - **Direct Apply Integrations** — POST `{{baseUrl}}/api/v{{version}}/Candidate/DirectApplyData`
  - **IndeedCS** — POST `{{baseUrl}}/Application/DirectApplyCandidate`
  - **psychometrictrequest** — POST `{{baseUrl}}/api/v1/PsychometricAssessment/Result`

#### 📁 Jobs
- **list** → **Retrieve a list of jobs** — GET
- **listCandidate** → `{Id}` → **Retrive list of candidates that have applied for this job by Id** — GET
- **GetDBSReadyCandidateByJobId** → `{Id}` → **Retrive list of candidates ready for DBS checks by ID** — GET
- **UpdateDBSUniqueId** → **DBS provider should post the unique reference ID back to Jobtrain** — POST
- **UpdateDBSStatus** → **DBS provider should post the status of each step/stage back to Jobtrain** — POST

#### 📁 Job
- `{Id}` → **Retrive job details details by Id** — GET `{{baseUrl}}/api/v{{version}}/Job/:Id`

#### 📁 Divisions
- List: **list of all divisions** — GET
- `{id}` → **Get division by Id** — GET

#### 📁 Department
- List: **list of all departments** — GET
- `{id}` → **Get department by Id** — GET

#### 📁 Locations
- List: **list of all locations** — GET
- `{id}` → **Get Location by Id** — GET

#### 📁 Region
- List: **list of all regions** — GET
- `{id}` → **Get Region by Id** — GET

#### 📁 JobCategories
- List: **list of all categories** — GET
- `{id}` → **Get Job Categories by Id** — GET

#### 📁 Salaries
- List: **list of all salaries** — GET
- `{id}` → **Get Salaries by Id** — GET

#### 📁 EmploymentTypes
- List: **list of all employment types** — GET
- `{id}` → **Get EmploymentTypes by Id** — GET

#### 📁 JobLevels
- List: **list of all job levels or Grades** — GET
- `{id}` → **Get Job Level by Id** — GET

#### 📁 SchoolLocations
- List: **list of all job school locations** — GET
- `{id}` → **Get School Location by Id** — GET

#### 📁 ApplicationStatus
- List: **list of all application statuses** — GET
- `{id}` → **Get applicationStatus by Id** — GET

#### 📁 JobStatus
- List: **list of all job statuses** — GET
- `{id}` → **Get Job Status by Id** — GET

#### 📁 JobTitle
- List: **list of all job titles** — GET `{{baseUrl}}/api/v{{version}}/JobTitle?PageNo=1&PageSize=20`
- `{id}` → **Get Job Title by Id** — GET

#### 📁 CostCentre
- List: **list of all CostCentre** — GET
- `{id}` → **Get Cost Centre by Id** — GET

#### 📁 Campaign
- List: **list of all Campaigns** — GET
- `{id}` → **Get Campaign by Id** — GET

#### 📁 Integration
- **getstarter form** — GET `{{baseUrl}}/api/v{{version}}/StarterForm/GetNewStarterFormDetail?candidateApplicationId=156`
- **GetRecentlyCancelledStarters** → **list of all Recent Cancelled Starters** — GET
- **GetRecentlyCompletedStarters** → **list of all Recent Complete Starters** — GET `{{baseUrl}}/api/v{{version}}/Integration/GetRecentlyCompletedStarters?PageNo=1&PageSize=20`

---

## 📬 All Requests (45 total)

| # | Method | Name | URL |
|---|---|---|---|
| 1 | GET | list of all job school locations | `{{baseUrl}}/api/v{{version}}/SchoolLocations` |
| 2 | POST | Direct Apply Integrations | `{{baseUrl}}/api/v{{version}}/Candidate/DirectApplyData` |
| 3 | GET | Get division by Id | `{{baseUrl}}/api/v{{version}}/Divisions/:id` |
| 4 | GET | Get Cost Centre by Id | `{{baseUrl}}/api/v{{version}}/CostCentre/:id` |
| 5 | GET | Get School Location by Id | `{{baseUrl}}/api/v{{version}}/SchoolLocations/:id` |
| 6 | GET | list of all salaries | `{{baseUrl}}/api/v{{version}}/Salaries` |
| 7 | GET | Retrive list of candidates ready for DBS checks by ID | `{{baseUrl}}/api/v{{version}}/Jobs/GetDBSReadyCandidateByJobId/:Id` |
| 8 | POST | IndeedCS | `{{baseUrl}}/Application/DirectApplyCandidate` |
| 9 | GET | list of all Recent Cancelled Starters | `{{baseUrl}}/api/v{{version}}/Integration/GetRecentlyCancelledStarters` |
| 10 | GET | Get Region by Id | `{{baseUrl}}/api/v{{version}}/Region/:id` |
| 11 | GET | list of all divisions | `{{baseUrl}}/api/v{{version}}/Divisions` |
| 12 | GET | Retrive job details details by Id | `{{baseUrl}}/api/v{{version}}/Job/:Id` |
| 13 | GET | list of all application statuses | `{{baseUrl}}/api/v{{version}}/ApplicationStatus` |
| 14 | POST | /connect/token | `{{baseUrl}}/connect/token` |
| 15 | GET | list of all departments | `{{baseUrl}}/api/v{{version}}/Department` |
| 16 | GET | Get Location by Id | `{{baseUrl}}/api/v{{version}}/Locations/:id` |
| 17 | GET | Get EmploymentTypes by Id | `{{baseUrl}}/api/v{{version}}/EmploymentTypes/:id` |
| 18 | GET | list of all employment types | `{{baseUrl}}/api/v{{version}}/EmploymentTypes` |
| 19 | GET | Get Recently Updated Candidate Application Details | `{{baseUrl}}/api/v{{version}}/Candidate/GetRecentlyUpdatedApplications` |
| 20 | GET | getstarter form | `{{baseUrl}}/api/v{{version}}/StarterForm/GetNewStarterFormDetail?candidateApplicationId=156` |
| 21 | GET | list of all job statuses | `{{baseUrl}}/api/v{{version}}/JobStatus` |
| 22 | GET | Get Campaign by Id | `{{baseUrl}}/api/v{{version}}/Campaign/:id` |
| 23 | GET | Retrive Candidate Application by Id | `{{baseUrl}}/api/v{{version}}/GetCandidateApplicationById/:Id` |
| 24 | GET | list of all Campaigns | `{{baseUrl}}/api/v{{version}}/Campaign` |
| 25 | POST | psychometrictrequest | `{{baseUrl}}/api/v1/PsychometricAssessment/Result` |
| 26 | GET | Retrieve a list of jobs | `{{baseUrl}}/api/v{{version}}/Jobs/list` |
| 27 | GET | Get applicationStatus by Id | `{{baseUrl}}/api/v{{version}}/ApplicationStatus/:id` |
| 28 | GET | Get Job Level by Id | `{{baseUrl}}/api/v{{version}}/JobLevels/:id` |
| 29 | GET | Get Job Title by Id | `{{baseUrl}}/api/v{{version}}/JobTitle/:id` |
| 30 | GET | list of all job levels or Grades | `{{baseUrl}}/api/v{{version}}/JobLevels` |
| 31 | GET | Get department by Id | `{{baseUrl}}/api/v{{version}}/Department/:id` |
| 32 | GET | Get Job Categories by Id | `{{baseUrl}}/api/v{{version}}/JobCategories/:id` |
| 33 | GET | Get Candidate Application Detail By JobId and CandidateId | `{{baseUrl}}/api/v{{version}}/Candidate/GetCandidateApplicationDetailByJobId/:candidateId/:jobId` |
| 34 | GET | list of all categories | `{{baseUrl}}/api/v{{version}}/JobCategories` |
| 35 | GET | list of all Recent Complete Starters | `{{baseUrl}}/api/v{{version}}/Integration/GetRecentlyCompletedStarters?PageNo=1&PageSize=20` |
| 36 | POST | DBS provider should post the status back to Jobtrain | `{{baseUrl}}/api/v{{version}}/Jobs/UpdateDBSStatus` |
| 37 | GET | list of all regions | `{{baseUrl}}/api/v{{version}}/Region` |
| 38 | GET | Retrive list of candidates that have applied for this job by Id | `{{baseUrl}}/api/v{{version}}/Jobs/listCandidate/:Id` |
| 39 | GET | list of all locations | `{{baseUrl}}/api/v{{version}}/Locations` |
| 40 | GET | Get Salaries by Id | `{{baseUrl}}/api/v{{version}}/Salaries/:id` |
| 41 | GET | Get Job Status by Id | `{{baseUrl}}/api/v{{version}}/JobStatus/:id` |
| 42 | GET | Retrieve candidate applications by ID | `{{baseUrl}}/api/v{{version}}/candidate/:Id` |
| 43 | GET | list of all job titles | `{{baseUrl}}/api/v{{version}}/JobTitle?PageNo=1&PageSize=20` |
| 44 | POST | DBS provider should post the unique reference ID back to Jobtrain | `{{baseUrl}}/api/v{{version}}/Jobs/UpdateDBSUniqueId` |
| 45 | GET | list of all CostCentre | `{{baseUrl}}/api/v{{version}}/CostCentre` |

---

## 🔑 Key Notes
- **Auth**: Bearer token set at collection level (JWT, inherited by all requests)
- **Variables used**: `{{baseUrl}}` and `{{version}}` throughout all requests
- **No folder descriptions** — all 55 folders have `null` descriptions
- **No collection-level tests** script
- **Pre-request script** at collection level pings `postman-echo.com` (likely a leftover/test script)

Here's a summary of the **README** and structure for the [Jobtrain - OpenAPI 1.0 Voyage JTTest](collection/15420825-ab4e69a4-b25d-43fd-b892-093bf8a23f9e) collection:

---

### 📝 README / Description

> **Jobtrain's OpenAPI** based on the OpenAPI 3.0 specification.
> Find out more at [https://jobtrain.co.uk](https://jobtrain.co.uk)
> **Contact:** apiteam@jobtrain.co.uk

---

### 🗂️ Collection Structure

- **Auth:** Bearer Token (JWT) — set at collection level, inherited by all requests
- **Variables:** `{{baseUrl}}` and `{{version}}` used throughout
- **55 folders**, **45 requests** total
- **Pre-request script** at collection level (pings postman-echo.com — likely a leftover test script)

---

### 📁 Top-Level Folders & Requests

| Folder | Requests |
|---|---|
| `connect/token` | POST `/connect/token` (Authentication) |
| `api/v{version}/Jobs` | List jobs, List candidates by job, DBS checks, Update DBS ID/Status |
| `api/v{version}/Job` | Get job by ID |
| `api/v{version}/Candidate` | Get by ID, Recently updated apps, DirectApply, IndeedCS, Psychometric |
| `api/v{version}/GetCandidateApplicationById` | Get candidate application by ID |
| `api/v{version}/Divisions` | List all, Get by ID |
| `api/v{version}/Department` | List all, Get by ID |
| `api/v{version}/Locations` | List all, Get by ID |
| `api/v{version}/Region` | List all, Get by ID |
| `api/v{version}/JobCategories` | List all, Get by ID |
| `api/v{version}/Salaries` | List all, Get by ID |
| `api/v{version}/EmploymentTypes` | List all, Get by ID |
| `api/v{version}/JobLevels` | List all, Get by ID |
| `api/v{version}/SchoolLocations` | List all, Get by ID |
| `api/v{version}/ApplicationStatus` | List all, Get by ID |
| `api/v{version}/JobStatus` | List all, Get by ID |
| `api/v{version}/JobTitle` | List all (paginated), Get by ID |
| `api/v{version}/CostCentre` | List all, Get by ID |
| `api/v{version}/Campaign` | List all, Get by ID |
| `api/v{version}/Integration` | Starter form, Recently cancelled/completed starters |

---

**Note:** No folder-level descriptions are set — all 55 folders have empty descriptions. Would you like me to add descriptions to the folders, fix the pre-request script, or help with anything else in this collection?

