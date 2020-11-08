---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 02a7a35f4498724266d4c352744169d733f5eeab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032699"
---
# <span data-ttu-id="9fefe-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="9fefe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9fefe-102">SYNOPSIS</span></span>
<span data-ttu-id="9fefe-103">Modifica un'API.</span><span class="sxs-lookup"><span data-stu-id="9fefe-103">Modifies an API.</span></span>

## <span data-ttu-id="9fefe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9fefe-104">SYNTAX</span></span>

### <span data-ttu-id="9fefe-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9fefe-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9fefe-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9fefe-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fefe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fefe-107">DESCRIPTION</span></span>
<span data-ttu-id="9fefe-108">Il cmdlet **set-AzApiManagementApi** modifica un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="9fefe-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="9fefe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9fefe-109">EXAMPLES</span></span>

### <span data-ttu-id="9fefe-110">Esempio 1: modificare un'API</span><span class="sxs-lookup"><span data-stu-id="9fefe-110">Example 1: Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="9fefe-111">Esempio 2: aggiungere un'API a un ApiVersionSet esistente</span><span class="sxs-lookup"><span data-stu-id="9fefe-111">Example 2: Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```

<span data-ttu-id="9fefe-112">Questo esempio aggiunge un'API a un set di versioni API esistente</span><span class="sxs-lookup"><span data-stu-id="9fefe-112">This example adds an API to an existing API Version Set</span></span>

