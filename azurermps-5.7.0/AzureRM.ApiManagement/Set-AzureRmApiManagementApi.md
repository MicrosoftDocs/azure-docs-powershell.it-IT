---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 29CCF141-CC2F-4E11-8235-64025CFB5782
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementApi.md
ms.openlocfilehash: 6ab29738f181f6fece9d3b4cd679496a9add9bc5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518255"
---
# <span data-ttu-id="9af62-101">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9af62-101">Set-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="9af62-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9af62-102">SYNOPSIS</span></span>
<span data-ttu-id="9af62-103">Modifica un'API.</span><span class="sxs-lookup"><span data-stu-id="9af62-103">Modifies an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9af62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9af62-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> -Name <String>
 [-Description <String>] -ServiceUrl <String> [-Path <String>] -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9af62-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9af62-105">DESCRIPTION</span></span>
<span data-ttu-id="9af62-106">Il cmdlet **set-AzureRmApiManagementApi** modifica un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="9af62-106">The **Set-AzureRmApiManagementApi** cmdlet modifies an Azure API Management API.</span></span>

## <span data-ttu-id="9af62-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9af62-107">EXAMPLES</span></span>

### <span data-ttu-id="9af62-108">Esempio 1 modificare un'API</span><span class="sxs-lookup"><span data-stu-id="9af62-108">Example 1 Modify an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @('https') -Description "Responds with what was sent" -Path "echo"
```

## <span data-ttu-id="9af62-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9af62-109">PARAMETERS</span></span>

### <span data-ttu-id="9af62-110">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9af62-110">-ApiId</span></span>
<span data-ttu-id="9af62-111">Specifica l'ID dell'API da modificare.</span><span class="sxs-lookup"><span data-stu-id="9af62-111">Specifies the ID of the API to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-112">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="9af62-112">-AuthorizationScope</span></span>
<span data-ttu-id="9af62-113">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="9af62-113">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="9af62-114">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9af62-114">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-115">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="9af62-115">-AuthorizationServerId</span></span>
<span data-ttu-id="9af62-116">Specifica l'identificatore del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="9af62-116">Specifies the OAuth authorization server identifier.</span></span>
<span data-ttu-id="9af62-117">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9af62-117">The default value is $Null.</span></span>
<span data-ttu-id="9af62-118">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="9af62-118">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9af62-119">-Context</span></span>
<span data-ttu-id="9af62-120">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9af62-120">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9af62-121">-DefaultProfile</span></span>
<span data-ttu-id="9af62-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9af62-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9af62-123">-Description</span></span>
<span data-ttu-id="9af62-124">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="9af62-124">Specifies a description for the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="9af62-125">-Name</span></span>
<span data-ttu-id="9af62-126">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="9af62-126">Specifies the name of the web API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9af62-127">-PassThru</span></span>
<span data-ttu-id="9af62-128">PassThru</span><span class="sxs-lookup"><span data-stu-id="9af62-128">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-129">-Path</span><span class="sxs-lookup"><span data-stu-id="9af62-129">-Path</span></span>
<span data-ttu-id="9af62-130">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API.</span><span class="sxs-lookup"><span data-stu-id="9af62-130">Specifies the web API path, which is the last part of the API's public URL.</span></span>
<span data-ttu-id="9af62-131">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9af62-131">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="9af62-132">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9af62-132">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-133">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="9af62-133">-Protocols</span></span>
<span data-ttu-id="9af62-134">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="9af62-134">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="9af62-135">psdx_paramvalues http e HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9af62-135">psdx_paramvalues http and https.</span></span>
<span data-ttu-id="9af62-136">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="9af62-136">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="9af62-137">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9af62-137">The default value is $Null.</span></span>

```yaml
Type: PsApiManagementSchema[]
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-138">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="9af62-138">-ServiceUrl</span></span>
<span data-ttu-id="9af62-139">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="9af62-139">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="9af62-140">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="9af62-140">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="9af62-141">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="9af62-141">The URL must be one to 2000 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-142">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="9af62-142">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="9af62-143">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9af62-143">Specifies the name of the subscription key header.</span></span>
<span data-ttu-id="9af62-144">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9af62-144">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-145">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="9af62-145">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="9af62-146">Specifica il nome del parametro della stringa di query della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9af62-146">Specifies the name of the subscription key query string parameter.</span></span>
<span data-ttu-id="9af62-147">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="9af62-147">The default value is $Null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9af62-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af62-148">CommonParameters</span></span>
<span data-ttu-id="9af62-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af62-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af62-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af62-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af62-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9af62-151">INPUTS</span></span>

### <span data-ttu-id="9af62-152">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9af62-152">None</span></span>
<span data-ttu-id="9af62-153">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9af62-153">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9af62-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9af62-154">OUTPUTS</span></span>

### <span data-ttu-id="9af62-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9af62-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="9af62-156">Note</span><span class="sxs-lookup"><span data-stu-id="9af62-156">NOTES</span></span>

## <span data-ttu-id="9af62-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9af62-157">RELATED LINKS</span></span>

[<span data-ttu-id="9af62-158">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9af62-158">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="9af62-159">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9af62-159">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="9af62-160">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9af62-160">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="9af62-161">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9af62-161">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="9af62-162">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="9af62-162">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)


