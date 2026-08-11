# DocumentAttachmentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createDocumentAttachment**](DocumentAttachmentsApi.md#createDocumentAttachment) | **POST** /api/v1/documents/{document_id}/attachments | Create Document Attachment |
| [**deleteDocumentAttachment**](DocumentAttachmentsApi.md#deleteDocumentAttachment) | **DELETE** /api/v1/documents/{document_id}/attachments/{attachment_id} | Delete Document Attachment |
| [**listDocumentAttachments**](DocumentAttachmentsApi.md#listDocumentAttachments) | **GET** /api/v1/documents/{document_id}/attachments | List Document Attachments |


<a id="createDocumentAttachment"></a>
# **createDocumentAttachment**
> InvoiceAttachmentResponse createDocumentAttachment(documentId, invoiceAttachmentCreateRequest)

Create Document Attachment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DocumentAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DocumentAttachmentsApi apiInstance = new DocumentAttachmentsApi(defaultClient);
    String documentId = "documentId_example"; // String | 
    InvoiceAttachmentCreateRequest invoiceAttachmentCreateRequest = new InvoiceAttachmentCreateRequest(); // InvoiceAttachmentCreateRequest | 
    try {
      InvoiceAttachmentResponse result = apiInstance.createDocumentAttachment(documentId, invoiceAttachmentCreateRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentAttachmentsApi#createDocumentAttachment");
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
| **documentId** | **String**|  | |
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

<a id="deleteDocumentAttachment"></a>
# **deleteDocumentAttachment**
> SimpleBoolResponse deleteDocumentAttachment(documentId, attachmentId)

Delete Document Attachment

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DocumentAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DocumentAttachmentsApi apiInstance = new DocumentAttachmentsApi(defaultClient);
    String documentId = "documentId_example"; // String | 
    String attachmentId = "attachmentId_example"; // String | 
    try {
      SimpleBoolResponse result = apiInstance.deleteDocumentAttachment(documentId, attachmentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentAttachmentsApi#deleteDocumentAttachment");
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
| **documentId** | **String**|  | |
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

<a id="listDocumentAttachments"></a>
# **listDocumentAttachments**
> InvoiceAttachmentsListResponse listDocumentAttachments(documentId)

List Document Attachments

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.DocumentAttachmentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    DocumentAttachmentsApi apiInstance = new DocumentAttachmentsApi(defaultClient);
    String documentId = "documentId_example"; // String | 
    try {
      InvoiceAttachmentsListResponse result = apiInstance.listDocumentAttachments(documentId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentAttachmentsApi#listDocumentAttachments");
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
| **documentId** | **String**|  | |

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

