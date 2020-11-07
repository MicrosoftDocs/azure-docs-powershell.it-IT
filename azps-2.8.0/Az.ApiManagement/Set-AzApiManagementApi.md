---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 973dc9bac629ee9a82b7624053f689bf7884fd8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675911"
---
# <span data-ttu-id="c27d6-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="c27d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c27d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c27d6-103">Modifica un'API.</span><span class="sxs-lookup"><span data-stu-id="c27d6-103">Modifies an API.</span></span>

## <span data-ttu-id="c27d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c27d6-104">SYNTAX</span></span>

### <span data-ttu-id="c27d6-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c27d6-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-Name <String>]
 [-Description <String>] [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c27d6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c27d6-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> [-Name <String>] [-Description <String>]
 [-ServiceUrl <String>] [-Path <String>] [-Protocols <PsApiManagementSchema[]>]
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-OpenIdProviderId <String>]
 [-BearerTokenSendingMethod <String[]>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-SubscriptionRequired] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c27d6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c27d6-107">DESCRIPTION</span></span>
<span data-ttu-id="c27d6-108">Il cmdlet **set-AzApiManagementApi** modifica un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="c27d6-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="c27d6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c27d6-109">EXAMPLES</span></span>

### <span data-ttu-id="c27d6-110">Esempio 1 modificare un'API</span><span class="sxs-lookup"><span data-stu-id="c27d6-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

