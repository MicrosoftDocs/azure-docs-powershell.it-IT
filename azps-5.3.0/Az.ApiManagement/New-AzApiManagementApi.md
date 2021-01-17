---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 3312c725d63bcb42aab7d82144c5a8f6f8e67641
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478867"
---
# <span data-ttu-id="95dbd-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95dbd-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="95dbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="95dbd-102">SYNOPSIS</span></span>
<span data-ttu-id="95dbd-103">Crea un'API.</span><span class="sxs-lookup"><span data-stu-id="95dbd-103">Creates an API.</span></span>

## <span data-ttu-id="95dbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="95dbd-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-SubscriptionRequired]
 [-ApiVersionDescription <String>] [-ApiVersionSetId <String>] [-ApiVersion <String>] [-SourceApiId <String>]
 [-SourceApiRevision <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95dbd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95dbd-105">DESCRIPTION</span></span>
<span data-ttu-id="95dbd-106">Il cmdlet **New-AzApiManagementApi** crea un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="95dbd-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="95dbd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="95dbd-107">EXAMPLES</span></span>

### <span data-ttu-id="95dbd-108">Esempio 1: creare un'API</span><span class="sxs-lookup"><span data-stu-id="95dbd-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="95dbd-109">Questo comando crea un'API denominata EchoApi con l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="95dbd-109">This command creates an API named EchoApi with the specified URL.</span></span>

### <span data-ttu-id="95dbd-110">Esempio 2: creare un'API copiando tutte le operazioni, i tag, i prodotti e i criteri da Echo-API e in un ApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="95dbd-110">Example 2: Create an API by copying all operation, Tags, Products and Policies from echo-api and into an ApiVersionSet</span></span>
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

<span data-ttu-id="95dbd-111">Questo comando crea un'API `echoapiv3` in ApiVersionSet `xmsVersionSet` e copia tutte le operazioni, i tag e i criteri dall'API di origine `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="95dbd-111">This command creates an API `echoapiv3` in ApiVersionSet `xmsVersionSet` and copies all operation, Tags and Policies from source Api `echo-api`.</span></span> <span data-ttu-id="95dbd-112">Esegue l'override di SubscriptionRequired, ServiceUrl, Path, Protocols</span><span class="sxs-lookup"><span data-stu-id="95dbd-112">It overrides the SubscriptionRequired, ServiceUrl, Path, Protocols</span></span>

### <span data-ttu-id="95dbd-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="95dbd-113">Example 3</span></span>

<span data-ttu-id="95dbd-114">Crea un'API.</span><span class="sxs-lookup"><span data-stu-id="95dbd-114">Creates an API.</span></span> <span data-ttu-id="95dbd-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="95dbd-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzApiManagementApi -ApiId '0001' -Context <PsApiManagementContext> -Name 'Echo api' -Path 'echov3' -Protocols Http -ServiceUrl 'https://contoso.com/apis/echo'
```

## <span data-ttu-id="95dbd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="95dbd-116">PARAMETERS</span></span>

### <span data-ttu-id="95dbd-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="95dbd-117">-ApiId</span></span>
<span data-ttu-id="95dbd-118">Specifica l'ID dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="95dbd-118">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="95dbd-119">Se non specifichi questo parametro, questo cmdlet genera un ID per te.</span><span class="sxs-lookup"><span data-stu-id="95dbd-119">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="95dbd-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="95dbd-120">-ApiVersion</span></span>
<span data-ttu-id="95dbd-121">Versione API dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="95dbd-121">Api Version of the Api to create.</span></span> <span data-ttu-id="95dbd-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="95dbd-123">-ApiVersionDescription</span><span class="sxs-lookup"><span data-stu-id="95dbd-123">-ApiVersionDescription</span></span>
<span data-ttu-id="95dbd-124">Descrizione della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="95dbd-124">Api Version Description.</span></span> <span data-ttu-id="95dbd-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="95dbd-126">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="95dbd-126">-ApiVersionSetId</span></span>
<span data-ttu-id="95dbd-127">Un identificatore di risorsa per il set di versioni dell'API correlato.</span><span class="sxs-lookup"><span data-stu-id="95dbd-127">A resource identifier for the related Api Version Set.</span></span> <span data-ttu-id="95dbd-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="95dbd-129">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="95dbd-129">-AuthorizationScope</span></span>
<span data-ttu-id="95dbd-130">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="95dbd-130">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="95dbd-131">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-131">The default value is $Null.</span></span>

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

### <span data-ttu-id="95dbd-132">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="95dbd-132">-AuthorizationServerId</span></span>
<span data-ttu-id="95dbd-133">Specifica l'ID del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="95dbd-133">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="95dbd-134">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-134">The default value is $Null.</span></span>
<span data-ttu-id="95dbd-135">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="95dbd-135">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="95dbd-136">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="95dbd-136">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="95dbd-137">Meccanismo del server di autorizzazione OpenId tramite il quale il token di accesso viene passato all'API.</span><span class="sxs-lookup"><span data-stu-id="95dbd-137">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="95dbd-138">Fare riferimento a http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="95dbd-138">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="95dbd-139">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-139">This parameter is optional.</span></span> <span data-ttu-id="95dbd-140">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-140">Default value is $null.</span></span>

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

### <span data-ttu-id="95dbd-141">-Contesto</span><span class="sxs-lookup"><span data-stu-id="95dbd-141">-Context</span></span>
<span data-ttu-id="95dbd-142">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="95dbd-142">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="95dbd-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95dbd-143">-DefaultProfile</span></span>
<span data-ttu-id="95dbd-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="95dbd-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95dbd-145">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="95dbd-145">-Description</span></span>
<span data-ttu-id="95dbd-146">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="95dbd-146">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="95dbd-147">-Nome</span><span class="sxs-lookup"><span data-stu-id="95dbd-147">-Name</span></span>
<span data-ttu-id="95dbd-148">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="95dbd-148">Specifies the name of the web API.</span></span>
<span data-ttu-id="95dbd-149">Questo è il nome pubblico dell'API come viene visualizzato nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="95dbd-149">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="95dbd-150">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="95dbd-150">-OpenIdProviderId</span></span>
<span data-ttu-id="95dbd-151">Identificatore del server di autorizzazione OpenId.</span><span class="sxs-lookup"><span data-stu-id="95dbd-151">OpenId authorization server identifier.</span></span> <span data-ttu-id="95dbd-152">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-152">This parameter is optional.</span></span> <span data-ttu-id="95dbd-153">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-153">Default value is $null.</span></span> <span data-ttu-id="95dbd-154">Deve essere specificato se BearerTokenSendingMethods è specificato.</span><span class="sxs-lookup"><span data-stu-id="95dbd-154">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="95dbd-155">-Path</span><span class="sxs-lookup"><span data-stu-id="95dbd-155">-Path</span></span>
<span data-ttu-id="95dbd-156">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API e corrisponde al campo suffisso URL API Web nel portale di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="95dbd-156">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="95dbd-157">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="95dbd-157">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="95dbd-158">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-158">The default value is $Null.</span></span>

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

### <span data-ttu-id="95dbd-159">-ProductId</span><span class="sxs-lookup"><span data-stu-id="95dbd-159">-ProductIds</span></span>
<span data-ttu-id="95dbd-160">Specifica una matrice di ID prodotto a cui aggiungere la nuova API.</span><span class="sxs-lookup"><span data-stu-id="95dbd-160">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="95dbd-161">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="95dbd-161">-Protocols</span></span>
<span data-ttu-id="95dbd-162">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="95dbd-162">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="95dbd-163">I valori validi sono http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="95dbd-163">Valid values are http, https.</span></span>
<span data-ttu-id="95dbd-164">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="95dbd-164">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="95dbd-165">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-165">The default value is $Null.</span></span>

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

### <span data-ttu-id="95dbd-166">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="95dbd-166">-ServiceUrl</span></span>
<span data-ttu-id="95dbd-167">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="95dbd-167">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="95dbd-168">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="95dbd-168">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="95dbd-169">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="95dbd-169">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="95dbd-170">-SourceApiId</span><span class="sxs-lookup"><span data-stu-id="95dbd-170">-SourceApiId</span></span>
<span data-ttu-id="95dbd-171">Identificatore API dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="95dbd-171">Api identifier of the source API.</span></span> <span data-ttu-id="95dbd-172">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-172">This parameter is optional.</span></span>

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

### <span data-ttu-id="95dbd-173">-SourceApiRevision</span><span class="sxs-lookup"><span data-stu-id="95dbd-173">-SourceApiRevision</span></span>
<span data-ttu-id="95dbd-174">Revisione API dell'API di origine.</span><span class="sxs-lookup"><span data-stu-id="95dbd-174">Api Revision of the source API.</span></span> <span data-ttu-id="95dbd-175">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-175">This parameter is optional.</span></span>

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

### <span data-ttu-id="95dbd-176">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="95dbd-176">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="95dbd-177">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="95dbd-177">Specifies the subscription key header name.</span></span>
<span data-ttu-id="95dbd-178">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-178">The default value is $Null.</span></span>

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

### <span data-ttu-id="95dbd-179">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="95dbd-179">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="95dbd-180">Specifica il nome del parametro della stringa di query per la chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="95dbd-180">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="95dbd-181">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="95dbd-181">The default value is $Null.</span></span>

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

### <span data-ttu-id="95dbd-182">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="95dbd-182">-SubscriptionRequired</span></span>
<span data-ttu-id="95dbd-183">Flag per applicare SubscriptionRequired per le richieste all'API.</span><span class="sxs-lookup"><span data-stu-id="95dbd-183">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="95dbd-184">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="95dbd-184">This parameter is optional.</span></span>

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

### <span data-ttu-id="95dbd-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95dbd-185">CommonParameters</span></span>
<span data-ttu-id="95dbd-186">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95dbd-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95dbd-187">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95dbd-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95dbd-188">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="95dbd-188">INPUTS</span></span>

### <span data-ttu-id="95dbd-189">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="95dbd-189">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="95dbd-190">System. String</span><span class="sxs-lookup"><span data-stu-id="95dbd-190">System.String</span></span>

### <span data-ttu-id="95dbd-191">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="95dbd-191">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="95dbd-192">System. String []</span><span class="sxs-lookup"><span data-stu-id="95dbd-192">System.String[]</span></span>

## <span data-ttu-id="95dbd-193">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="95dbd-193">OUTPUTS</span></span>

### <span data-ttu-id="95dbd-194">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95dbd-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="95dbd-195">Note</span><span class="sxs-lookup"><span data-stu-id="95dbd-195">NOTES</span></span>

## <span data-ttu-id="95dbd-196">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="95dbd-196">RELATED LINKS</span></span>

[<span data-ttu-id="95dbd-197">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95dbd-197">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="95dbd-198">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95dbd-198">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="95dbd-199">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95dbd-199">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="95dbd-200">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95dbd-200">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="95dbd-201">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="95dbd-201">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


