---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApi.md
ms.openlocfilehash: 75a6dbf480e8b2f2f3d9f7524db4e57e5ed88f69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687956"
---
# <span data-ttu-id="1b466-101">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b466-101">New-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="1b466-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b466-102">SYNOPSIS</span></span>
<span data-ttu-id="1b466-103">Crea un'API.</span><span class="sxs-lookup"><span data-stu-id="1b466-103">Creates an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b466-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b466-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b466-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b466-105">DESCRIPTION</span></span>
<span data-ttu-id="1b466-106">Il cmdlet **New-AzureRmApiManagementApi** crea un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b466-106">The **New-AzureRmApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="1b466-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b466-107">EXAMPLES</span></span>

### <span data-ttu-id="1b466-108">Esempio 1: creare un'API</span><span class="sxs-lookup"><span data-stu-id="1b466-108">Example 1: Create an API</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="1b466-109">Questo comando crea un'API denominata EchoApi con l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="1b466-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="1b466-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b466-110">PARAMETERS</span></span>

### <span data-ttu-id="1b466-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1b466-111">-ApiId</span></span>
<span data-ttu-id="1b466-112">Specifica l'ID dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="1b466-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="1b466-113">Se non specifichi questo parametro, questo cmdlet genera un ID per te.</span><span class="sxs-lookup"><span data-stu-id="1b466-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="1b466-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="1b466-114">-AuthorizationScope</span></span>
<span data-ttu-id="1b466-115">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="1b466-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="1b466-116">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="1b466-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b466-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="1b466-117">-AuthorizationServerId</span></span>
<span data-ttu-id="1b466-118">Specifica l'ID del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="1b466-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="1b466-119">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="1b466-119">The default value is $Null.</span></span>
<span data-ttu-id="1b466-120">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="1b466-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="1b466-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1b466-121">-Context</span></span>
<span data-ttu-id="1b466-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1b466-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1b466-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b466-123">-DefaultProfile</span></span>
<span data-ttu-id="1b466-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b466-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="1b466-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b466-125">-Description</span></span>
<span data-ttu-id="1b466-126">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="1b466-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="1b466-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b466-127">-Name</span></span>
<span data-ttu-id="1b466-128">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="1b466-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="1b466-129">Questo è il nome pubblico dell'API come viene visualizzato nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="1b466-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="1b466-130">-Path</span><span class="sxs-lookup"><span data-stu-id="1b466-130">-Path</span></span>
<span data-ttu-id="1b466-131">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API e corrisponde al campo suffisso URL API Web nel portale di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="1b466-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="1b466-132">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1b466-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="1b466-133">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="1b466-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b466-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1b466-134">-ProductIds</span></span>
<span data-ttu-id="1b466-135">Specifica una matrice di ID prodotto a cui aggiungere la nuova API.</span><span class="sxs-lookup"><span data-stu-id="1b466-135">Specifies an array of product IDs to which to add the new API.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b466-136">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="1b466-136">-Protocols</span></span>
<span data-ttu-id="1b466-137">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="1b466-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="1b466-138">I valori validi sono http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1b466-138">Valid values are http, https.</span></span>
<span data-ttu-id="1b466-139">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="1b466-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="1b466-140">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="1b466-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b466-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="1b466-141">-ServiceUrl</span></span>
<span data-ttu-id="1b466-142">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="1b466-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="1b466-143">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="1b466-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="1b466-144">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="1b466-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="1b466-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="1b466-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="1b466-146">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1b466-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="1b466-147">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="1b466-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b466-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="1b466-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="1b466-149">Specifica il nome del parametro della stringa di query per la chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1b466-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="1b466-150">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="1b466-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="1b466-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b466-151">CommonParameters</span></span>
<span data-ttu-id="1b466-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b466-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b466-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b466-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b466-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b466-154">INPUTS</span></span>

### <span data-ttu-id="1b466-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1b466-155">None</span></span>
<span data-ttu-id="1b466-156">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1b466-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1b466-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b466-157">OUTPUTS</span></span>

### <span data-ttu-id="1b466-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b466-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="1b466-159">Note</span><span class="sxs-lookup"><span data-stu-id="1b466-159">NOTES</span></span>

## <span data-ttu-id="1b466-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b466-160">RELATED LINKS</span></span>

[<span data-ttu-id="1b466-161">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b466-161">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="1b466-162">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b466-162">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="1b466-163">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b466-163">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="1b466-164">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b466-164">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="1b466-165">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="1b466-165">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


