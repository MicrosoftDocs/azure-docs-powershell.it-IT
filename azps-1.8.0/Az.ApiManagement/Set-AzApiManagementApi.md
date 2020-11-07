---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApi.md
ms.openlocfilehash: 190dfb075e16b6b7eaaa0cb6fafd0145b3211654
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852414"
---
# <span data-ttu-id="9929e-101">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-101">Set-AzApiManagementApi</span></span>

## <span data-ttu-id="9929e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9929e-102">SYNOPSIS</span></span>
<span data-ttu-id="9929e-103">Modifica un'API.</span><span class="sxs-lookup"><span data-stu-id="9929e-103">Modifies an API.</span></span>

## <span data-ttu-id="9929e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9929e-104">SYNTAX</span></span>

### <span data-ttu-id="9929e-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9929e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9929e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9929e-106">ByInputObject</span></span>
```
Set-AzApiManagementApi -InputObject <PsApiManagementApi> -Name <String> [-Description <String>]
 -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]> [-AuthorizationServerId <String>]
 [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>] [-SubscriptionKeyQueryParamName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9929e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9929e-107">DESCRIPTION</span></span>
<span data-ttu-id="9929e-108">Il cmdlet **set-AzApiManagementApi** modifica un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="9929e-108">The **Set-AzApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="9929e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9929e-109">EXAMPLES</span></span>

### <span data-ttu-id="9929e-110">Esempio 1 modificare un'API</span><span class="sxs-lookup"><span data-stu-id="9929e-110">Example 1 Modify an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="9929e-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9929e-111">PARAMETERS</span></span>

### <span data-ttu-id="9929e-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9929e-112">-ApiId</span></span>
<span data-ttu-id="9929e-113">Specifica l'ID dell'API da modificare.</span><span class="sxs-lookup"><span data-stu-id="9929e-113">Specifies the ID of the API to modify.</span></span>

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

### <span data-ttu-id="9929e-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9929e-114">-AuthorizationScope</span></span>
<span data-ttu-id="9929e-115">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="9929e-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="9929e-116">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9929e-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="9929e-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9929e-117">-AuthorizationServerId</span></span>
<span data-ttu-id="9929e-118">Specifica l'identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="9929e-118">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="9929e-119">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9929e-119">The default value is $Null.</span></span>
<span data-ttu-id="9929e-120">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="9929e-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="9929e-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9929e-121">-Context</span></span>
<span data-ttu-id="9929e-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9929e-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9929e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9929e-123">-DefaultProfile</span></span>
<span data-ttu-id="9929e-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9929e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9929e-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9929e-125">-Description</span></span>
<span data-ttu-id="9929e-126">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="9929e-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="9929e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9929e-127">-InputObject</span></span>
<span data-ttu-id="9929e-128">Istanza di PsApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="9929e-128">Instance of PsApiManagementApi.</span></span> <span data-ttu-id="9929e-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9929e-129">This parameter is required.</span></span>

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

### <span data-ttu-id="9929e-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="9929e-130">-Name</span></span>
<span data-ttu-id="9929e-131">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="9929e-131">Specifies the name of the web API.</span></span>

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

### <span data-ttu-id="9929e-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9929e-132">-PassThru</span></span>
<span data-ttu-id="9929e-133">PassThru</span><span class="sxs-lookup"><span data-stu-id="9929e-133">passthru</span></span>

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

### <span data-ttu-id="9929e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="9929e-134">-Path</span></span>
<span data-ttu-id="9929e-135">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="9929e-135">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="9929e-136">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9929e-136">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="9929e-137">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9929e-137">The default value is $Null.</span></span>

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

### <span data-ttu-id="9929e-138">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="9929e-138">-Protocols</span></span>
<span data-ttu-id="9929e-139">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="9929e-139">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="9929e-140">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9929e-140">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="9929e-141">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="9929e-141">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="9929e-142">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9929e-142">The default value is $Null.</span></span>

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

### <span data-ttu-id="9929e-143">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9929e-143">-ServiceUrl</span></span>
<span data-ttu-id="9929e-144">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="9929e-144">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="9929e-145">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="9929e-145">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="9929e-146">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9929e-146">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="9929e-147">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9929e-147">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9929e-148">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9929e-148">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="9929e-149">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9929e-149">The default value is $Null.</span></span>

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

### <span data-ttu-id="9929e-150">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9929e-150">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9929e-151">Specifica il nome del parametro della stringa di query della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9929e-151">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="9929e-152">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9929e-152">The default value is $Null.</span></span>

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

### <span data-ttu-id="9929e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9929e-153">CommonParameters</span></span>
<span data-ttu-id="9929e-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9929e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9929e-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9929e-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9929e-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9929e-156">INPUTS</span></span>

### <span data-ttu-id="9929e-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9929e-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9929e-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9929e-158">System.String</span></span>

### <span data-ttu-id="9929e-159">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

### <span data-ttu-id="9929e-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="9929e-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="9929e-161">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9929e-161">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9929e-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9929e-162">OUTPUTS</span></span>

### <span data-ttu-id="9929e-163">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9929e-164">Note</span><span class="sxs-lookup"><span data-stu-id="9929e-164">NOTES</span></span>

## <span data-ttu-id="9929e-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9929e-165">RELATED LINKS</span></span>

[<span data-ttu-id="9929e-166">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-166">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="9929e-167">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-167">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="9929e-168">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-168">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="9929e-169">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-169">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="9929e-170">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9929e-170">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)


