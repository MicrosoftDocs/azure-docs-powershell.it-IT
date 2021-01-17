---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 48C143BE-3BF6-43E3-99B0-1A1D12A0A3F3
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/import-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Import-AzApiManagementApi.md
ms.openlocfilehash: 5a9141cf0f609eedd35c25f6fd3d7977201e58c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478880"
---
# <span data-ttu-id="84bbc-101">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84bbc-101">Import-AzApiManagementApi</span></span>

## <span data-ttu-id="84bbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="84bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="84bbc-103">Importa un'API da un file o da un URL.</span><span class="sxs-lookup"><span data-stu-id="84bbc-103">Imports an API from a file or a URL.</span></span>

## <span data-ttu-id="84bbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84bbc-104">SYNTAX</span></span>

### <span data-ttu-id="84bbc-105">ImportFromLocalFile (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="84bbc-105">ImportFromLocalFile (Default)</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationPath <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84bbc-106">ImportFromUrl</span><span class="sxs-lookup"><span data-stu-id="84bbc-106">ImportFromUrl</span></span>
```
Import-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SpecificationUrl <String> [-Path <String>]
 [-WsdlServiceName <String>] [-WsdlEndpointName <String>] [-ApiType <PsApiManagementApiType>]
 [-Protocol <PsApiManagementSchema[]>] [-ServiceUrl <String>] [-ApiVersionSetId <String>]
 [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84bbc-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="84bbc-108">Il cmdlet **Import-AzApiManagementApi** importa un'API di gestione delle API di Azure da un file o un URL nel linguaggio Wadl (Web Application Description Language), WSDL (Web Services Description Language) o in formato spavalderia.</span><span class="sxs-lookup"><span data-stu-id="84bbc-108">The **Import-AzApiManagementApi** cmdlet imports an Azure API Management API from a file or a URL in Web Application Description Language (WADL), Web Services Description Language (WSDL), or Swagger format.</span></span>

## <span data-ttu-id="84bbc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="84bbc-110">Esempio 1: importare un'API da un file WADL</span><span class="sxs-lookup"><span data-stu-id="84bbc-110">Example 1: Import an API from a WADL file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationPath "C:\contoso\specifications\echoapi.wadl" -Path "apis"
```

<span data-ttu-id="84bbc-111">Questo comando importa un'API dal file WADL specificato.</span><span class="sxs-lookup"><span data-stu-id="84bbc-111">This command imports an API from the specified WADL file.</span></span>

### <span data-ttu-id="84bbc-112">Esempio 2: importare un'API da un file di spavalderia</span><span class="sxs-lookup"><span data-stu-id="84bbc-112">Example 2: Import an API from a Swagger file</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Swagger" -SpecificationPath "C:\contoso\specifications\echoapi.swagger" -Path "apis"
```

<span data-ttu-id="84bbc-113">Questo comando importa un'API dal file di spavalderia specificato.</span><span class="sxs-lookup"><span data-stu-id="84bbc-113">This command imports an API from the specified Swagger file.</span></span>

### <span data-ttu-id="84bbc-114">Esempio 3: importare un'API da un collegamento a WADL</span><span class="sxs-lookup"><span data-stu-id="84bbc-114">Example 3: Import an API from a WADL link</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Import-AzApiManagementApi -Context $ApiMgmtContext -SpecificationFormat "Wadl" -SpecificationUrl "http://contoso.com/specifications/wadl/echoapi" -Path "apis"
```

<span data-ttu-id="84bbc-115">Questo comando importa un'API dal collegamento WADL specificato.</span><span class="sxs-lookup"><span data-stu-id="84bbc-115">This command imports an API from the specified WADL link.</span></span>

### <span data-ttu-id="84bbc-116">Esempio 4: importare un'API da un collegamento API aperto</span><span class="sxs-lookup"><span data-stu-id="84bbc-116">Example 4: Import an API from a Open Api Link</span></span>
```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationFormat OpenApi -SpecificationUrl https://raw.githubusercontent.com/OAI/OpenAPI-Specification/master/examples/v3.0/petstore.yaml -Path "petstore30"

ApiId                         : af3f57bab399455aa875d7050654e9d1
Name                          : Swagger Petstore
Description                   :
ServiceUrl                    : http://petstore.swagger.io/v1
Path                          : petstore30
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    :
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               :
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/af3f57bab399455aa875d7050654e9d1     
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="84bbc-117">Questo comando importa un'API dal collegamento specifica di 3,0 aperto specificato.</span><span class="sxs-lookup"><span data-stu-id="84bbc-117">This command imports an API from the specified Open 3.0 specification link.</span></span>

### <span data-ttu-id="84bbc-118">Esempio 5: importare un'API da un collegamento API aperto in un set di ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84bbc-118">Example 5:  Import an API from a Open Api Link into a ApiVersion Set</span></span>

```powershell
PS C:\>$context = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Import-AzApiManagementApi -Context $context -SpecificationPath "C:\contoso\specifications\uspto.yml" -SpecificationFormat OpenApi -Path uspostal -ApiVersionSetId 0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd -ApiVersion v2

