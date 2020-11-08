---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: fcae55c69b1874e06ce9110631baaf3b679fe99a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191702"
---
# <span data-ttu-id="0337d-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0337d-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="0337d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0337d-102">SYNOPSIS</span></span>
<span data-ttu-id="0337d-103">Modifica di una revisione API</span><span class="sxs-lookup"><span data-stu-id="0337d-103">Modifies an API Revision</span></span>

## <span data-ttu-id="0337d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0337d-104">SYNTAX</span></span>

### <span data-ttu-id="0337d-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0337d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 [-Name <String>] [-Description <String>] [-ServiceUrl <String>] [-Path <String>]
 [-Protocols <PsApiManagementSchema[]>] [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-OpenIdProviderId <String>] [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0337d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0337d-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0337d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0337d-107">DESCRIPTION</span></span>
<span data-ttu-id="0337d-108">Il cmdlet **set-AzApiManagementApiRevision** modifica una revisione API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="0337d-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="0337d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0337d-109">EXAMPLES</span></span>

### <span data-ttu-id="0337d-110">Esempio 1: modificare una revisione delle API</span><span class="sxs-lookup"><span data-stu-id="0337d-110">Example 1: Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="0337d-111">Il cmdlet aggiorna la `2` revisione dell'API `echo-api` con una nuova descrizione, un protocollo e un percorso.</span><span class="sxs-lookup"><span data-stu-id="0337d-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="0337d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0337d-112">PARAMETERS</span></span>

### <span data-ttu-id="0337d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0337d-113">-ApiId</span></span>
<span data-ttu-id="0337d-114">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="0337d-114">Identifier of existing API.</span></span>
<span data-ttu-id="0337d-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0337d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="0337d-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="0337d-116">-ApiRevision</span></span>
<span data-ttu-id="0337d-117">Identificatore della revisione API esistente.</span><span class="sxs-lookup"><span data-stu-id="0337d-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="0337d-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0337d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0337d-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="0337d-119">-AuthorizationScope</span></span>
<span data-ttu-id="0337d-120">Ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="0337d-120">OAuth operations scope.</span></span>
<span data-ttu-id="0337d-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-121">This parameter is optional.</span></span>
<span data-ttu-id="0337d-122">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-122">Default value is $null.</span></span>

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

### <span data-ttu-id="0337d-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="0337d-123">-AuthorizationServerId</span></span>
<span data-ttu-id="0337d-124">Identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="0337d-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="0337d-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-125">This parameter is optional.</span></span>
<span data-ttu-id="0337d-126">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-126">Default value is $null.</span></span>
<span data-ttu-id="0337d-127">Deve essere specificato se AuthorizationScope specificato.</span><span class="sxs-lookup"><span data-stu-id="0337d-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="0337d-128">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="0337d-128">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="0337d-129">Meccanismo del server di autorizzazione OpenId tramite il quale il token di accesso viene passato all'API.</span><span class="sxs-lookup"><span data-stu-id="0337d-129">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="0337d-130">Fare riferimento a http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="0337d-130">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="0337d-131">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-131">This parameter is optional.</span></span> <span data-ttu-id="0337d-132">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-132">Default value is $null.</span></span>

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

### <span data-ttu-id="0337d-133">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0337d-133">-Context</span></span>
<span data-ttu-id="0337d-134">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0337d-134">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0337d-135">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0337d-135">This parameter is required.</span></span>

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

### <span data-ttu-id="0337d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0337d-136">-DefaultProfile</span></span>
<span data-ttu-id="0337d-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0337d-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0337d-138">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0337d-138">-Description</span></span>
<span data-ttu-id="0337d-139">Descrizione dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="0337d-139">Web API description.</span></span>
<span data-ttu-id="0337d-140">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="0337d-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0337d-141">-InputObject</span></span>
<span data-ttu-id="0337d-142">Istanza di PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="0337d-142">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="0337d-143">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0337d-143">This parameter is required.</span></span>

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

### <span data-ttu-id="0337d-144">-Nome</span><span class="sxs-lookup"><span data-stu-id="0337d-144">-Name</span></span>
<span data-ttu-id="0337d-145">Nome API Web.</span><span class="sxs-lookup"><span data-stu-id="0337d-145">Web API name.</span></span>
<span data-ttu-id="0337d-146">Nome pubblico dell'API come comparirebbe nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="0337d-146">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="0337d-147">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0337d-147">This parameter is required.</span></span>

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

### <span data-ttu-id="0337d-148">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="0337d-148">-OpenIdProviderId</span></span>
<span data-ttu-id="0337d-149">Identificatore del server di autorizzazione OpenId.</span><span class="sxs-lookup"><span data-stu-id="0337d-149">OpenId authorization server identifier.</span></span> <span data-ttu-id="0337d-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-150">This parameter is optional.</span></span> <span data-ttu-id="0337d-151">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-151">Default value is $null.</span></span> <span data-ttu-id="0337d-152">Deve essere specificato se BearerTokenSendingMethods è specificato.</span><span class="sxs-lookup"><span data-stu-id="0337d-152">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="0337d-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0337d-153">-PassThru</span></span>
<span data-ttu-id="0337d-154">Se specificato, l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi che rappresenta l'API set.</span><span class="sxs-lookup"><span data-stu-id="0337d-154">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="0337d-155">-Path</span><span class="sxs-lookup"><span data-stu-id="0337d-155">-Path</span></span>
<span data-ttu-id="0337d-156">Percorso API Web.</span><span class="sxs-lookup"><span data-stu-id="0337d-156">Web API Path.</span></span>
<span data-ttu-id="0337d-157">Ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="0337d-157">Last part of the API's public URL.</span></span>
<span data-ttu-id="0337d-158">Questo URL verrà usato dagli utenti dell'API per l'invio di richieste al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="0337d-158">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="0337d-159">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0337d-159">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="0337d-160">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-160">This parameter is optional.</span></span>
<span data-ttu-id="0337d-161">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-161">Default value is $null.</span></span>

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

### <span data-ttu-id="0337d-162">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="0337d-162">-Protocols</span></span>
<span data-ttu-id="0337d-163">Protocolli API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="0337d-163">Web API protocols (http, https).</span></span>
<span data-ttu-id="0337d-164">Protocolli su cui viene resa disponibile l'API.</span><span class="sxs-lookup"><span data-stu-id="0337d-164">Protocols over which API is made available.</span></span>
<span data-ttu-id="0337d-165">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0337d-165">This parameter is required.</span></span>
<span data-ttu-id="0337d-166">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-166">Default value is $null.</span></span>

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

### <span data-ttu-id="0337d-167">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="0337d-167">-ServiceUrl</span></span>
<span data-ttu-id="0337d-168">URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="0337d-168">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="0337d-169">Questo URL verrà usato solo dalla gestione delle API di Azure e non verrà reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="0337d-169">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="0337d-170">Deve essere lunga da 1 a 2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="0337d-170">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="0337d-171">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0337d-171">This parameter is required.</span></span>

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

### <span data-ttu-id="0337d-172">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="0337d-172">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="0337d-173">Nome intestazione chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0337d-173">Subscription key header name.</span></span>
<span data-ttu-id="0337d-174">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-174">This parameter is optional.</span></span>
<span data-ttu-id="0337d-175">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-175">Default value is $null.</span></span>

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

### <span data-ttu-id="0337d-176">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="0337d-176">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="0337d-177">Nome parametro stringa query chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0337d-177">Subscription key query string parameter name.</span></span>
<span data-ttu-id="0337d-178">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-178">This parameter is optional.</span></span>
<span data-ttu-id="0337d-179">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="0337d-179">Default value is $null.</span></span>

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

### <span data-ttu-id="0337d-180">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="0337d-180">-SubscriptionRequired</span></span>
<span data-ttu-id="0337d-181">Flag per applicare SubscriptionRequired per le richieste all'API.</span><span class="sxs-lookup"><span data-stu-id="0337d-181">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="0337d-182">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0337d-182">This parameter is optional.</span></span>

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

### <span data-ttu-id="0337d-183">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0337d-183">-Confirm</span></span>
<span data-ttu-id="0337d-184">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0337d-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0337d-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0337d-185">-WhatIf</span></span>
<span data-ttu-id="0337d-186">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0337d-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0337d-187">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0337d-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0337d-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0337d-188">CommonParameters</span></span>
<span data-ttu-id="0337d-189">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0337d-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0337d-190">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0337d-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0337d-191">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0337d-191">INPUTS</span></span>

### <span data-ttu-id="0337d-192">System. String</span><span class="sxs-lookup"><span data-stu-id="0337d-192">System.String</span></span>

### <span data-ttu-id="0337d-193">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0337d-193">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0337d-194">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0337d-194">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="0337d-195">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="0337d-195">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="0337d-196">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0337d-196">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0337d-197">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0337d-197">OUTPUTS</span></span>

### <span data-ttu-id="0337d-198">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0337d-198">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="0337d-199">Note</span><span class="sxs-lookup"><span data-stu-id="0337d-199">NOTES</span></span>

## <span data-ttu-id="0337d-200">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0337d-200">RELATED LINKS</span></span>

[<span data-ttu-id="0337d-201">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0337d-201">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="0337d-202">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0337d-202">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="0337d-203">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="0337d-203">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)