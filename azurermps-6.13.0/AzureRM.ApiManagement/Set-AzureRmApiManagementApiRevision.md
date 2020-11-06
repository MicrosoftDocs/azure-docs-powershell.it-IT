---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: fe709b560c790ad010469bf2f0a2043231124138
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519776"
---
# <span data-ttu-id="5409f-101">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5409f-101">Set-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="5409f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5409f-102">SYNOPSIS</span></span>
<span data-ttu-id="5409f-103">Modifica di una revisione API</span><span class="sxs-lookup"><span data-stu-id="5409f-103">Modifies an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5409f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5409f-104">SYNTAX</span></span>

### <span data-ttu-id="5409f-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5409f-105">ExpandedParameter (Default)</span></span>
```
Set-AzureRmApiManagementApiRevision -ApiRevision <String> -Context <PsApiManagementContext> -ApiId <String>
 -Name <String> [-Description <String>] -ServiceUrl <String> [-Path <String>]
 -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>] [-AuthorizationScope <String>]
 [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5409f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5409f-106">ByInputObject</span></span>
```
Set-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5409f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5409f-107">DESCRIPTION</span></span>
<span data-ttu-id="5409f-108">Il cmdlet **set-AzureRmApiManagementApiRevision** modifica una revisione API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="5409f-108">The **Set-AzureRmApiManagementApiRevision** cmdlet modifies an Azure API Management API Revision.</span></span>

## <span data-ttu-id="5409f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5409f-109">EXAMPLES</span></span>

### <span data-ttu-id="5409f-110">Esempio 1 modificare una revisione API</span><span class="sxs-lookup"><span data-stu-id="5409f-110">Example 1 Modify an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApiRevision -Context $ApiMgmtContext -ApiId "echo-api" -ApiRevision "2" -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

<span data-ttu-id="5409f-111">Il cmdlet aggiorna la `2` revisione dell'API `echo-api` con una nuova descrizione, un protocollo e un percorso.</span><span class="sxs-lookup"><span data-stu-id="5409f-111">The cmdlet updates the `2` revision of the API `echo-api` with a new description, protocol and path.</span></span>

## <span data-ttu-id="5409f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5409f-112">PARAMETERS</span></span>

### <span data-ttu-id="5409f-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5409f-113">-ApiId</span></span>
<span data-ttu-id="5409f-114">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="5409f-114">Identifier of existing API.</span></span>
<span data-ttu-id="5409f-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5409f-115">This parameter is required.</span></span>

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

### <span data-ttu-id="5409f-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="5409f-116">-ApiRevision</span></span>
<span data-ttu-id="5409f-117">Identificatore della revisione API esistente.</span><span class="sxs-lookup"><span data-stu-id="5409f-117">Identifier of existing API Revision.</span></span> <span data-ttu-id="5409f-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5409f-118">This parameter is required.</span></span>

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

### <span data-ttu-id="5409f-119">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="5409f-119">-AuthorizationScope</span></span>
<span data-ttu-id="5409f-120">Ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="5409f-120">OAuth operations scope.</span></span>
<span data-ttu-id="5409f-121">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5409f-121">This parameter is optional.</span></span>
<span data-ttu-id="5409f-122">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5409f-122">Default value is $null.</span></span>

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

### <span data-ttu-id="5409f-123">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="5409f-123">-AuthorizationServerId</span></span>
<span data-ttu-id="5409f-124">Identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="5409f-124">OAuth authorization server identifier.</span></span>
<span data-ttu-id="5409f-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5409f-125">This parameter is optional.</span></span>
<span data-ttu-id="5409f-126">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5409f-126">Default value is $null.</span></span>
<span data-ttu-id="5409f-127">Deve essere specificato se AuthorizationScope specificato.</span><span class="sxs-lookup"><span data-stu-id="5409f-127">Must be specified if AuthorizationScope specified.</span></span>

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

### <span data-ttu-id="5409f-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5409f-128">-Context</span></span>
<span data-ttu-id="5409f-129">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5409f-129">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5409f-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5409f-130">This parameter is required.</span></span>

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

### <span data-ttu-id="5409f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5409f-131">-DefaultProfile</span></span>
<span data-ttu-id="5409f-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5409f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5409f-133">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="5409f-133">-Description</span></span>
<span data-ttu-id="5409f-134">Descrizione dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="5409f-134">Web API description.</span></span>
<span data-ttu-id="5409f-135">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5409f-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="5409f-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5409f-136">-InputObject</span></span>
<span data-ttu-id="5409f-137">Istanza di PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="5409f-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="5409f-138">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5409f-138">This parameter is required.</span></span>

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

### <span data-ttu-id="5409f-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="5409f-139">-Name</span></span>
<span data-ttu-id="5409f-140">Nome API Web.</span><span class="sxs-lookup"><span data-stu-id="5409f-140">Web API name.</span></span>
<span data-ttu-id="5409f-141">Nome pubblico dell'API come comparirebbe nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="5409f-141">Public name of the API as it would appear on the developer and admin portals.</span></span>
<span data-ttu-id="5409f-142">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5409f-142">This parameter is required.</span></span>

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