ApiId                         : 6c3f20c66e5745b19229d06cd865948f
Name                          : USPTO Data Set API
Description                   : The Data Set API (DSAPI) allows the public users to discover and search USPTO exported data sets. This is a generic API that allows USPTO users to make any CSV based data files
                                searchable through API. With the help of GET call, it returns the list of data fields that are searchable. With the help of POST call, data can be fetched based on the filters on the    
                                field names. Please note that POST call is used to search the actual data. The reason for the POST call is that it allows users to specify any complex search criteria without worry      
                                about the GET size limitations as well as encoding of the input parameters.
ServiceUrl                    : https://developer.uspto.gov/ds-api
Path                          : uspostal
ApiType                       : http
Protocols                     : {Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v2
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          :
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/0d50e2cf-aaeb-4ea3-8a58-db9ec079c6cd
Id                            : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis/6c3f20c66e5745b19229d06cd865948f    
ResourceGroupName             : Api-Default-East-US
ServiceName                   : contoso
```

<span data-ttu-id="84bbc-119">Questo comando importa un'API dal documento di specifica Open 3,0 specificato e crea un nuovo ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="84bbc-119">This command imports an API from the specified Open 3.0 specification document and create a new ApiVersion.</span></span>

## <span data-ttu-id="84bbc-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="84bbc-120">PARAMETERS</span></span>

### <span data-ttu-id="84bbc-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="84bbc-121">-ApiId</span></span>
<span data-ttu-id="84bbc-122">Specifica un ID per l'API da importare.</span><span class="sxs-lookup"><span data-stu-id="84bbc-122">Specifies an ID for the API to import.</span></span>
<span data-ttu-id="84bbc-123">Se non specifichi questo parametro, viene generato un ID.</span><span class="sxs-lookup"><span data-stu-id="84bbc-123">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="84bbc-124">-ApiRevision</span></span>
<span data-ttu-id="84bbc-125">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="84bbc-125">Identifier of API Revision.</span></span> <span data-ttu-id="84bbc-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84bbc-126">This parameter is optional.</span></span> <span data-ttu-id="84bbc-127">Se non specificato, l'importazione verrà eseguita nella revisione attualmente attiva o in una nuova API.</span><span class="sxs-lookup"><span data-stu-id="84bbc-127">If not specified, the import will be done onto the currently active revision or a new api.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-128">-ApiType</span><span class="sxs-lookup"><span data-stu-id="84bbc-128">-ApiType</span></span>
<span data-ttu-id="84bbc-129">Questo parametro è facoltativo con un valore predefinito di http.</span><span class="sxs-lookup"><span data-stu-id="84bbc-129">This parameter is optional with a default value of Http.</span></span> <span data-ttu-id="84bbc-130">L'opzione SOAP è applicabile solo quando si importano WSDL e si crea un'API passthrough SOAP.</span><span class="sxs-lookup"><span data-stu-id="84bbc-130">The Soap option is only applicable when importing WSDL and will create a SOAP Passthrough API.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="84bbc-131">-ApiVersion</span></span>
<span data-ttu-id="84bbc-132">Versione API dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="84bbc-132">Api Version of the Api to create.</span></span> <span data-ttu-id="84bbc-133">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84bbc-133">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-134">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="84bbc-134">-ApiVersionSetId</span></span>
<span data-ttu-id="84bbc-135">Un identificatore di risorsa per il set di versioni dell'API correlato.</span><span class="sxs-lookup"><span data-stu-id="84bbc-135">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="84bbc-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84bbc-136">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-137">-Contesto</span><span class="sxs-lookup"><span data-stu-id="84bbc-137">-Context</span></span>
<span data-ttu-id="84bbc-138">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="84bbc-138">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84bbc-139">-DefaultProfile</span></span>
<span data-ttu-id="84bbc-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="84bbc-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-141">-Path</span><span class="sxs-lookup"><span data-stu-id="84bbc-141">-Path</span></span>
<span data-ttu-id="84bbc-142">Specifica un percorso dell'API Web come ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="84bbc-142">Specifies a web API path as the last part of the API's public URL.</span></span>
<span data-ttu-id="84bbc-143">Questo URL viene usato dagli utenti dell'API per l'invio di richieste al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="84bbc-143">This URL is used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="84bbc-144">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="84bbc-144">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="84bbc-145">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="84bbc-145">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-146">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="84bbc-146">-Protocol</span></span>
<span data-ttu-id="84bbc-147">Protocolli API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="84bbc-147">Web API protocols (http, https).</span></span> <span data-ttu-id="84bbc-148">Protocolli su cui viene resa disponibile l'API.</span><span class="sxs-lookup"><span data-stu-id="84bbc-148">Protocols over which API is made available.</span></span> <span data-ttu-id="84bbc-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84bbc-149">This parameter is optional.</span></span> <span data-ttu-id="84bbc-150">Se specificato, eseguirà l'override dei protocolli specificati nel documento specifiche.</span><span class="sxs-lookup"><span data-stu-id="84bbc-150">If provided it will override the protocols specified in the specifications document.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-151">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="84bbc-151">-ServiceUrl</span></span>
<span data-ttu-id="84bbc-152">URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="84bbc-152">A URL of the web service exposing the API.</span></span> <span data-ttu-id="84bbc-153">Questo URL verrà usato solo dalla gestione delle API di Azure e non verrà reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="84bbc-153">This URL will be used by Azure API Management only, and will not be made public.</span></span> <span data-ttu-id="84bbc-154">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="84bbc-154">This parameter is optional.</span></span> <span data-ttu-id="84bbc-155">Se specificato, eseguirà l'override della ServiceUrl specificata nel documento specifiche.</span><span class="sxs-lookup"><span data-stu-id="84bbc-155">If provided it will override the ServiceUrl specified in the Specifications document.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-156">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="84bbc-156">-SpecificationFormat</span></span>
<span data-ttu-id="84bbc-157">Specifica il formato della specifica.</span><span class="sxs-lookup"><span data-stu-id="84bbc-157">Specifies the specification format.</span></span>
<span data-ttu-id="84bbc-158">psdx_paramvalues Wadl, WSDL e spavalderia.</span><span class="sxs-lookup"><span data-stu-id="84bbc-158">psdx_paramvalues Wadl, Wsdl, and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-159">-SpecificationPath</span><span class="sxs-lookup"><span data-stu-id="84bbc-159">-SpecificationPath</span></span>
<span data-ttu-id="84bbc-160">Specifica il percorso del file delle specifiche.</span><span class="sxs-lookup"><span data-stu-id="84bbc-160">Specifies the specification file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromLocalFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-161">-SpecificationUrl</span><span class="sxs-lookup"><span data-stu-id="84bbc-161">-SpecificationUrl</span></span>
<span data-ttu-id="84bbc-162">Specifica l'URL della specifica.</span><span class="sxs-lookup"><span data-stu-id="84bbc-162">Specifies the specification URL.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportFromUrl
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-163">-WsdlEndpointName</span><span class="sxs-lookup"><span data-stu-id="84bbc-163">-WsdlEndpointName</span></span>
<span data-ttu-id="84bbc-164">Nome locale dell'endpoint WSDL (porta) da importare.</span><span class="sxs-lookup"><span data-stu-id="84bbc-164">Local name of WSDL Endpoint (port) to be imported.</span></span> <span data-ttu-id="84bbc-165">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="84bbc-165">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="84bbc-166">Questo parametro è facoltativo e necessario solo per l'importazione di WSDL.</span><span class="sxs-lookup"><span data-stu-id="84bbc-166">This parameter is optional and only required for importing Wsdl.</span></span> <span data-ttu-id="84bbc-167">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="84bbc-167">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-168">-WsdlServiceName</span><span class="sxs-lookup"><span data-stu-id="84bbc-168">-WsdlServiceName</span></span>
<span data-ttu-id="84bbc-169">Nome locale del servizio WSDL da importare.</span><span class="sxs-lookup"><span data-stu-id="84bbc-169">Local name of WSDL Service to be imported.</span></span> <span data-ttu-id="84bbc-170">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="84bbc-170">Must be 1 to 400 characters long.</span></span> <span data-ttu-id="84bbc-171">Questo parametro è facoltativo e necessario solo per l'importazione di WSDL.</span><span class="sxs-lookup"><span data-stu-id="84bbc-171">This parameter is optional and only required for importing Wsdl .</span></span> <span data-ttu-id="84bbc-172">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="84bbc-172">Default value is $null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84bbc-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84bbc-173">CommonParameters</span></span>
<span data-ttu-id="84bbc-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84bbc-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84bbc-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84bbc-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84bbc-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="84bbc-176">INPUTS</span></span>

### <span data-ttu-id="84bbc-177">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="84bbc-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="84bbc-178">System. String</span><span class="sxs-lookup"><span data-stu-id="84bbc-178">System.String</span></span>

### <span data-ttu-id="84bbc-179">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="84bbc-179">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="84bbc-180">System. Nullable ' 1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiType, Microsoft. Azure. PowerShell. Cmdlets. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="84bbc-180">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="84bbc-181">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84bbc-181">OUTPUTS</span></span>

### <span data-ttu-id="84bbc-182">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84bbc-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="84bbc-183">Note</span><span class="sxs-lookup"><span data-stu-id="84bbc-183">NOTES</span></span>

## <span data-ttu-id="84bbc-184">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84bbc-184">RELATED LINKS</span></span>

[<span data-ttu-id="84bbc-185">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84bbc-185">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="84bbc-186">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84bbc-186">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="84bbc-187">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84bbc-187">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="84bbc-188">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84bbc-188">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="84bbc-189">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="84bbc-189">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


