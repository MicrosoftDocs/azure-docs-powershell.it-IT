---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310980"
---
# <span data-ttu-id="5f9cf-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5f9cf-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="5f9cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f9cf-102">SYNOPSIS</span></span>
<span data-ttu-id="5f9cf-103">Modifica di una revisione API</span><span class="sxs-lookup"><span data-stu-id="5f9cf-103">Modifies an API Revision</span></span>

## <span data-ttu-id="5f9cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f9cf-104">SYNTAX</span></span>

### <span data-ttu-id="5f9cf-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f9cf-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f9cf-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5f9cf-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f9cf-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f9cf-107">DESCRIPTION</span></span>
<span data-ttu-id="5f9cf-108">Il cmdlet **set-AzApiManagementApiRevision** modifica una revisione API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="5f9cf-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f9cf-109">EXAMPLES</span></span>

### <span data-ttu-id="5f9cf-110">Esempio 1: modificare una revisione delle API</span><span class="sxs-lookup"><span data-stu-id="5f9cf-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="5f9cf-111">Il cmdlet aggiorna la `2` revisione dell'API `echo-api` con una nuova descrizione, un protocollo e un percorso.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="5f9cf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f9cf-112">PARAMETERS</span></span>

### <span data-ttu-id="5f9cf-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5f9cf-113">-ApiId</span></span>
<span data-ttu-id="5f9cf-114">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-114">Identifier of existing API.</span></span>
<span data-ttu-id="5f9cf-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9cf-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="5f9cf-116">-ApiRevision</span></span>
<span data-ttu-id="5f9cf-117">Identificatore della revisione API esistente.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="5f9cf-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9cf-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="5f9cf-119">-AuthorizationScope</span></span>
<span data-ttu-id="5f9cf-120">Ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-120">OAuth operations scope.</span></span>
<span data-ttu-id="5f9cf-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-121">This parameter is optional.</span></span>
<span data-ttu-id="5f9cf-122">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-122">Default value is $null.</span></span>

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

### <span data-ttu-id="5f9cf-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="5f9cf-123">-AuthorizationServerId</span></span>
<span data-ttu-id="5f9cf-124">Identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="5f9cf-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-125">This parameter is optional.</span></span>
<span data-ttu-id="5f9cf-126">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-126">Default value is $null.</span></span>
<span data-ttu-id="5f9cf-127">Deve essere specificato se AuthorizationScope specificato.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="5f9cf-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="5f9cf-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="5f9cf-129">Meccanismo del server di autorizzazione OpenId tramite il quale il token di accesso viene passato all'API.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="5f9cf-130">Fare riferimento a http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="5f9cf-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="5f9cf-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-131">This parameter is optional.</span></span> <span data-ttu-id="5f9cf-132">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-132">Default value is $null.</span></span>

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

### <span data-ttu-id="5f9cf-133">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5f9cf-133">-Context</span></span>
<span data-ttu-id="5f9cf-134">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5f9cf-135">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-135">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9cf-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f9cf-136">-DefaultProfile</span></span>
<span data-ttu-id="5f9cf-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5f9cf-138">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f9cf-138">-Description</span></span>
<span data-ttu-id="5f9cf-139">Descrizione dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-139">Web API description.</span></span>
<span data-ttu-id="5f9cf-140">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f9cf-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5f9cf-141">-InputObject</span></span>
<span data-ttu-id="5f9cf-142">Istanza di PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="5f9cf-143">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-143">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f9cf-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f9cf-144">-Name</span></span>
<span data-ttu-id="5f9cf-145">Nome API Web.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-145">Web API name.</span></span>
<span data-ttu-id="5f9cf-146">Nome pubblico dell'API come comparirebbe nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="5f9cf-147">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-147">This parameter is required.</span></span>

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

