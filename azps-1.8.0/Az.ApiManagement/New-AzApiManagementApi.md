---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 664CF009-FC52-4F1B-933B-3DEBD05AC8C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApi.md
ms.openlocfilehash: 43793ef7d1d3f9a4e5e63687e1eaf785d237e86b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673608"
---
# <span data-ttu-id="f741e-101">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f741e-101">New-AzApiManagementApi</span></span>

## <span data-ttu-id="f741e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f741e-102">SYNOPSIS</span></span>
<span data-ttu-id="f741e-103">Crea un'API.</span><span class="sxs-lookup"><span data-stu-id="f741e-103">Creates an API.</span></span>

## <span data-ttu-id="f741e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f741e-104">SYNTAX</span></span>

```
New-AzApiManagementApi -Context <PsApiManagementContext> [-ApiId <String>] -Name <String>
 [-Description <String>] -ServiceUrl <String> -Path <String> -Protocols <PsApiManagementSchema[]>
 [-AuthorizationServerId <String>] [-AuthorizationScope <String>] [-SubscriptionKeyHeaderName <String>]
 [-SubscriptionKeyQueryParamName <String>] [-ProductIds <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f741e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f741e-105">DESCRIPTION</span></span>
<span data-ttu-id="f741e-106">Il cmdlet **New-AzApiManagementApi** crea un'API di gestione delle API di Azure.</span><span class="sxs-lookup"><span data-stu-id="f741e-106">The **New-AzApiManagementApi** cmdlet creates an Azure API Management API.</span></span>

## <span data-ttu-id="f741e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f741e-107">EXAMPLES</span></span>

### <span data-ttu-id="f741e-108">Esempio 1: creare un'API</span><span class="sxs-lookup"><span data-stu-id="f741e-108">Example 1: Create an API</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApi -Context $ApiMgmtContext -Name "Echo api" -ServiceUrl "https://contoso.com/apis/echo" -Protocols @("http", "https") -Path "testapi"
```

<span data-ttu-id="f741e-109">Questo comando crea un'API denominata EchoApi con l'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="f741e-109">This command creates an API named EchoApi with the specified URL.</span></span>

## <span data-ttu-id="f741e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f741e-110">PARAMETERS</span></span>

### <span data-ttu-id="f741e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f741e-111">-ApiId</span></span>
<span data-ttu-id="f741e-112">Specifica l'ID dell'API da creare.</span><span class="sxs-lookup"><span data-stu-id="f741e-112">Specifies the ID of the API to create.</span></span>
<span data-ttu-id="f741e-113">Se non specifichi questo parametro, questo cmdlet genera un ID per te.</span><span class="sxs-lookup"><span data-stu-id="f741e-113">If you do not specify this parameter, this cmdlet generates an ID for you.</span></span>

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

### <span data-ttu-id="f741e-114">-AuthorizationScope</span><span class="sxs-lookup"><span data-stu-id="f741e-114">-AuthorizationScope</span></span>
<span data-ttu-id="f741e-115">Specifica l'ambito delle operazioni OAuth.</span><span class="sxs-lookup"><span data-stu-id="f741e-115">Specifies the OAuth operations scope.</span></span>
<span data-ttu-id="f741e-116">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="f741e-116">The default value is $Null.</span></span>

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

### <span data-ttu-id="f741e-117">-AuthorizationServerId</span><span class="sxs-lookup"><span data-stu-id="f741e-117">-AuthorizationServerId</span></span>
<span data-ttu-id="f741e-118">Specifica l'ID del server di autorizzazione OAuth.</span><span class="sxs-lookup"><span data-stu-id="f741e-118">Specifies the OAuth authorization server ID.</span></span>
<span data-ttu-id="f741e-119">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="f741e-119">The default value is $Null.</span></span>
<span data-ttu-id="f741e-120">Devi specificare questo parametro se *AuthorizationScope* è specificato.</span><span class="sxs-lookup"><span data-stu-id="f741e-120">You must specify this parameter if *AuthorizationScope* is specified.</span></span>

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

### <span data-ttu-id="f741e-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f741e-121">-Context</span></span>
<span data-ttu-id="f741e-122">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f741e-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f741e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f741e-123">-DefaultProfile</span></span>
<span data-ttu-id="f741e-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f741e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f741e-125">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f741e-125">-Description</span></span>
<span data-ttu-id="f741e-126">Specifica una descrizione per l'API Web.</span><span class="sxs-lookup"><span data-stu-id="f741e-126">Specifies a description for the web API.</span></span>

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

### <span data-ttu-id="f741e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f741e-127">-Name</span></span>
<span data-ttu-id="f741e-128">Specifica il nome dell'API Web.</span><span class="sxs-lookup"><span data-stu-id="f741e-128">Specifies the name of the web API.</span></span>
<span data-ttu-id="f741e-129">Questo è il nome pubblico dell'API come viene visualizzato nei portali per sviluppatori e amministratori.</span><span class="sxs-lookup"><span data-stu-id="f741e-129">This is the public name of the API as it appears on the developer and admin portals.</span></span>

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