### <span data-ttu-id="9fefe-113">Esempio 3: cambiare il backend di ServiceUrl in cui punta l'API</span><span class="sxs-lookup"><span data-stu-id="9fefe-113">Example 3: Change the Backend ServiceUrl where the API is pointing to</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$updatedApiServiceUrl = "http://newechoapi.cloudapp.net/updateapi"
PS C:\>$updatedApi = Set-AzApiManagementApi -Context $ApiMgmtContext -ApiId $echoApiId -ServiceUrl $updatedApiServiceUrl
```

<span data-ttu-id="9fefe-114">Questo esempio aggiorna l'ServiceUrl `echo-api` a cui punta.</span><span class="sxs-lookup"><span data-stu-id="9fefe-114">This example updates the ServiceUrl the `echo-api` is pointing to.</span></span>

## <span data-ttu-id="9fefe-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9fefe-115">PARAMETERS</span></span>

### <span data-ttu-id="9fefe-116">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9fefe-116">-ApiId</span></span>
<span data-ttu-id="9fefe-117">Specifica l'ID dell'API da modificare.</span><span class="sxs-lookup"><span data-stu-id="9fefe-117">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="9fefe-118">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9fefe-118">-AuthorizationScope</span></span>
<span data-ttu-id="9fefe-119">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="9fefe-119">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="9fefe-120">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-120">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fefe-121">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9fefe-121">-AuthorizationServerId</span></span>
<span data-ttu-id="9fefe-122">Specifica l'identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="9fefe-122">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="9fefe-123">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-123">The default value is $Null.</span></span>
<span data-ttu-id="9fefe-124">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="9fefe-124">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="9fefe-125">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="9fefe-125">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="9fefe-126">Meccanismo del server di autorizzazione OpenId tramite il quale il token di accesso viene passato all'API.</span><span class="sxs-lookup"><span data-stu-id="9fefe-126">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="9fefe-127">Fare riferimento a http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="9fefe-127">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="9fefe-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9fefe-128">This parameter is optional.</span></span> <span data-ttu-id="9fefe-129">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-129">Default value is $null.</span></span>

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

### <span data-ttu-id="9fefe-130">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9fefe-130">-Context</span></span>
<span data-ttu-id="9fefe-131">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9fefe-131">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9fefe-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fefe-132">-DefaultProfile</span></span>
<span data-ttu-id="9fefe-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9fefe-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fefe-134">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9fefe-134">-Description</span></span>
<span data-ttu-id="9fefe-135">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="9fefe-135">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="9fefe-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9fefe-136">-InputObject</span></span>
<span data-ttu-id="9fefe-137">Istanza di PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="9fefe-137">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="9fefe-138">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9fefe-138">This parameter is required.</span></span>

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

### <span data-ttu-id="9fefe-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="9fefe-139">-Name</span></span>
<span data-ttu-id="9fefe-140">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="9fefe-140">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="9fefe-141">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="9fefe-141">-OpenIdProviderId</span></span>
<span data-ttu-id="9fefe-142">Identificatore del server di autorizzazione OpenId.</span><span class="sxs-lookup"><span data-stu-id="9fefe-142">OpenId authorization server identifier.</span></span> <span data-ttu-id="9fefe-143">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9fefe-143">This parameter is optional.</span></span> <span data-ttu-id="9fefe-144">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-144">Default value is $null.</span></span> <span data-ttu-id="9fefe-145">Deve essere specificato se BearerTokenSendingMethods è specificato.</span><span class="sxs-lookup"><span data-stu-id="9fefe-145">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="9fefe-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9fefe-146">-PassThru</span></span>
<span data-ttu-id="9fefe-147">PassThru</span><span class="sxs-lookup"><span data-stu-id="9fefe-147">passthru</span></span>

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

### <span data-ttu-id="9fefe-148">-Path</span><span class="sxs-lookup"><span data-stu-id="9fefe-148">-Path</span></span>
<span data-ttu-id="9fefe-149">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="9fefe-149">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="9fefe-150">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9fefe-150">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="9fefe-151">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-151">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fefe-152">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="9fefe-152">-Protocols</span></span>
<span data-ttu-id="9fefe-153">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="9fefe-153">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="9fefe-154">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9fefe-154">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="9fefe-155">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="9fefe-155">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="9fefe-156">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-156">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fefe-157">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9fefe-157">-ServiceUrl</span></span>
<span data-ttu-id="9fefe-158">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="9fefe-158">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="9fefe-159">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="9fefe-159">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="9fefe-160">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9fefe-160">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="9fefe-161">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9fefe-161">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9fefe-162">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9fefe-162">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="9fefe-163">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-163">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fefe-164">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9fefe-164">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9fefe-165">Specifica il nome del parametro della stringa di query della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9fefe-165">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="9fefe-166">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9fefe-166">The default value is $Null.</span></span>

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

### <span data-ttu-id="9fefe-167">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="9fefe-167">-SubscriptionRequired</span></span>
<span data-ttu-id="9fefe-168">Flag per applicare SubscriptionRequired per le richieste all'API.</span><span class="sxs-lookup"><span data-stu-id="9fefe-168">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="9fefe-169">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9fefe-169">This parameter is optional.</span></span>

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

### <span data-ttu-id="9fefe-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fefe-170">CommonParameters</span></span>
<span data-ttu-id="9fefe-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fefe-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fefe-172">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fefe-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fefe-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9fefe-173">INPUTS</span></span>

### <span data-ttu-id="9fefe-174">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9fefe-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9fefe-175">System. String</span><span class="sxs-lookup"><span data-stu-id="9fefe-175">System.String</span></span>

### <span data-ttu-id="9fefe-176">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-176">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="9fefe-177">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="9fefe-177">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="9fefe-178">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9fefe-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9fefe-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9fefe-179">OUTPUTS</span></span>

### <span data-ttu-id="9fefe-180">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-180">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9fefe-181">Note</span><span class="sxs-lookup"><span data-stu-id="9fefe-181">NOTES</span></span>

## <span data-ttu-id="9fefe-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9fefe-182">RELATED LINKS</span></span>

[<span data-ttu-id="9fefe-183">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-183">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="9fefe-184">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-184">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9fefe-185">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-185">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9fefe-186">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-186">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="9fefe-187">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9fefe-187">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