### <span data-ttu-id="5f9cf-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="5f9cf-148">-OpenIdProviderId</span></span>
<span data-ttu-id="5f9cf-149">Identificatore del server di autorizzazione OpenId.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="5f9cf-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-150">This parameter is optional.</span></span> <span data-ttu-id="5f9cf-151">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-151">Default value is $null.</span></span> <span data-ttu-id="5f9cf-152">Deve essere specificato se BearerTokenSendingMethods è specificato.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="5f9cf-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5f9cf-153">-PassThru</span></span>
<span data-ttu-id="5f9cf-154">Se specificato, l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi che rappresenta l'API set.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="5f9cf-155">-Path</span><span class="sxs-lookup"><span data-stu-id="5f9cf-155">-Path</span></span>
<span data-ttu-id="5f9cf-156">Percorso API Web.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-156">Web API Path.</span></span>
<span data-ttu-id="5f9cf-157">Ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="5f9cf-158">Questo URL verrà usato dagli utenti dell'API per l'invio di richieste al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="5f9cf-159">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="5f9cf-160">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-160">This parameter is optional.</span></span>
<span data-ttu-id="5f9cf-161">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-161">Default value is $null.</span></span>

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

### <span data-ttu-id="5f9cf-162">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="5f9cf-162">-Protocols</span></span>
<span data-ttu-id="5f9cf-163">Protocolli API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="5f9cf-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="5f9cf-164">Protocolli su cui viene resa disponibile l'API.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="5f9cf-165">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-165">This parameter is required.</span></span>
<span data-ttu-id="5f9cf-166">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-166">Default value is $null.</span></span>

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

### <span data-ttu-id="5f9cf-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="5f9cf-167">-ServiceUrl</span></span>
<span data-ttu-id="5f9cf-168">URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="5f9cf-169">Questo URL verrà usato solo dalla gestione delle API di Azure e non verrà reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="5f9cf-170">Deve essere lunga da 1 a 2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="5f9cf-171">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-171">This parameter is required.</span></span>

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

### <span data-ttu-id="5f9cf-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="5f9cf-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="5f9cf-173">Nome intestazione chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-173">Subscription key header name.</span></span>
<span data-ttu-id="5f9cf-174">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-174">This parameter is optional.</span></span>
<span data-ttu-id="5f9cf-175">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-175">Default value is $null.</span></span>

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

### <span data-ttu-id="5f9cf-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="5f9cf-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="5f9cf-177">Nome parametro stringa query chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="5f9cf-178">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-178">This parameter is optional.</span></span>
<span data-ttu-id="5f9cf-179">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-179">Default value is $null.</span></span>

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

### <span data-ttu-id="5f9cf-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="5f9cf-180">-SubscriptionRequired</span></span>
<span data-ttu-id="5f9cf-181">Flag per applicare SubscriptionRequired per le richieste all'API.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="5f9cf-182">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="5f9cf-183">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f9cf-183">-Confirm</span></span>
<span data-ttu-id="5f9cf-184">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9cf-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f9cf-185">-WhatIf</span></span>
<span data-ttu-id="5f9cf-186">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f9cf-187">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f9cf-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f9cf-188">CommonParameters</span></span>
<span data-ttu-id="5f9cf-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f9cf-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f9cf-190">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f9cf-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f9cf-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f9cf-191">INPUTS</span></span>

### <span data-ttu-id="5f9cf-192">System. String</span><span class="sxs-lookup"><span data-stu-id="5f9cf-192">System.String</span></span>

### <span data-ttu-id="5f9cf-193">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5f9cf-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5f9cf-194">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9cf-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="5f9cf-195">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="5f9cf-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="5f9cf-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5f9cf-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5f9cf-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f9cf-197">OUTPUTS</span></span>

### <span data-ttu-id="5f9cf-198">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5f9cf-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="5f9cf-199">Note</span><span class="sxs-lookup"><span data-stu-id="5f9cf-199">NOTES</span></span>

## <span data-ttu-id="5f9cf-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f9cf-200">RELATED LINKS</span></span>

[<span data-ttu-id="5f9cf-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5f9cf-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="5f9cf-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5f9cf-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="5f9cf-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5f9cf-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)