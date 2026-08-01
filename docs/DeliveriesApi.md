# DeliveriesApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**getDeliveryApiV1DeliveriesDeliveryIdGet**](DeliveriesApi.md#getDeliveryApiV1DeliveriesDeliveryIdGet) | **GET** /api/v1/deliveries/{delivery_id} | Get Delivery |
| [**retryDeliveryApiV1DeliveriesDeliveryIdRetryPost**](DeliveriesApi.md#retryDeliveryApiV1DeliveriesDeliveryIdRetryPost) | **POST** /api/v1/deliveries/{delivery_id}/retry | Retry Delivery |


<a id="getDeliveryApiV1DeliveriesDeliveryIdGet"></a>
# **getDeliveryApiV1DeliveriesDeliveryIdGet**
> DeliveryResponse getDeliveryApiV1DeliveriesDeliveryIdGet(deliveryId)

Get Delivery

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DeliveriesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DeliveriesApi apiInstance = new DeliveriesApi(defaultClient);
    String deliveryId = "deliveryId_example"; // String | 
    try {
      DeliveryResponse result = apiInstance.getDeliveryApiV1DeliveriesDeliveryIdGet(deliveryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeliveriesApi#getDeliveryApiV1DeliveriesDeliveryIdGet");
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

[**DeliveryResponse**](DeliveryResponse.md)

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

<a id="retryDeliveryApiV1DeliveriesDeliveryIdRetryPost"></a>
# **retryDeliveryApiV1DeliveriesDeliveryIdRetryPost**
> DeliveryResponse retryDeliveryApiV1DeliveriesDeliveryIdRetryPost(deliveryId)

Retry Delivery

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DeliveriesApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DeliveriesApi apiInstance = new DeliveriesApi(defaultClient);
    String deliveryId = "deliveryId_example"; // String | 
    try {
      DeliveryResponse result = apiInstance.retryDeliveryApiV1DeliveriesDeliveryIdRetryPost(deliveryId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DeliveriesApi#retryDeliveryApiV1DeliveriesDeliveryIdRetryPost");
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

[**DeliveryResponse**](DeliveryResponse.md)

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

