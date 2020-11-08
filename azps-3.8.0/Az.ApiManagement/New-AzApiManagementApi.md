---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: c9c0ab0ed8b932892f2bea27ff811197b808b86b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022958"
---
# <span data-ttu-id="da5aa-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da5aa-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="da5aa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="da5aa-103">Crea un'API.</span><span class="sxs-lookup"><span data-stu-id="da5aa-103">Creates an API.</span></span>

## <span data-ttu-id="da5aa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da5aa-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da5aa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da5aa-105">DESCRIPTION</span></span>
<span data-ttu-id="da5aa-106">Il cmdlet **New-AzApiManagementApi** crea un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="da5aa-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="da5aa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da5aa-107">EXAMPLES</span></span>

### <span data-ttu-id="da5aa-108">Esempio 1: creare un'API</span><span class="sxs-lookup"><span data-stu-id="da5aa-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="da5aa-109">Questo comando crea un'API denominata EchoApi con l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="da5aa-110">Esempio 1: creare un'API copiando tutte le operazioni, i tag, i prodotti e i criteri da Echo-API e in un ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="da5aa-110">Example 1: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
```powershell
PS D:\github\azure-powershell>$context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso
PS D:\github\azure-powershell>$versionSet = Get-AzApiManagementApiVersionSet -Context $context -ApiVersionSetId "xmsVersionSet"
PS D:\github\azure-powershell> New-AzApiManagementApi -Context $context -Name "echoapiv4" -Description "Create Echo Api V4" -SubscriptionRequired -ServiceUrl "https://echoapi.cloudapp.net/v4" -Path "echov3" -Protocols @("http", "https") -ApiVersionSetId $versionSet.ApiVersionSetId -SourceApiId "echo-api" -ApiVersion "v4"


ApiId                         : 691b7d410125414a929c108541c60e06
Name                          : echoapiv4
Description                   : Create Echo Api V4
ServiceUrl                    : https://echoapi.cloudapp.net/v4 
Path                          : echov3
ApiType                       : http
Protocols                     : {Http, Https}
AuthorizationServerId         :
AuthorizationScope            :
OpenidProviderId              :
BearerTokenSendingMethod      : {}
SubscriptionKeyHeaderName     : Ocp-Apim-Subscription-Key
SubscriptionKeyQueryParamName : subscription-key
ApiRevision                   : 1
ApiVersion                    : v4
IsCurrent                     : True
IsOnline                      : False
SubscriptionRequired          : True
ApiRevisionDescription        :
ApiVersionSetDescription      :
ApiVersionSetId               : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apiVersionSets/xmsVersionSet
Id                            : /subscriptions/subid/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/apis/691b7d410125414a929c108541c60e06    
ResourceGroupName             : Api-Default-West-US
ServiceName                   : contoso
```

