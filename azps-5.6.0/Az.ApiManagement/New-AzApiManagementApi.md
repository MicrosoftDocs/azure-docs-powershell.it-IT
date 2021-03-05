---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 61c02917d5381753ec8fd9e4b7560f68722d5f19
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962526"
---
# <span data-ttu-id="fc140-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc140-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="fc140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc140-102">SYNOPSIS</span></span>
<span data-ttu-id="fc140-103">Crea un'API.</span><span class="sxs-lookup"><span data-stu-id="fc140-103">Creates an API.</span></span>

## <span data-ttu-id="fc140-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc140-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc140-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fc140-105">DESCRIPTION</span></span>
<span data-ttu-id="fc140-106">Il cmdlet **New-AzApiManagementApi** crea un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc140-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="fc140-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc140-107">EXAMPLES</span></span>

### <span data-ttu-id="fc140-108">Esempio 1: Creare un'API</span><span class="sxs-lookup"><span data-stu-id="fc140-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="fc140-109">Questo comando crea un'API denominata EchoApi con l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="fc140-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="fc140-110">Esempio 2: Creare un'API copiando tutte le operazioni, tag, prodotti e criteri da echo-api e in un apiVersionSet</span><span class="sxs-lookup"><span data-stu-id="fc140-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="fc140-111">Questo comando crea un'API `echoapiv3` in ApiVersionSet e copia tutte le `xmsVersionSet` operazioni, i tag e i criteri dall'Api di `echo-api` origine.</span><span class="sxs-lookup"><span data-stu-id="fc140-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="fc140-112">Sostituisce SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="fc140-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="fc140-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fc140-113">Example 3</span></span>

<span data-ttu-id="fc140-114">Crea un'API.</span><span class="sxs-lookup"><span data-stu-id="fc140-114">Creates an API.</span></span> <span data-ttu-id="fc140-115">(autogenerati)</span><span class="sxs-lookup"><span data-stu-id="fc140-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="fc140-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc140-116">PARAMETERS</span></span>

### <span data-ttu-id="fc140-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fc140-117">-ApiId</span></span>
<span data-ttu-id="fc140-118">Specifica l'ID dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="fc140-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="fc140-119">Se non si specifica questo parametro, questo cmdlet genera automaticamente un ID.</span><span class="sxs-lookup"><span data-stu-id="fc140-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="fc140-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fc140-120">-ApiVersion</span></span>
<span data-ttu-id="fc140-121">Versione API dell'Api da creare.</span><span class="sxs-lookup"><span data-stu-id="fc140-121">Api Version of the Api to create.</span></span> <span data-ttu-id="fc140-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc140-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="fc140-123">-ApiVersionDescription</span></span>
<span data-ttu-id="fc140-124">Descrizione della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="fc140-124">Api Version Description.</span></span> <span data-ttu-id="fc140-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc140-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="fc140-126">-ApiVersionSetId</span></span>
<span data-ttu-id="fc140-127">Identificatore di risorsa per il set di versioni dell'API correlato.</span><span class="sxs-lookup"><span data-stu-id="fc140-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="fc140-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc140-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="fc140-129">-AuthorizationScope</span></span>
<span data-ttu-id="fc140-130">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="fc140-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="fc140-131">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="fc140-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc140-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="fc140-132">-AuthorizationServerId</span></span>
<span data-ttu-id="fc140-133">Specifica l'ID server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="fc140-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="fc140-134">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="fc140-134">The default value is $Null.</span></span>
<span data-ttu-id="fc140-135">È necessario specificare questo parametro se *è specificato AuthorizationScope.*</span><span class="sxs-lookup"><span data-stu-id="fc140-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="fc140-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="fc140-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="fc140-137">Meccanismo del server di autorizzazione OpenId tramite il quale il token di accesso viene passato all'API.</span><span class="sxs-lookup"><span data-stu-id="fc140-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="fc140-138">Fare riferimento a http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="fc140-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="fc140-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-139">This parameter is optional.</span></span> <span data-ttu-id="fc140-140">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="fc140-140">Default value is $null.</span></span>

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

