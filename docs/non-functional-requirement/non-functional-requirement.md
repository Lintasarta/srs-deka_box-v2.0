# Non-Functional Requirements

*Tabel 5. Non-Functional Requirements*

| ID         | Requirements     | Needs |
|------------|------------------|------|
| DB-NFR-0001 | Performance | Each user action (e.g., creating a Deka Box, adding a bucket, configuring CORS, uploading a file) must complete within ≤ 2 seconds under normal load (≤ 100 concurrent users). |
| DB-NFR-0002 | Scalability | The platform must support ≥ 10,000 active Deka Boxes and ≥ 1,000 concurrent S3 Browser connections without any performance degradation. |
| DB-NFR-0003 | Availability | The service must be available (uptime) ≥ 99.9% per month, with no more than 4 hours of scheduled maintenance in any given month. |
| DB-NFR-0004 | Security | All API and portal communications must use TLS 1.2 or higher; sensitive data (Access Keys, Secret Keys, bucket metadata) must be encrypted with AES-256 both in transit and at rest. |
| DB-NFR-0005 | Auditability | All CRUD operations on Deka Boxes, buckets, and access keys must be recorded in an immutable audit log, retained for at least 365 days and exportable by the Super Admin. |
| DB-NFR-0006 | Usability | The portal UI must conform to WCAG 2.1 AA; every core workflow (e.g., create box, add bucket, apply CORS) must be completable in ≤ 5 clicks. |
| DB-NFR-0007 | Maintainability | The codebase must have ≥ 80% unit-test coverage, adhere to linting standards, and full CI/CD (build + deploy) must complete within ≤ 30 minutes. |
| DB-NFR-0008 | Portability | The application must be containerized and deployable to any Kubernetes-compliant environment via a single Helm chart. |
| DB-NFR-0009 | Reliability | On external API failures (e.g., S3 Browser API), the system must automatically retry up to 3 times; if still unsuccessful, it must switch to a read-only fallback mode. |
| DB-NFR-0010 | Localization | All UI text, error messages, and documentation must be available in English. |