### <span data-ttu-id="c27d6-111">Esempio 2 aggiunta di un'API a un ApiVersionSet esistente</span><span class="sxs-lookup"><span data-stu-id="c27d6-111">Example 2 Add an API to an existing ApiVersionSet</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$versionSet = New-AzApiManagementApiVersionSet -Context $context -Name "Echo API Version Set" -Scheme Segment -Description "version set sample"
PS C:\>$api = Get-AzApiManagementApi -Context $ApiMgmtContext -ApiId "echo-api"
PS C:\>$api.ApiVersionSetId = $versionSet.Id
PS C:\>$api.ApiVersion = "v1"
PS C:\>$api.ApiVersionSetDescription = $versionSet.Description
PS C:\>Set-AzApiManagementApi -InputObject $api -PassThru
```
<span data-ttu-id="c27d6-112">Questo esempio aggiunge un'API a un set di versioni API esistente</span><span class="sxs-lookup"><span data-stu-id="c27d6-112">This example adds an API to an existing API Version Set</span></span>

## <span data-ttu-id="c27d6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c27d6-113">PARAMETERS</span></span>

### <span data-ttu-id="c27d6-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c27d6-114">-ApiId</span></span>
<span data-ttu-id="c27d6-115">Specifica l'ID dell'API da modificare.</span><span class="sxs-lookup"><span data-stu-id="c27d6-115">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="c27d6-116">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="c27d6-116">-AuthorizationScope</span></span>
<span data-ttu-id="c27d6-117">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="c27d6-117">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="c27d6-118">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-118">The default value is $Null.</span></span>

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

### <span data-ttu-id="c27d6-119">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="c27d6-119">-AuthorizationServerId</span></span>
<span data-ttu-id="c27d6-120">Specifica l'identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="c27d6-120">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="c27d6-121">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-121">The default value is $Null.</span></span>
<span data-ttu-id="c27d6-122">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="c27d6-122">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="c27d6-123">-BearerTokenSendingMethod</span><span class="sxs-lookup"><span data-stu-id="c27d6-123">-BearerTokenSendingMethod</span></span>
<span data-ttu-id="c27d6-124">Meccanismo del server di autorizzazione OpenId tramite il quale il token di accesso viene passato all'API.</span><span class="sxs-lookup"><span data-stu-id="c27d6-124">OpenId authorization server mechanism by which access token is passed to the API.</span></span> <span data-ttu-id="c27d6-125">Fare riferimento a http://tools.ietf.org/html/rfc6749#section-4 .</span><span class="sxs-lookup"><span data-stu-id="c27d6-125">Refer to http://tools.ietf.org/html/rfc6749#section-4.</span></span> <span data-ttu-id="c27d6-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c27d6-126">This parameter is optional.</span></span> <span data-ttu-id="c27d6-127">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-127">Default value is $null.</span></span>

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

### <span data-ttu-id="c27d6-128">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c27d6-128">-Context</span></span>
<span data-ttu-id="c27d6-129">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c27d6-129">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c27d6-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27d6-130">-DefaultProfile</span></span>
<span data-ttu-id="c27d6-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c27d6-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c27d6-132">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c27d6-132">-Description</span></span>
<span data-ttu-id="c27d6-133">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="c27d6-133">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="c27d6-134">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c27d6-134">-InputObject</span></span>
<span data-ttu-id="c27d6-135">Istanza di PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="c27d6-135">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="c27d6-136">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c27d6-136">This parameter is required.</span></span>

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

### <span data-ttu-id="c27d6-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="c27d6-137">-Name</span></span>
<span data-ttu-id="c27d6-138">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="c27d6-138">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="c27d6-139">-OpenIdProviderId</span><span class="sxs-lookup"><span data-stu-id="c27d6-139">-OpenIdProviderId</span></span>
<span data-ttu-id="c27d6-140">Identificatore del server di autorizzazione OpenId.</span><span class="sxs-lookup"><span data-stu-id="c27d6-140">OpenId authorization server identifier.</span></span> <span data-ttu-id="c27d6-141">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c27d6-141">This parameter is optional.</span></span> <span data-ttu-id="c27d6-142">Il valore predefinito è $null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-142">Default value is $null.</span></span> <span data-ttu-id="c27d6-143">Deve essere specificato se BearerTokenSendingMethods è specificato.</span><span class="sxs-lookup"><span data-stu-id="c27d6-143">Must be specified if BearerTokenSendingMethods is specified.</span></span>

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

### <span data-ttu-id="c27d6-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c27d6-144">-PassThru</span></span>
<span data-ttu-id="c27d6-145">PassThru</span><span class="sxs-lookup"><span data-stu-id="c27d6-145">passthru</span></span>

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

### <span data-ttu-id="c27d6-146">-Path</span><span class="sxs-lookup"><span data-stu-id="c27d6-146">-Path</span></span>
<span data-ttu-id="c27d6-147">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="c27d6-147">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="c27d6-148">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c27d6-148">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="c27d6-149">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="c27d6-150">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="c27d6-150">-Protocols</span></span>
<span data-ttu-id="c27d6-151">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="c27d6-151">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="c27d6-152">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="c27d6-152">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="c27d6-153">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="c27d6-153">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="c27d6-154">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-154">The default value is $Null.</span></span>

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

### <span data-ttu-id="c27d6-155">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="c27d6-155">-ServiceUrl</span></span>
<span data-ttu-id="c27d6-156">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="c27d6-156">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="c27d6-157">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="c27d6-157">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="c27d6-158">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="c27d6-158">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="c27d6-159">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="c27d6-159">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="c27d6-160">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c27d6-160">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="c27d6-161">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-161">The default value is $Null.</span></span>

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

### <span data-ttu-id="c27d6-162">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="c27d6-162">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="c27d6-163">Specifica il nome del parametro della stringa di query della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c27d6-163">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="c27d6-164">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="c27d6-164">The default value is $Null.</span></span>

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

### <span data-ttu-id="c27d6-165">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="c27d6-165">-SubscriptionRequired</span></span>
<span data-ttu-id="c27d6-166">Flag per applicare SubscriptionRequired per le richieste all'API.</span><span class="sxs-lookup"><span data-stu-id="c27d6-166">Flag to enforce SubscriptionRequired for requests to the Api.</span></span> <span data-ttu-id="c27d6-167">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c27d6-167">This parameter is optional.</span></span>

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

### <span data-ttu-id="c27d6-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27d6-168">CommonParameters</span></span>
<span data-ttu-id="c27d6-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c27d6-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27d6-170">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c27d6-170">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27d6-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c27d6-171">INPUTS</span></span>

### <span data-ttu-id="c27d6-172">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c27d6-172">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c27d6-173">System. String</span><span class="sxs-lookup"><span data-stu-id="c27d6-173">System.String</span></span>

### <span data-ttu-id="c27d6-174">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-174">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="c27d6-175">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="c27d6-175">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="c27d6-176">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c27d6-176">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c27d6-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c27d6-177">OUTPUTS</span></span>

### <span data-ttu-id="c27d6-178">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-178">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="c27d6-179">Note</span><span class="sxs-lookup"><span data-stu-id="c27d6-179">NOTES</span></span>

## <span data-ttu-id="c27d6-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c27d6-180">RELATED LINKS</span></span>

[<span data-ttu-id="c27d6-181">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-181">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="c27d6-182">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-182">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="c27d6-183">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-183">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="c27d6-184">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-184">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="c27d6-185">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c27d6-185">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


