import EdgeRouteWebhookVerificationModuleReplaceRequest from './examples/_edge_route_webhook_verification_module_replace_request.md';
import EdgeRouteWebhookVerificationModuleReplaceResponse from './examples/_edge_route_webhook_verification_module_replace_response.md';
import EdgeRouteWebhookVerificationModuleGetRequest from './examples/_edge_route_webhook_verification_module_get_request.md';
import EdgeRouteWebhookVerificationModuleGetResponse from './examples/_edge_route_webhook_verification_module_get_response.md';
import EdgeRouteWebhookVerificationModuleDeleteRequest from './examples/_edge_route_webhook_verification_module_delete_request.md';


# HTTPS Edge Route Webhook Verification Module
------------------


## Replace HTTPS Edge Route Webhook Verification Module

### Request

PUT /edges/https/{edge_id}/routes/{id}/webhook_verification

<EdgeRouteWebhookVerificationModuleReplaceRequest />

#### Parameters

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `enabled` | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| `provider` | string | a string indicating which webhook provider will be sending webhooks to this endpoint. Value must be one of the supported providers defined at https://ngrok.com/docs/cloud-edge#webhook-verification |
| `secret` | string | a string secret used to validate requests from the given provider. All providers except AWS SNS require a secret |

### Response

Returns a 200 response  on success

<EdgeRouteWebhookVerificationModuleReplaceResponse />

#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `enabled` | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| `provider` | string | a string indicating which webhook provider will be sending webhooks to this endpoint. Value must be one of the supported providers defined at https://ngrok.com/docs/cloud-edge#webhook-verification |
| `secret` | string | a string secret used to validate requests from the given provider. All providers except AWS SNS require a secret |


## Get HTTPS Edge Route Webhook Verification Module

### Request

GET /edges/https/{edge_id}/routes/{id}/webhook_verification

<EdgeRouteWebhookVerificationModuleGetRequest />

### Response

Returns a 200 response  on success

<EdgeRouteWebhookVerificationModuleGetResponse />

#### Fields

|&nbsp;| &nbsp;| &nbsp;|
|---|---|---|
| `enabled` | boolean | `true` if the module will be applied to traffic, `false` to disable. default `true` if unspecified |
| `provider` | string | a string indicating which webhook provider will be sending webhooks to this endpoint. Value must be one of the supported providers defined at https://ngrok.com/docs/cloud-edge#webhook-verification |
| `secret` | string | a string secret used to validate requests from the given provider. All providers except AWS SNS require a secret |


## Delete HTTPS Edge Route Webhook Verification Module

### Request

DELETE /edges/https/{edge_id}/routes/{id}/webhook_verification

<EdgeRouteWebhookVerificationModuleDeleteRequest />

### Response

Returns a 204 response with no body on success