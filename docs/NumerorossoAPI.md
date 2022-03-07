# NumerorossoAPI

All URIs are relative to *http://localhost:8080/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**aggiornaStatoLetturaRisposta**](NumerorossoAPI.md#aggiornastatoletturarisposta) | **PATCH** /istanze/{idIstanza}/risposta/{idRisposta} | Aggiornamento stato risposta numero rosso
[**getCountRisposteNonLette**](NumerorossoAPI.md#getcountrispostenonlette) | **GET** /istanze/count | Recupera il numero di istanze con risposte non lette
[**getIstanzaById**](NumerorossoAPI.md#getistanzabyid) | **GET** /istanze/{idIstanza} | Ricerca un istanza per id
[**getListIstanzeNumeroRosso**](NumerorossoAPI.md#getlististanzenumerorosso) | **GET** /istanze | Recupera tutte le istanze numero rosso


# **aggiornaStatoLetturaRisposta**
```swift
    open class func aggiornaStatoLetturaRisposta(idIstanza: String, idRisposta: String, notificaLettura: NotificaLettura, completion: @escaping (_ data: IstanzeReadResponse?, _ error: Error?) -> Void)
```

Aggiornamento stato risposta numero rosso

Aggiorna lo stato della risposta relativa all'istanza numero rosso

### Example 
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let idIstanza = "idIstanza_example" // String | id istanza
let idRisposta = "idRisposta_example" // String | id risposta
let notificaLettura = NotificaLettura(letto: false) // NotificaLettura | informazione sullo stato da assegnare alla risposta

// Aggiornamento stato risposta numero rosso
NumerorossoAPI.aggiornaStatoLetturaRisposta(idIstanza: idIstanza, idRisposta: idRisposta, notificaLettura: notificaLettura) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **idIstanza** | **String** | id istanza | 
 **idRisposta** | **String** | id risposta | 
 **notificaLettura** | [**NotificaLettura**](NotificaLettura.md) | informazione sullo stato da assegnare alla risposta | 

### Return type

[**IstanzeReadResponse**](IstanzeReadResponse.md)

### Authorization

[OHS](../README.md#OHS), [OSB](../README.md#OSB)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/hal+json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getCountRisposteNonLette**
```swift
    open class func getCountRisposteNonLette(X_CLIENT_ID: String, X_EXTERNAL_JWT: String? = nil, X_CORRELATION_ID: String? = nil, unreadOnly: Bool? = nil, completion: @escaping (_ data: IstanzeCountResponse?, _ error: Error?) -> Void)
```

Recupera il numero di istanze con risposte non lette

Recupera il numero totale di risposte non lette per tutte le istanze numero rosso

### Example 
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let X_CLIENT_ID = "X_CLIENT_ID_example" // String | Identificativo del chiamante
let X_EXTERNAL_JWT = "X_EXTERNAL_JWT_example" // String | rappresenta il token applicativo nel quale gestire eventuali informazioni di contesto e sessione (optional)
let X_CORRELATION_ID = "X_CORRELATION_ID_example" // String | identificativo richiesta, utilizzato per correlare tra loro una sequenza di eventi o azioni attivate da una singola richiesta web (optional)
let unreadOnly = true // Bool | booleano, se true restituisce solo il numero delle istanze che presentano risposte non lette (optional)

// Recupera il numero di istanze con risposte non lette
NumerorossoAPI.getCountRisposteNonLette(X_CLIENT_ID: X_CLIENT_ID, X_EXTERNAL_JWT: X_EXTERNAL_JWT, X_CORRELATION_ID: X_CORRELATION_ID, unreadOnly: unreadOnly) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X_CLIENT_ID** | **String** | Identificativo del chiamante | 
 **X_EXTERNAL_JWT** | **String** | rappresenta il token applicativo nel quale gestire eventuali informazioni di contesto e sessione | [optional] 
 **X_CORRELATION_ID** | **String** | identificativo richiesta, utilizzato per correlare tra loro una sequenza di eventi o azioni attivate da una singola richiesta web | [optional] 
 **unreadOnly** | **Bool** | booleano, se true restituisce solo il numero delle istanze che presentano risposte non lette | [optional] 

### Return type

[**IstanzeCountResponse**](IstanzeCountResponse.md)

### Authorization

[OHS](../README.md#OHS), [OSB](../README.md#OSB)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/hal+json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getIstanzaById**
```swift
    open class func getIstanzaById(X_CLIENT_ID: String, idIstanza: String, X_EXTERNAL_JWT: String? = nil, X_CORRELATION_ID: String? = nil, completion: @escaping (_ data: IstanzaResponse?, _ error: Error?) -> Void)
```

Ricerca un istanza per id

Ritorna una singola istanza numero rosso a partire da un id

### Example 
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let X_CLIENT_ID = "X_CLIENT_ID_example" // String | Identificativo del chiamante
let idIstanza = "idIstanza_example" // String | Id dell'istanza numero rosso da ritornare
let X_EXTERNAL_JWT = "X_EXTERNAL_JWT_example" // String | rappresenta il token applicativo nel quale gestire eventuali informazioni di contesto e sessione (optional)
let X_CORRELATION_ID = "X_CORRELATION_ID_example" // String | identificativo richiesta, utilizzato per correlare tra loro una sequenza di eventi o azioni attivate da una singola richiesta web (optional)

// Ricerca un istanza per id
NumerorossoAPI.getIstanzaById(X_CLIENT_ID: X_CLIENT_ID, idIstanza: idIstanza, X_EXTERNAL_JWT: X_EXTERNAL_JWT, X_CORRELATION_ID: X_CORRELATION_ID) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X_CLIENT_ID** | **String** | Identificativo del chiamante | 
 **idIstanza** | **String** | Id dell&#39;istanza numero rosso da ritornare | 
 **X_EXTERNAL_JWT** | **String** | rappresenta il token applicativo nel quale gestire eventuali informazioni di contesto e sessione | [optional] 
 **X_CORRELATION_ID** | **String** | identificativo richiesta, utilizzato per correlare tra loro una sequenza di eventi o azioni attivate da una singola richiesta web | [optional] 

### Return type

[**IstanzaResponse**](IstanzaResponse.md)

### Authorization

[OHS](../README.md#OHS), [OSB](../README.md#OSB)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/hal+json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **getListIstanzeNumeroRosso**
```swift
    open class func getListIstanzeNumeroRosso(X_CLIENT_ID: String, X_EXTERNAL_JWT: String? = nil, X_CORRELATION_ID: String? = nil, X_FULL: Bool? = nil, testPar: String? = nil, completion: @escaping (_ data: IstanzeListResponse?, _ error: Error?) -> Void)
```

Recupera tutte le istanze numero rosso

Ritorna la lista delle istanze numero rosso

### Example 
```swift
// The following code samples are still beta. For any issue, please report via http://github.com/OpenAPITools/openapi-generator/issues/new
import OpenAPIClient

let X_CLIENT_ID = "X_CLIENT_ID_example" // String | Identificativo del chiamante
let X_EXTERNAL_JWT = "X_EXTERNAL_JWT_example" // String | rappresenta il token applicativo nel quale gestire eventuali informazioni di contesto e sessione (optional)
let X_CORRELATION_ID = "X_CORRELATION_ID_example" // String | identificativo richiesta, utilizzato per correlare tra loro una sequenza di eventi o azioni attivate da una singola richiesta web (optional)
let X_FULL = true // Bool | indica se restituire tutta la risposta o solo una parte (optional)
let testPar = "testPar_example" // String | booleano, se true restituisce solo il numero delle istanze che presentano risposte non lette (optional)

// Recupera tutte le istanze numero rosso
NumerorossoAPI.getListIstanzeNumeroRosso(X_CLIENT_ID: X_CLIENT_ID, X_EXTERNAL_JWT: X_EXTERNAL_JWT, X_CORRELATION_ID: X_CORRELATION_ID, X_FULL: X_FULL, testPar: testPar) { (response, error) in
    guard error == nil else {
        print(error)
        return
    }

    if (response) {
        dump(response)
    }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **X_CLIENT_ID** | **String** | Identificativo del chiamante | 
 **X_EXTERNAL_JWT** | **String** | rappresenta il token applicativo nel quale gestire eventuali informazioni di contesto e sessione | [optional] 
 **X_CORRELATION_ID** | **String** | identificativo richiesta, utilizzato per correlare tra loro una sequenza di eventi o azioni attivate da una singola richiesta web | [optional] 
 **X_FULL** | **Bool** | indica se restituire tutta la risposta o solo una parte | [optional] 
 **testPar** | **String** | booleano, se true restituisce solo il numero delle istanze che presentano risposte non lette | [optional] 

### Return type

[**IstanzeListResponse**](IstanzeListResponse.md)

### Authorization

[OHS](../README.md#OHS), [OSB](../README.md#OSB)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/hal+json, application/problem+json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

