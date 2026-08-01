# InvoiceAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost**](InvoiceAttachmentsApi.md#createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost) | **POST** /api/v1/invoices/{invoice_id}/attachments | Create Attachment |
| [**deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete**](InvoiceAttachmentsApi.md#deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete) | **DELETE** /api/v1/invoices/{invoice_id}/attachments/{attachment_id} | Delete Attachment |
| [**listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet**](InvoiceAttachmentsApi.md#listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet) | **GET** /api/v1/invoices/{invoice_id}/attachments | List Attachments |


<a id="createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost"></a>
# **createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost**
> InvoiceAttachmentResponse createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost(invoiceId, invoiceAttachmentCreateRequest)

Create Attachment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoiceAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoiceAttachmentsApi apiInstance = new InvoiceAttachmentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    InvoiceAttachmentCreateRequest invoiceAttachmentCreateRequest = new InvoiceAttachmentCreateRequest(); // InvoiceAttachmentCreateRequest | 
    try {
      InvoiceAttachmentResponse result = apiInstance.createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost(invoiceId, invoiceAttachmentCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceAttachmentsApi#createAttachmentApiV1InvoicesInvoiceIdAttachmentsPost");
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
| **invoiceAttachmentCreateRequest** | [**InvoiceAttachmentCreateRequest**](InvoiceAttachmentCreateRequest.md)|  | |

### Return type

[**InvoiceAttachmentResponse**](InvoiceAttachmentResponse.md)

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

<a id="deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete"></a>
# **deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete**
> SimpleBoolResponse deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete(invoiceId, attachmentId)

Delete Attachment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoiceAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoiceAttachmentsApi apiInstance = new InvoiceAttachmentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    String attachmentId = "attachmentId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete(invoiceId, attachmentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceAttachmentsApi#deleteAttachmentApiV1InvoicesInvoiceIdAttachmentsAttachmentIdDelete");
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
| **attachmentId** | **String**|  | |

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

<a id="listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet"></a>
# **listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet**
> InvoiceAttachmentsListResponse listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet(invoiceId)

List Attachments

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.InvoiceAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    InvoiceAttachmentsApi apiInstance = new InvoiceAttachmentsApi(defaultClient);
    String invoiceId = "invoiceId_example"; // String | 
    try {
      InvoiceAttachmentsListResponse result = apiInstance.listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet(invoiceId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling InvoiceAttachmentsApi#listAttachmentsApiV1InvoicesInvoiceIdAttachmentsGet");
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

### Return type

[**InvoiceAttachmentsListResponse**](InvoiceAttachmentsListResponse.md)

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