<span data-ttu-id="da5aa-111">Questo comando crea un'API `echoapiv3` in ApiVersionSet `xmsVersionSet` e copia tutte le operazioni, i tag e i criteri dall'API di origine `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="da5aa-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="da5aa-112">Esegue l'override di SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="da5aa-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

## <span data-ttu-id="da5aa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da5aa-113">PARAMETERS</span></span>

### <span data-ttu-id="da5aa-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="da5aa-114">-ApiId</span></span>
<span data-ttu-id="da5aa-115">Specifica l'ID dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="da5aa-115">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="da5aa-116">Se non specifichi questo parametro, questo cmdlet genera un ID per te.</span><span class="sxs-lookup"><span data-stu-id="da5aa-116">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="da5aa-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="da5aa-117">-ApiVersion</span></span>
<span data-ttu-id="da5aa-118">Versione API dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="da5aa-118">Api Version of the Api to create.</span></span> <span data-ttu-id="da5aa-119">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="da5aa-120">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="da5aa-120">-ApiVersionDescription</span></span>
<span data-ttu-id="da5aa-121">Descrizione della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="da5aa-121">Api Version Description.</span></span> <span data-ttu-id="da5aa-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="da5aa-123">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="da5aa-123">-ApiVersionSetId</span></span>
<span data-ttu-id="da5aa-124">Un identificatore di risorsa per il set di versioni dell'API correlato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-124">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="da5aa-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="da5aa-126">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="da5aa-126">-AuthorizationScope</span></span>
<span data-ttu-id="da5aa-127">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="da5aa-127">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="da5aa-128">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-128">The default value is $Null.</span></span>

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

### <span data-ttu-id="da5aa-129">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="da5aa-129">-AuthorizationServerId</span></span>
<span data-ttu-id="da5aa-130">Specifica l'ID del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="da5aa-130">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="da5aa-131">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-131">The default value is $Null.</span></span>
<span data-ttu-id="da5aa-132">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-132">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="da5aa-133">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="da5aa-133">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="da5aa-134">Meccanismo del server di autorizzazione OpenId tramite il quale il token di accesso viene passato all'API.</span><span class="sxs-lookup"><span data-stu-id="da5aa-134">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="da5aa-135">Fare riferimento a http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="da5aa-135">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="da5aa-136">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-136">This parameter is optional.</span></span> <span data-ttu-id="da5aa-137">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-137">Default value is $null.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5aa-138">-Contesto</span><span class="sxs-lookup"><span data-stu-id="da5aa-138">-Context</span></span>
<span data-ttu-id="da5aa-139">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="da5aa-139">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="da5aa-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da5aa-140">-DefaultProfile</span></span>
<span data-ttu-id="da5aa-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da5aa-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da5aa-142">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="da5aa-142">-Description</span></span>
<span data-ttu-id="da5aa-143">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="da5aa-143">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="da5aa-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="da5aa-144">-Name</span></span>
<span data-ttu-id="da5aa-145">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="da5aa-145">Specifies the name of the web API.</span></span>
<span data-ttu-id="da5aa-146">Questo è il nome pubblico dell'API come viene visualizzato nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="da5aa-146">This is the public name of the API as it appears on the developer and admin portals.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5aa-147">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="da5aa-147">-OpenIdProviderId</span></span>
<span data-ttu-id="da5aa-148">Identificatore del server di autorizzazione OpenId.</span><span class="sxs-lookup"><span data-stu-id="da5aa-148">OpenId authorization server identifier.</span></span> <span data-ttu-id="da5aa-149">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-149">This parameter is optional.</span></span> <span data-ttu-id="da5aa-150">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-150">Default value is $null.</span></span> <span data-ttu-id="da5aa-151">Deve essere specificato se BearerTokenSendingMethods è specificato.</span><span class="sxs-lookup"><span data-stu-id="da5aa-151">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="da5aa-152">-Path</span><span class="sxs-lookup"><span data-stu-id="da5aa-152">-Path</span></span>
<span data-ttu-id="da5aa-153">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API e corrisponde al campo suffisso URL API Web nel portale di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="da5aa-153">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="da5aa-154">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="da5aa-154">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="da5aa-155">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-155">The default value is $Null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5aa-156">-ProductId</span><span class="sxs-lookup"><span data-stu-id="da5aa-156">-ProductIds</span></span>
<span data-ttu-id="da5aa-157">Specifica una matrice di ID prodotto a cui aggiungere la nuova API.</span><span class="sxs-lookup"><span data-stu-id="da5aa-157">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5aa-158">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="da5aa-158">-Protocols</span></span>
<span data-ttu-id="da5aa-159">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="da5aa-159">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="da5aa-160">I valori validi sono http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="da5aa-160">Valid values are http, https.</span></span>
<span data-ttu-id="da5aa-161">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="da5aa-161">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="da5aa-162">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-162">The default value is $Null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5aa-163">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="da5aa-163">-ServiceUrl</span></span>
<span data-ttu-id="da5aa-164">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="da5aa-164">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="da5aa-165">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="da5aa-165">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="da5aa-166">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="da5aa-166">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5aa-167">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="da5aa-167">-SourceApiId</span></span>
<span data-ttu-id="da5aa-168">Identificatore API dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="da5aa-168">Api identifier of the source API.</span></span> <span data-ttu-id="da5aa-169">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="da5aa-170">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="da5aa-170">-SourceApiRevision</span></span>
<span data-ttu-id="da5aa-171">Revisione API dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="da5aa-171">Api Revision of the source API.</span></span> <span data-ttu-id="da5aa-172">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="da5aa-173">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="da5aa-173">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="da5aa-174">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="da5aa-174">Specifies the subscription key header name.</span></span>
<span data-ttu-id="da5aa-175">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-175">The default value is $Null.</span></span>

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

### <span data-ttu-id="da5aa-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="da5aa-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="da5aa-177">Specifica il nome del parametro della stringa di query per la chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="da5aa-177">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="da5aa-178">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="da5aa-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="da5aa-179">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="da5aa-179">-SubscriptionRequired</span></span>
<span data-ttu-id="da5aa-180">Flag per applicare SubscriptionRequired per le richieste all'API.</span><span class="sxs-lookup"><span data-stu-id="da5aa-180">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="da5aa-181">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="da5aa-181">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da5aa-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da5aa-182">CommonParameters</span></span>
<span data-ttu-id="da5aa-183">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da5aa-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da5aa-184">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da5aa-184">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da5aa-185">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da5aa-185">INPUTS</span></span>

### <span data-ttu-id="da5aa-186">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da5aa-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da5aa-187">System. String</span><span class="sxs-lookup"><span data-stu-id="da5aa-187">System.String</span></span>

### <span data-ttu-id="da5aa-188">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="da5aa-188">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="da5aa-189">System. String []</span><span class="sxs-lookup"><span data-stu-id="da5aa-189">System.String[]</span></span>

## <span data-ttu-id="da5aa-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da5aa-190">OUTPUTS</span></span>

### <span data-ttu-id="da5aa-191">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da5aa-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="da5aa-192">Note</span><span class="sxs-lookup"><span data-stu-id="da5aa-192">NOTES</span></span>

## <span data-ttu-id="da5aa-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da5aa-193">RELATED LINKS</span></span>

[<span data-ttu-id="da5aa-194">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da5aa-194">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="da5aa-195">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da5aa-195">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="da5aa-196">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da5aa-196">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="da5aa-197">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da5aa-197">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="da5aa-198">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="da5aa-198">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


