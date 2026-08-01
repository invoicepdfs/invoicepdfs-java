# WebhooksApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createWebhookEndpointApiV1WebhookEndpointsPost**](WebhooksApi.md#createWebhookEndpointApiV1WebhookEndpointsPost) | **POST** /api/v1/webhook-endpoints | Create Webhook Endpoint |
| [**deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete**](WebhooksApi.md#deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete) | **DELETE** /api/v1/webhook-endpoints/{endpoint_id} | Delete Webhook Endpoint |
| [**getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet**](WebhooksApi.md#getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet) | **GET** /api/v1/webhook-deliveries/{delivery_id} | Get Webhook Delivery |
| [**getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet**](WebhooksApi.md#getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet) | **GET** /api/v1/webhook-endpoints/{endpoint_id} | Get Webhook Endpoint |
| [**listWebhookDeliveriesApiV1WebhookDeliveriesGet**](WebhooksApi.md#listWebhookDeliveriesApiV1WebhookDeliveriesGet) | **GET** /api/v1/webhook-deliveries | List Webhook Deliveries |
| [**listWebhookEndpointsApiV1WebhookEndpointsGet**](WebhooksApi.md#listWebhookEndpointsApiV1WebhookEndpointsGet) | **GET** /api/v1/webhook-endpoints | List Webhook Endpoints |
| [**retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost**](WebhooksApi.md#retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost) | **POST** /api/v1/webhook-deliveries/{delivery_id}/retry | Retry Webhook Delivery |
| [**rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost**](WebhooksApi.md#rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/rotate-secret | Rotate Webhook Secret |
| [**testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost**](WebhooksApi.md#testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost) | **POST** /api/v1/webhook-endpoints/{endpoint_id}/test | Test Webhook Endpoint |
| [**updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch**](WebhooksApi.md#updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch) | **PATCH** /api/v1/webhook-endpoints/{endpoint_id} | Update Webhook Endpoint |


<a id="createWebhookEndpointApiV1WebhookEndpointsPost"></a>
# **createWebhookEndpointApiV1WebhookEndpointsPost**
> WebhookEndpointResponse createWebhookEndpointApiV1WebhookEndpointsPost(webhookEndpointCreateRequest)

Create Webhook Endpoint

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    WebhookEndpointCreateRequest webhookEndpointCreateRequest = new WebhookEndpointCreateRequest(); // WebhookEndpointCreateRequest | 
    try {
      WebhookEndpointResponse result = apiInstance.createWebhookEndpointApiV1WebhookEndpointsPost(webhookEndpointCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#createWebhookEndpointApiV1WebhookEndpointsPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **webhookEndpointCreateRequest** | [**WebhookEndpointCreateRequest**](WebhookEndpointCreateRequest.md)|  | |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete"></a>
# **deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete**
> SimpleBoolResponse deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete(endpointId)

Delete Webhook Endpoint

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String endpointId = "endpointId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete(endpointId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#deleteWebhookEndpointApiV1WebhookEndpointsEndpointIdDelete");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **endpointId** | **String**|  | |

### Return type

[**SimpleBoolResponse**](SimpleBoolResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet"></a>
# **getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet**
> WebhookDeliveryResponse getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet(deliveryId)

Get Webhook Delivery

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String deliveryId = "deliveryId_example"; // String | 
    try {
      WebhookDeliveryResponse result = apiInstance.getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet(deliveryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#getWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **deliveryId** | **String**|  | |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet"></a>
# **getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet**
> WebhookEndpointResponse getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet(endpointId)

Get Webhook Endpoint

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String endpointId = "endpointId_example"; // String | 
    try {
      WebhookEndpointResponse result = apiInstance.getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet(endpointId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#getWebhookEndpointApiV1WebhookEndpointsEndpointIdGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **endpointId** | **String**|  | |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="listWebhookDeliveriesApiV1WebhookDeliveriesGet"></a>
# **listWebhookDeliveriesApiV1WebhookDeliveriesGet**
> WebhookDeliveriesListResponse listWebhookDeliveriesApiV1WebhookDeliveriesGet(limit, cursor)

List Webhook Deliveries

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      WebhookDeliveriesListResponse result = apiInstance.listWebhookDeliveriesApiV1WebhookDeliveriesGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#listWebhookDeliveriesApiV1WebhookDeliveriesGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**WebhookDeliveriesListResponse**](WebhookDeliveriesListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="listWebhookEndpointsApiV1WebhookEndpointsGet"></a>
# **listWebhookEndpointsApiV1WebhookEndpointsGet**
> WebhookEndpointsListResponse listWebhookEndpointsApiV1WebhookEndpointsGet(limit, cursor)

List Webhook Endpoints

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      WebhookEndpointsListResponse result = apiInstance.listWebhookEndpointsApiV1WebhookEndpointsGet(limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#listWebhookEndpointsApiV1WebhookEndpointsGet");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**WebhookEndpointsListResponse**](WebhookEndpointsListResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost"></a>
# **retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost**
> WebhookDeliveryResponse retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost(deliveryId)

Retry Webhook Delivery

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String deliveryId = "deliveryId_example"; // String | 
    try {
      WebhookDeliveryResponse result = apiInstance.retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost(deliveryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#retryWebhookDeliveryApiV1WebhookDeliveriesDeliveryIdRetryPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **deliveryId** | **String**|  | |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost"></a>
# **rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost**
> WebhookSecretResponse rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost(endpointId)

Rotate Webhook Secret

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String endpointId = "endpointId_example"; // String | 
    try {
      WebhookSecretResponse result = apiInstance.rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost(endpointId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#rotateWebhookSecretApiV1WebhookEndpointsEndpointIdRotateSecretPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **endpointId** | **String**|  | |

### Return type

[**WebhookSecretResponse**](WebhookSecretResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost"></a>
# **testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost**
> WebhookDeliveryResponse testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost(endpointId)

Test Webhook Endpoint

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String endpointId = "endpointId_example"; // String | 
    try {
      WebhookDeliveryResponse result = apiInstance.testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost(endpointId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#testWebhookEndpointApiV1WebhookEndpointsEndpointIdTestPost");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **endpointId** | **String**|  | |

### Return type

[**WebhookDeliveryResponse**](WebhookDeliveryResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

<a id="updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch"></a>
# **updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch**
> WebhookEndpointResponse updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch(endpointId, webhookEndpointPatchRequest)

Update Webhook Endpoint

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.WebhooksApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    WebhooksApi apiInstance = new WebhooksApi(defaultClient);
    String endpointId = "endpointId_example"; // String | 
    WebhookEndpointPatchRequest webhookEndpointPatchRequest = new WebhookEndpointPatchRequest(); // WebhookEndpointPatchRequest | 
    try {
      WebhookEndpointResponse result = apiInstance.updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch(endpointId, webhookEndpointPatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling WebhooksApi#updateWebhookEndpointApiV1WebhookEndpointsEndpointIdPatch");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **endpointId** | **String**|  | |
| **webhookEndpointPatchRequest** | [**WebhookEndpointPatchRequest**](WebhookEndpointPatchRequest.md)|  | |

### Return type

[**WebhookEndpointResponse**](WebhookEndpointResponse.md)

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Successful Response |  -  |
| **422** | Validation Error |  -  |

