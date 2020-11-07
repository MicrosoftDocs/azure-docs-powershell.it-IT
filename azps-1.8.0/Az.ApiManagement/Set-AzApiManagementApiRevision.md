---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiRevision.md
ms.openlocfilehash: 8b2e29da3c3f6140cbab422e74d09656c921c16c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852405"
---
# <span data-ttu-id="8577d-101">Set-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8577d-101">Set-AzApiManagementApiRevision</span></span>

## <span data-ttu-id="8577d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8577d-102">SYNOPSIS</span></span>
<span data-ttu-id="8577d-103">Modifica di una revisione API</span><span class="sxs-lookup"><span data-stu-id="8577d-103">Modifies an API Revision</span></span>

## <span data-ttu-id="8577d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8577d-104">SYNTAX</span></span>

### <span data-ttu-id="8577d-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8577d-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8577d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8577d-106">ByInputObject</span></span>
```
Set-AzApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8577d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8577d-107">DESCRIPTION</span></span>
<span data-ttu-id="8577d-108">Il cmdlet **set-AzApiManagementApiRevision** modifica una revisione API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="8577d-108">The **Set-AzApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="8577d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8577d-109">EXAMPLES</span></span>

### <span data-ttu-id="8577d-110">Esempio 1 modificare una revisione API</span><span class="sxs-lookup"><span data-stu-id="8577d-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="8577d-111">Il cmdlet aggiorna la `2` revisione dell'API `echo-api` con una nuova descrizione, un protocollo e un percorso.</span><span class="sxs-lookup"><span data-stu-id="8577d-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="8577d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8577d-112">PARAMETERS</span></span>

### <span data-ttu-id="8577d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8577d-113">-ApiId</span></span>
<span data-ttu-id="8577d-114">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="8577d-114">Identifier of existing API.</span></span>
<span data-ttu-id="8577d-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8577d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="8577d-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="8577d-116">-ApiRevision</span></span>
<span data-ttu-id="8577d-117">Identificatore della revisione API esistente.</span><span class="sxs-lookup"><span data-stu-id="8577d-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="8577d-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8577d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="8577d-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="8577d-119">-AuthorizationScope</span></span>
<span data-ttu-id="8577d-120">Ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="8577d-120">OAuth operations scope.</span></span>
<span data-ttu-id="8577d-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8577d-121">This parameter is optional.</span></span>
<span data-ttu-id="8577d-122">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="8577d-122">Default value is $null.</span></span>

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

### <span data-ttu-id="8577d-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="8577d-123">-AuthorizationServerId</span></span>
<span data-ttu-id="8577d-124">Identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="8577d-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="8577d-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8577d-125">This parameter is optional.</span></span>
<span data-ttu-id="8577d-126">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="8577d-126">Default value is $null.</span></span>
<span data-ttu-id="8577d-127">Deve essere specificato se AuthorizationScope specificato.</span><span class="sxs-lookup"><span data-stu-id="8577d-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="8577d-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="8577d-128">-Context</span></span>
<span data-ttu-id="8577d-129">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8577d-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8577d-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8577d-130">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8577d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8577d-131">-DefaultProfile</span></span>
<span data-ttu-id="8577d-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8577d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8577d-133">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="8577d-133">-Description</span></span>
<span data-ttu-id="8577d-134">Descrizione dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="8577d-134">Web API description.</span></span>
<span data-ttu-id="8577d-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8577d-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="8577d-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8577d-136">-InputObject</span></span>
<span data-ttu-id="8577d-137">Istanza di PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="8577d-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="8577d-138">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8577d-138">This parameter is required.</span></span>

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

### <span data-ttu-id="8577d-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="8577d-139">-Name</span></span>
<span data-ttu-id="8577d-140">Nome API Web.</span><span class="sxs-lookup"><span data-stu-id="8577d-140">Web API name.</span></span>
<span data-ttu-id="8577d-141">Nome pubblico dell'API come comparirebbe nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="8577d-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="8577d-142">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8577d-142">This parameter is required.</span></span>

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

### <span data-ttu-id="8577d-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8577d-143">-PassThru</span></span>
<span data-ttu-id="8577d-144">Se specificato, l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi che rappresenta l'API set.</span><span class="sxs-lookup"><span data-stu-id="8577d-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="8577d-145">-Path</span><span class="sxs-lookup"><span data-stu-id="8577d-145">-Path</span></span>
<span data-ttu-id="8577d-146">Percorso API Web.</span><span class="sxs-lookup"><span data-stu-id="8577d-146">Web API Path.</span></span>
<span data-ttu-id="8577d-147">Ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="8577d-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="8577d-148">Questo URL verrà usato dagli utenti dell'API per l'invio di richieste al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="8577d-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="8577d-149">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="8577d-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="8577d-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8577d-150">This parameter is optional.</span></span>
<span data-ttu-id="8577d-151">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="8577d-151">Default value is $null.</span></span>

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

### <span data-ttu-id="8577d-152">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="8577d-152">-Protocols</span></span>
<span data-ttu-id="8577d-153">Protocolli API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="8577d-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="8577d-154">Protocolli su cui viene resa disponibile l'API.</span><span class="sxs-lookup"><span data-stu-id="8577d-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="8577d-155">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8577d-155">This parameter is required.</span></span>
<span data-ttu-id="8577d-156">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="8577d-156">Default value is $null.</span></span>

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

### <span data-ttu-id="8577d-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="8577d-157">-ServiceUrl</span></span>
<span data-ttu-id="8577d-158">URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="8577d-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="8577d-159">Questo URL verrà usato solo dalla gestione delle API di Azure e non verrà reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="8577d-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="8577d-160">Deve essere lunga da 1 a 2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="8577d-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="8577d-161">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="8577d-161">This parameter is required.</span></span>

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

### <span data-ttu-id="8577d-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="8577d-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="8577d-163">Nome intestazione chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8577d-163">Subscription key header name.</span></span>
<span data-ttu-id="8577d-164">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8577d-164">This parameter is optional.</span></span>
<span data-ttu-id="8577d-165">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="8577d-165">Default value is $null.</span></span>

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

### <span data-ttu-id="8577d-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="8577d-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="8577d-167">Nome parametro stringa query chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8577d-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="8577d-168">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="8577d-168">This parameter is optional.</span></span>
<span data-ttu-id="8577d-169">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="8577d-169">Default value is $null.</span></span>

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

### <span data-ttu-id="8577d-170">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8577d-170">-Confirm</span></span>
<span data-ttu-id="8577d-171">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8577d-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8577d-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8577d-172">-WhatIf</span></span>
<span data-ttu-id="8577d-173">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8577d-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8577d-174">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8577d-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8577d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8577d-175">CommonParameters</span></span>
<span data-ttu-id="8577d-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8577d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8577d-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8577d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8577d-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8577d-178">INPUTS</span></span>

### <span data-ttu-id="8577d-179">System. String</span><span class="sxs-lookup"><span data-stu-id="8577d-179">System.String</span></span>

### <span data-ttu-id="8577d-180">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8577d-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8577d-181">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8577d-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="8577d-182">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="8577d-182">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="8577d-183">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8577d-183">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8577d-184">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8577d-184">OUTPUTS</span></span>

### <span data-ttu-id="8577d-185">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8577d-185">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8577d-186">Note</span><span class="sxs-lookup"><span data-stu-id="8577d-186">NOTES</span></span>

## <span data-ttu-id="8577d-187">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8577d-187">RELATED LINKS</span></span>

[<span data-ttu-id="8577d-188">Get-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8577d-188">Get-AzApiManagementApiRevision</span></span>](./Get-AzApiManagementApiRevision.md)

[<span data-ttu-id="8577d-189">New-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8577d-189">New-AzApiManagementApiRevision</span></span>](./New-AzApiManagementApiRevision.md)

[<span data-ttu-id="8577d-190">Remove-AzApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="8577d-190">Remove-AzApiManagementApiRevision</span></span>](./Remove-AzApiManagementApiRevision.md)