# ComplianceApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**downloadDocumentXml**](ComplianceApi.md#downloadDocumentXml) | **GET** /api/v1/documents/{document_id}/xml | Download Document Xml |
| [**renderDocumentXml**](ComplianceApi.md#renderDocumentXml) | **POST** /api/v1/documents/xml | Render Document Xml |
| [**validateCompliance**](ComplianceApi.md#validateCompliance) | **POST** /api/v1/documents/validate-compliance | Validate Compliance |


<a id="downloadDocumentXml"></a>
# **downloadDocumentXml**
> String downloadDocumentXml(documentId, profile)

Download Document Xml

The e-invoicing XML for a document already stored here.  Reads &#x60;data_json&#x60; directly rather than going through the render path&#39;s reconstruction: the status, the logo and the source document&#39;s number are all attached there for the *PDF*, and none of them belong in the XML. The credit note&#39;s BG-3 reference is already in the stored payload, resolved when the document was written.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ComplianceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ComplianceApi apiInstance = new ComplianceApi(defaultClient);
    String documentId = "documentId_example"; // String | 
    String profile = "peppol_bis_billing_3"; // String | Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request.
    try {
      String result = apiInstance.downloadDocumentXml(documentId, profile);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ComplianceApi#downloadDocumentXml");
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
| **profile** | **String**| Which ruleset to write this against. No default: a document valid under one can be rejected by another, so the choice is the request. | |

### Return type

**String**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The stored document as XML, in the syntax the chosen profile is expressed in — UBL for Peppol BIS, CII for Factur-X. |  -  |
| **422** | Validation Error |  -  |

<a id="renderDocumentXml"></a>
# **renderDocumentXml**
> String renderDocumentXml(documentComplianceRequest)

Render Document Xml

The e-invoicing XML for a document, without storing anything.  Takes the same body as &#x60;/validate-compliance&#x60;, and the pairing is the point: check first, then take the XML once it passes. Nothing here validates against the ruleset — a document missing mandatory fields serialises to XML missing those elements, which is a more useful artefact to look at than a refusal, and &#x60;/validate-compliance&#x60; is where the refusal belongs.  The syntax is not a parameter. It follows from the profile, because a profile already is a syntax plus a ruleset, and asking a caller for both is asking them to know that Peppol means UBL.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ComplianceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ComplianceApi apiInstance = new ComplianceApi(defaultClient);
    DocumentComplianceRequest documentComplianceRequest = new DocumentComplianceRequest(); // DocumentComplianceRequest | 
    try {
      String result = apiInstance.renderDocumentXml(documentComplianceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ComplianceApi#renderDocumentXml");
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
| **documentComplianceRequest** | [**DocumentComplianceRequest**](DocumentComplianceRequest.md)|  | |

### Return type

**String**

### Authorization

[HTTPBearer](../README.md#HTTPBearer)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/xml, application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The document as XML, in the syntax the chosen profile is expressed in — UBL for Peppol BIS, CII for Factur-X. |  -  |
| **422** | Validation Error |  -  |

<a id="validateCompliance"></a>
# **validateCompliance**
> DocumentComplianceResponse validateCompliance(documentComplianceRequest)

Validate Compliance

Check a document against an e-invoicing ruleset without rendering it.  Costs no renders: nothing is stored and no PDF is produced, so a caller can check every invoice they are about to send rather than discovering the problem from a rejection weeks later.  Two tiers run, and both are reported. The mandatory-field check names a field of the request you can go and change. Schematron then serializes the document and runs the **published rules at a pinned version** over the result — the same artefacts an access point runs — so a finding here quotes the rule id a rejection notice would quote.  Read &#x60;valid&#x60; together with &#x60;fully_checked&#x60;: &#x60;valid&#x60; says nothing fatal was found, and &#x60;rulesets&#x60; says what actually ran to find it.

### Example
```java
// Import classes:
import com.invoicepdfs.ApiClient;
import com.invoicepdfs.ApiException;
import com.invoicepdfs.Configuration;
import com.invoicepdfs.auth.*;
import com.invoicepdfs.models.*;
import org.openapitools.client.api.ComplianceApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: HTTPBearer
    HttpBearerAuth HTTPBearer = (HttpBearerAuth) defaultClient.getAuthentication("HTTPBearer");
    HTTPBearer.setBearerToken("BEARER TOKEN");

    ComplianceApi apiInstance = new ComplianceApi(defaultClient);
    DocumentComplianceRequest documentComplianceRequest = new DocumentComplianceRequest(); // DocumentComplianceRequest | 
    try {
      DocumentComplianceResponse result = apiInstance.validateCompliance(documentComplianceRequest);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ComplianceApi#validateCompliance");
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
| **documentComplianceRequest** | [**DocumentComplianceRequest**](DocumentComplianceRequest.md)|  | |

### Return type

[**DocumentComplianceResponse**](DocumentComplianceResponse.md)

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

