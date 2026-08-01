# PaymentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPaymentApiV1DocumentsInvoiceIdPaymentsPost**](PaymentsApi.md#createPaymentApiV1DocumentsInvoiceIdPaymentsPost) | **POST** /api/v1/documents/{invoice_id}/payments | Create Payment |
| [**deletePaymentApiV1PaymentsPaymentIdDelete**](PaymentsApi.md#deletePaymentApiV1PaymentsPaymentIdDelete) | **DELETE** /api/v1/payments/{payment_id} | Delete Payment |
| [**getPaymentApiV1PaymentsPaymentIdGet**](PaymentsApi.md#getPaymentApiV1PaymentsPaymentIdGet) | **GET** /api/v1/payments/{payment_id} | Get Payment |
| [**listInvoicePaymentsApiV1DocumentsInvoiceIdPaymentsGet**](PaymentsApi.md#listInvoicePaymentsApiV1DocumentsInvoiceIdPaymentsGet) | **GET** /api/v1/documents/{invoice_id}/payments | List Invoice Payments |
| [**updatePaymentApiV1PaymentsPaymentIdPatch**](PaymentsApi.md#updatePaymentApiV1PaymentsPaymentIdPatch) | **PATCH** /api/v1/payments/{payment_id} | Update Payment |


<a id="createPaymentApiV1DocumentsInvoiceIdPaymentsPost"></a>
# **createPaymentApiV1DocumentsInvoiceIdPaymentsPost**
> PaymentResponse createPaymentApiV1DocumentsInvoiceIdPaymentsPost(invoiceId, paymentCreateRequest)

Create Payment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.PaymentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    PaymentsApi apiInstance = new PaymentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    PaymentCreateRequest paymentCreateRequest = new PaymentCreateRequest(); // PaymentCreateRequest | 
    try {
      PaymentResponse result = apiInstance.createPaymentApiV1DocumentsInvoiceIdPaymentsPost(invoiceId, paymentCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentsApi#createPaymentApiV1DocumentsInvoiceIdPaymentsPost");
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
| **invoiceId** | **String**|  | |
| **paymentCreateRequest** | [**PaymentCreateRequest**](PaymentCreateRequest.md)|  | |

### Return type

[**PaymentResponse**](PaymentResponse.md)

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

<a id="deletePaymentApiV1PaymentsPaymentIdDelete"></a>
# **deletePaymentApiV1PaymentsPaymentIdDelete**
> SimpleBoolResponse deletePaymentApiV1PaymentsPaymentIdDelete(paymentId)

Delete Payment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.PaymentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    PaymentsApi apiInstance = new PaymentsApi(defaultClient);
    String paymentId = "paymentId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deletePaymentApiV1PaymentsPaymentIdDelete(paymentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentsApi#deletePaymentApiV1PaymentsPaymentIdDelete");
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
| **paymentId** | **String**|  | |

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

<a id="getPaymentApiV1PaymentsPaymentIdGet"></a>
# **getPaymentApiV1PaymentsPaymentIdGet**
> PaymentResponse getPaymentApiV1PaymentsPaymentIdGet(paymentId)

Get Payment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.PaymentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    PaymentsApi apiInstance = new PaymentsApi(defaultClient);
    String paymentId = "paymentId_example"; // String | 
    try {
      PaymentResponse result = apiInstance.getPaymentApiV1PaymentsPaymentIdGet(paymentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentsApi#getPaymentApiV1PaymentsPaymentIdGet");
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
| **paymentId** | **String**|  | |

### Return type

[**PaymentResponse**](PaymentResponse.md)

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

<a id="listInvoicePaymentsApiV1DocumentsInvoiceIdPaymentsGet"></a>
# **listInvoicePaymentsApiV1DocumentsInvoiceIdPaymentsGet**
> PaymentsListResponse listInvoicePaymentsApiV1DocumentsInvoiceIdPaymentsGet(invoiceId, limit, cursor)

List Invoice Payments

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.PaymentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    PaymentsApi apiInstance = new PaymentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    Integer limit = 50; // Integer | 
    String cursor = "cursor_example"; // String | 
    try {
      PaymentsListResponse result = apiInstance.listInvoicePaymentsApiV1DocumentsInvoiceIdPaymentsGet(invoiceId, limit, cursor);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentsApi#listInvoicePaymentsApiV1DocumentsInvoiceIdPaymentsGet");
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
| **invoiceId** | **String**|  | |
| **limit** | **Integer**|  | [optional] [default to 50] |
| **cursor** | **String**|  | [optional] |

### Return type

[**PaymentsListResponse**](PaymentsListResponse.md)

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

<a id="updatePaymentApiV1PaymentsPaymentIdPatch"></a>
# **updatePaymentApiV1PaymentsPaymentIdPatch**
> PaymentResponse updatePaymentApiV1PaymentsPaymentIdPatch(paymentId, paymentPatchRequest)

Update Payment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.PaymentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    PaymentsApi apiInstance = new PaymentsApi(defaultClient);
    String paymentId = "paymentId_example"; // String | 
    PaymentPatchRequest paymentPatchRequest = new PaymentPatchRequest(); // PaymentPatchRequest | 
    try {
      PaymentResponse result = apiInstance.updatePaymentApiV1PaymentsPaymentIdPatch(paymentId, paymentPatchRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PaymentsApi#updatePaymentApiV1PaymentsPaymentIdPatch");
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
| **paymentId** | **String**|  | |
| **paymentPatchRequest** | [**PaymentPatchRequest**](PaymentPatchRequest.md)|  | |

### Return type

[**PaymentResponse**](PaymentResponse.md)

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