### <span data-ttu-id="f741e-130">-Path</span><span class="sxs-lookup"><span data-stu-id="f741e-130">-Path</span></span>
<span data-ttu-id="f741e-131">Specifica il percorso dell'API Web, che è l'ultima parte dell'URL pubblico dell'API e corrisponde al campo suffisso URL API Web nel portale di amministrazione.</span><span class="sxs-lookup"><span data-stu-id="f741e-131">Specifies the web API path, which is the last part of the API's public URL and corresponds to the Web API URL suffix field in the admin portal.</span></span>
<span data-ttu-id="f741e-132">Questo URL viene usato dagli utenti dell'API per inviare richieste al servizio Web e deve essere di una lunghezza di 400 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f741e-132">This URL is used by API consumers to send requests to the web service, and must be one to 400 characters long.</span></span>
<span data-ttu-id="f741e-133">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="f741e-133">The default value is $Null.</span></span>

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

### <span data-ttu-id="f741e-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f741e-134">-ProductIds</span></span>
<span data-ttu-id="f741e-135">Specifica una matrice di ID prodotto a cui aggiungere la nuova API.</span><span class="sxs-lookup"><span data-stu-id="f741e-135">Specifies an array of product IDs to which to add the new API.</span></span>

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

### <span data-ttu-id="f741e-136">-Protocolli</span><span class="sxs-lookup"><span data-stu-id="f741e-136">-Protocols</span></span>
<span data-ttu-id="f741e-137">Specifica una matrice di protocolli API Web.</span><span class="sxs-lookup"><span data-stu-id="f741e-137">Specifies an array of web API protocols.</span></span>
<span data-ttu-id="f741e-138">I valori validi sono http, HTTPS.</span><span class="sxs-lookup"><span data-stu-id="f741e-138">Valid values are http, https.</span></span>
<span data-ttu-id="f741e-139">Questi sono i protocolli Web su cui l'API è resa disponibile.</span><span class="sxs-lookup"><span data-stu-id="f741e-139">These are the web protocols over which the API is made available.</span></span>
<span data-ttu-id="f741e-140">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="f741e-140">The default value is $Null.</span></span>

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

### <span data-ttu-id="f741e-141">-ServiceUrl</span><span class="sxs-lookup"><span data-stu-id="f741e-141">-ServiceUrl</span></span>
<span data-ttu-id="f741e-142">Specifica l'URL del servizio Web che espone l'API.</span><span class="sxs-lookup"><span data-stu-id="f741e-142">Specifies the URL of the web service that exposes the API.</span></span>
<span data-ttu-id="f741e-143">Questo URL viene usato solo dalla gestione delle API di Azure e non viene reso pubblico.</span><span class="sxs-lookup"><span data-stu-id="f741e-143">This URL is used only by Azure API Management, and is not made public.</span></span>
<span data-ttu-id="f741e-144">L'URL deve essere lungo uno-2000 caratteri.</span><span class="sxs-lookup"><span data-stu-id="f741e-144">The URL must be one to 2000 characters long.</span></span>

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

### <span data-ttu-id="f741e-145">-SubscriptionKeyHeaderName</span><span class="sxs-lookup"><span data-stu-id="f741e-145">-SubscriptionKeyHeaderName</span></span>
<span data-ttu-id="f741e-146">Specifica il nome dell'intestazione della chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f741e-146">Specifies the subscription key header name.</span></span>
<span data-ttu-id="f741e-147">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="f741e-147">The default value is $Null.</span></span>

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

### <span data-ttu-id="f741e-148">-SubscriptionKeyQueryParamName</span><span class="sxs-lookup"><span data-stu-id="f741e-148">-SubscriptionKeyQueryParamName</span></span>
<span data-ttu-id="f741e-149">Specifica il nome del parametro della stringa di query per la chiave di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f741e-149">Specifies the subscription key query string parameter name.</span></span>
<span data-ttu-id="f741e-150">Il valore predefinito è $Null.</span><span class="sxs-lookup"><span data-stu-id="f741e-150">The default value is $Null.</span></span>

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

### <span data-ttu-id="f741e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f741e-151">CommonParameters</span></span>
<span data-ttu-id="f741e-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f741e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f741e-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f741e-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f741e-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f741e-154">INPUTS</span></span>

### <span data-ttu-id="f741e-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f741e-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f741e-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f741e-156">System.String</span></span>

### <span data-ttu-id="f741e-157">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementSchema []</span><span class="sxs-lookup"><span data-stu-id="f741e-157">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSchema[]</span></span>

### <span data-ttu-id="f741e-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="f741e-158">System.String[]</span></span>

## <span data-ttu-id="f741e-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f741e-159">OUTPUTS</span></span>

### <span data-ttu-id="f741e-160">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f741e-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="f741e-161">Note</span><span class="sxs-lookup"><span data-stu-id="f741e-161">NOTES</span></span>

## <span data-ttu-id="f741e-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f741e-162">RELATED LINKS</span></span>

[<span data-ttu-id="f741e-163">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f741e-163">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="f741e-164">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f741e-164">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="f741e-165">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f741e-165">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="f741e-166">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f741e-166">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="f741e-167">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f741e-167">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


