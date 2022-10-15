import CertificateAuthoritiesCreateRequest from './examples/_certificate_authorities_create_request.md';
import CertificateAuthoritiesCreateResponse from './examples/_certificate_authorities_create_response.md';
import CertificateAuthoritiesDeleteRequest from './examples/_certificate_authorities_delete_request.md';
import CertificateAuthoritiesGetRequest from './examples/_certificate_authorities_get_request.md';
import CertificateAuthoritiesGetResponse from './examples/_certificate_authorities_get_response.md';
import CertificateAuthoritiesListRequest from './examples/_certificate_authorities_list_request.md';
import CertificateAuthoritiesListResponse from './examples/_certificate_authorities_list_response.md';
import CertificateAuthoritiesUpdateRequest from './examples/_certificate_authorities_update_request.md';
import CertificateAuthoritiesUpdateResponse from './examples/_certificate_authorities_update_response.md';

# Certificate Authorities
------------------


## Create Certificate Authority

Upload a new Certificate Authority

### Request

POST /certificate_authorities

<CertificateAuthoritiesCreateRequest />

#### Parameters

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `description` | string | human-readable description of this Certificate Authority. optional, max 255 bytes. |
| `metadata` | string | arbitrary user-defined machine-readable data of this Certificate Authority. optional, max 4096 bytes. |
| `ca_pem` | string | raw PEM of the Certificate Authority |

### Response

Returns a 201 response  on success

<CertificateAuthoritiesCreateResponse />

#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `id` | string | unique identifier for this Certificate Authority |
| `uri` | string | URI of the Certificate Authority API resource |
| `created_at` | string | timestamp when the Certificate Authority was created, RFC 3339 format |
| `description` | string | human-readable description of this Certificate Authority. optional, max 255 bytes. |
| `metadata` | string | arbitrary user-defined machine-readable data of this Certificate Authority. optional, max 4096 bytes. |
| `ca_pem` | string | raw PEM of the Certificate Authority |
| `subject_common_name` | string | subject common name of the Certificate Authority |
| `not_before` | string | timestamp when this Certificate Authority becomes valid, RFC 3339 format |
| `not_after` | string | timestamp when this Certificate Authority becomes invalid, RFC 3339 format |
| `key_usages` | List&lt;string&gt; | set of actions the private key of this Certificate Authority can be used for |
| `extended_key_usages` | List&lt;string&gt; | extended set of actions the private key of this Certificate Authority can be used for |


## Delete Certificate Authority

Delete a Certificate Authority

### Request

DELETE /certificate_authorities/{id}

<CertificateAuthoritiesDeleteRequest />

### Response

Returns a 204 response with no body on success


## Get Certificate Authority

Get detailed information about a certficate authority

### Request

GET /certificate_authorities/{id}

<CertificateAuthoritiesGetRequest />

### Response

Returns a 200 response  on success

<CertificateAuthoritiesGetResponse />

#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `id` | string | unique identifier for this Certificate Authority |
| `uri` | string | URI of the Certificate Authority API resource |
| `created_at` | string | timestamp when the Certificate Authority was created, RFC 3339 format |
| `description` | string | human-readable description of this Certificate Authority. optional, max 255 bytes. |
| `metadata` | string | arbitrary user-defined machine-readable data of this Certificate Authority. optional, max 4096 bytes. |
| `ca_pem` | string | raw PEM of the Certificate Authority |
| `subject_common_name` | string | subject common name of the Certificate Authority |
| `not_before` | string | timestamp when this Certificate Authority becomes valid, RFC 3339 format |
| `not_after` | string | timestamp when this Certificate Authority becomes invalid, RFC 3339 format |
| `key_usages` | List&lt;string&gt; | set of actions the private key of this Certificate Authority can be used for |
| `extended_key_usages` | List&lt;string&gt; | extended set of actions the private key of this Certificate Authority can be used for |


## List Certificate Authorities

List all Certificate Authority on this account

### Request

GET /certificate_authorities

<CertificateAuthoritiesListRequest />

### Response

Returns a 200 response  on success

<CertificateAuthoritiesListResponse />

#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `certificate_authorities` | [CertificateAuthority](#api-certificate-authorities-list-fields-certificate-authority) | the list of all certificate authorities on this account |
| `uri` | string | URI of the certificates authorities list API resource |
| `next_page_uri` | string | URI of the next page, or null if there is no next page |

#### CertificateAuthority fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `id` | string | unique identifier for this Certificate Authority |
| `uri` | string | URI of the Certificate Authority API resource |
| `created_at` | string | timestamp when the Certificate Authority was created, RFC 3339 format |
| `description` | string | human-readable description of this Certificate Authority. optional, max 255 bytes. |
| `metadata` | string | arbitrary user-defined machine-readable data of this Certificate Authority. optional, max 4096 bytes. |
| `ca_pem` | string | raw PEM of the Certificate Authority |
| `subject_common_name` | string | subject common name of the Certificate Authority |
| `not_before` | string | timestamp when this Certificate Authority becomes valid, RFC 3339 format |
| `not_after` | string | timestamp when this Certificate Authority becomes invalid, RFC 3339 format |
| `key_usages` | List&lt;string&gt; | set of actions the private key of this Certificate Authority can be used for |
| `extended_key_usages` | List&lt;string&gt; | extended set of actions the private key of this Certificate Authority can be used for |


## Update Certificate Authority

Update attributes of a Certificate Authority by ID

### Request

PATCH /certificate_authorities/{id}

<CertificateAuthoritiesUpdateRequest />

#### Parameters

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `id` | string |  |
| `description` | string | human-readable description of this Certificate Authority. optional, max 255 bytes. |
| `metadata` | string | arbitrary user-defined machine-readable data of this Certificate Authority. optional, max 4096 bytes. |


### Response

Returns a 200 response  on success

<CertificateAuthoritiesUpdateResponse />

#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `id` | string | unique identifier for this Certificate Authority |
| `uri` | string | URI of the Certificate Authority API resource |
| `created_at` | string | timestamp when the Certificate Authority was created, RFC 3339 format |
| `description` | string | human-readable description of this Certificate Authority. optional, max 255 bytes. |
| `metadata` | string | arbitrary user-defined machine-readable data of this Certificate Authority. optional, max 4096 bytes. |
| `ca_pem` | string | raw PEM of the Certificate Authority |
| `subject_common_name` | string | subject common name of the Certificate Authority |
| `not_before` | string | timestamp when this Certificate Authority becomes valid, RFC 3339 format |
| `not_after` | string | timestamp when this Certificate Authority becomes invalid, RFC 3339 format |
| `key_usages` | List&lt;string&gt; | set of actions the private key of this Certificate Authority can be used for |
| `extended_key_usages` | List&lt;string&gt; | extended set of actions the private key of this Certificate Authority can be used for |