### <span data-ttu-id="fc140-141">-Context</span><span class="sxs-lookup"><span data-stu-id="fc140-141">-Context</span></span>
<span data-ttu-id="fc140-142">Specifica un **oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="fc140-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fc140-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc140-143">-DefaultProfile</span></span>
<span data-ttu-id="fc140-144">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc140-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc140-145">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc140-145">-Description</span></span>
<span data-ttu-id="fc140-146">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="fc140-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="fc140-147">-Name</span><span class="sxs-lookup"><span data-stu-id="fc140-147">-Name</span></span>
<span data-ttu-id="fc140-148">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="fc140-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="fc140-149">Nome pubblico dell'API così come viene visualizzata nei portali di sviluppo e amministrazione.</span><span class="sxs-lookup"><span data-stu-id="fc140-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="fc140-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="fc140-150">-OpenIdProviderId</span></span>
<span data-ttu-id="fc140-151">Identificatore del server di autorizzazione OpenId.</span><span class="sxs-lookup"><span data-stu-id="fc140-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="fc140-152">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-152">This parameter is optional.</span></span> <span data-ttu-id="fc140-153">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="fc140-153">Default value is $null.</span></span> <span data-ttu-id="fc140-154">Deve essere specificato se si specifica BearerTokenSendingMethods.</span><span class="sxs-lookup"><span data-stu-id="fc140-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="fc140-155">-Path</span><span class="sxs-lookup"><span data-stu-id="fc140-155">-Path</span></span>
<span data-ttu-id="fc140-156">Specifica il percorso dell'API Web, ovvero l'ultima parte dell'URL pubblico dell'API e corrisponde al campo del suffisso URL dell'API Web nel portale di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="fc140-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="fc140-157">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve contenere da uno a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="fc140-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="fc140-158">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="fc140-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc140-159">-ProductIds</span><span class="sxs-lookup"><span data-stu-id="fc140-159">-ProductIds</span></span>
<span data-ttu-id="fc140-160">Specifica una matrice di ID prodotto a cui aggiungere la nuova API.</span><span class="sxs-lookup"><span data-stu-id="fc140-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="fc140-161">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="fc140-161">-Protocols</span></span>
<span data-ttu-id="fc140-162">Specifica una matrice di protocolli web API.</span><span class="sxs-lookup"><span data-stu-id="fc140-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="fc140-163">I valori validi sono http, https.</span><span class="sxs-lookup"><span data-stu-id="fc140-163">Valid values are http, https.</span></span>
<span data-ttu-id="fc140-164">Si tratta dei protocolli Web su cui viene resa disponibile l'API.</span><span class="sxs-lookup"><span data-stu-id="fc140-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="fc140-165">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="fc140-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc140-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="fc140-166">-ServiceUrl</span></span>
<span data-ttu-id="fc140-167">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="fc140-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="fc140-168">Questo URL viene usato solo da Gestione API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="fc140-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="fc140-169">L'URL deve contenere da uno a 2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="fc140-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="fc140-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="fc140-170">-SourceApiId</span></span>
<span data-ttu-id="fc140-171">Identificatore API dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="fc140-171">Api identifier of the source API.</span></span> <span data-ttu-id="fc140-172">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc140-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="fc140-173">-SourceApiRevision</span></span>
<span data-ttu-id="fc140-174">Revisione api dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="fc140-174">Api Revision of the source API.</span></span> <span data-ttu-id="fc140-175">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc140-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="fc140-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="fc140-177">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fc140-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="fc140-178">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="fc140-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc140-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="fc140-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="fc140-180">Specifica il nome del parametro della stringa di query con chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fc140-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="fc140-181">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="fc140-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="fc140-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="fc140-182">-SubscriptionRequired</span></span>
<span data-ttu-id="fc140-183">Contrassegno per applicare SubscriptionRequired per le richieste all'Api.</span><span class="sxs-lookup"><span data-stu-id="fc140-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="fc140-184">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="fc140-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="fc140-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc140-185">CommonParameters</span></span>
<span data-ttu-id="fc140-186">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc140-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc140-187">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fc140-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc140-188">INPUT</span><span class="sxs-lookup"><span data-stu-id="fc140-188">INPUTS</span></span>

### <span data-ttu-id="fc140-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fc140-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fc140-190">System.String</span><span class="sxs-lookup"><span data-stu-id="fc140-190">System.String</span></span>

### <span data-ttu-id="fc140-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span><span class="sxs-lookup"><span data-stu-id="fc140-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="fc140-192">System.String[]</span><span class="sxs-lookup"><span data-stu-id="fc140-192">System.String[]</span></span>

## <span data-ttu-id="fc140-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc140-193">OUTPUTS</span></span>

### <span data-ttu-id="fc140-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc140-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="fc140-195">NOTE</span><span class="sxs-lookup"><span data-stu-id="fc140-195">NOTES</span></span>

## <span data-ttu-id="fc140-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc140-196">RELATED LINKS</span></span>

[<span data-ttu-id="fc140-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc140-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="fc140-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc140-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="fc140-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc140-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="fc140-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc140-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="fc140-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fc140-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