### <span data-ttu-id="5409f-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5409f-143">-PassThru</span></span>
<span data-ttu-id="5409f-144">Se specificato, l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi che rappresenta l'API set.</span><span class="sxs-lookup"><span data-stu-id="5409f-144">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="5409f-145">-Path</span><span class="sxs-lookup"><span data-stu-id="5409f-145">-Path</span></span>
<span data-ttu-id="5409f-146">Percorso API Web.</span><span class="sxs-lookup"><span data-stu-id="5409f-146">Web API Path.</span></span>
<span data-ttu-id="5409f-147">Ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="5409f-147">Last part of the API's public URL.</span></span>
<span data-ttu-id="5409f-148">Questo URL verrà usato dagli utenti dell'API per l'invio di richieste al servizio Web.</span><span class="sxs-lookup"><span data-stu-id="5409f-148">This URL will be used by API consumers for sending requests to the web service.</span></span>
<span data-ttu-id="5409f-149">Deve essere lunga da 1 a 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5409f-149">Must be 1 to 400 characters long.</span></span>
<span data-ttu-id="5409f-150">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5409f-150">This parameter is optional.</span></span>
<span data-ttu-id="5409f-151">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5409f-151">Default value is $null.</span></span>

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

### <span data-ttu-id="5409f-152">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="5409f-152">-Protocols</span></span>
<span data-ttu-id="5409f-153">Protocolli API Web (http, HTTPS).</span><span class="sxs-lookup"><span data-stu-id="5409f-153">Web API protocols (http, https).</span></span>
<span data-ttu-id="5409f-154">Protocolli su cui viene resa disponibile l'API.</span><span class="sxs-lookup"><span data-stu-id="5409f-154">Protocols over which API is made available.</span></span>
<span data-ttu-id="5409f-155">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5409f-155">This parameter is required.</span></span>
<span data-ttu-id="5409f-156">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5409f-156">Default value is $null.</span></span>

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

### <span data-ttu-id="5409f-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="5409f-157">-ServiceUrl</span></span>
<span data-ttu-id="5409f-158">URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="5409f-158">A URL of the web service exposing the API.</span></span>
<span data-ttu-id="5409f-159">Questo URL verrà usato solo dalla gestione delle API di Azure e non verrà reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="5409f-159">This URL will be used by Azure API Management only, and will not be made public.</span></span>
<span data-ttu-id="5409f-160">Deve essere lunga da 1 a 2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="5409f-160">Must be 1 to 2000 characters long.</span></span>
<span data-ttu-id="5409f-161">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="5409f-161">This parameter is required.</span></span>

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

### <span data-ttu-id="5409f-162">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="5409f-162">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="5409f-163">Nome intestazione chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5409f-163">Subscription key header name.</span></span>
<span data-ttu-id="5409f-164">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5409f-164">This parameter is optional.</span></span>
<span data-ttu-id="5409f-165">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5409f-165">Default value is $null.</span></span>

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

### <span data-ttu-id="5409f-166">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="5409f-166">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="5409f-167">Nome parametro stringa query chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="5409f-167">Subscription key query string parameter name.</span></span>
<span data-ttu-id="5409f-168">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="5409f-168">This parameter is optional.</span></span>
<span data-ttu-id="5409f-169">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="5409f-169">Default value is $null.</span></span>

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

### <span data-ttu-id="5409f-170">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5409f-170">-Confirm</span></span>
<span data-ttu-id="5409f-171">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5409f-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5409f-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5409f-172">-WhatIf</span></span>
<span data-ttu-id="5409f-173">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5409f-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5409f-174">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5409f-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5409f-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5409f-175">CommonParameters</span></span>
<span data-ttu-id="5409f-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5409f-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5409f-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5409f-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5409f-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5409f-178">INPUTS</span></span>

### <span data-ttu-id="5409f-179">System. String</span><span class="sxs-lookup"><span data-stu-id="5409f-179">System.String</span></span>

### <span data-ttu-id="5409f-180">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5409f-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5409f-181">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5409f-181">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="5409f-182">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5409f-182">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="5409f-183">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="5409f-183">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="5409f-184">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5409f-184">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5409f-185">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5409f-185">OUTPUTS</span></span>

### <span data-ttu-id="5409f-186">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5409f-186">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="5409f-187">Note</span><span class="sxs-lookup"><span data-stu-id="5409f-187">NOTES</span></span>

## <span data-ttu-id="5409f-188">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5409f-188">RELATED LINKS</span></span>

[<span data-ttu-id="5409f-189">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5409f-189">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="5409f-190">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5409f-190">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="5409f-191">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="5409f-191">Remove-AzureRmApiManagementApiRevision</span></span>](./Remove-AzureRmApiManagementApiRevision.md)
