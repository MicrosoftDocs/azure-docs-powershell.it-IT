---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344332"
---
# <span data-ttu-id="66f19-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="66f19-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="66f19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="66f19-102">SYNOPSIS</span></span>
<span data-ttu-id="66f19-103">Crea un'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-103">Creates an API management operation.</span></span>

## <span data-ttu-id="66f19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="66f19-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66f19-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66f19-105">DESCRIPTION</span></span>
<span data-ttu-id="66f19-106">Il cmdlet **New-AzApiManagementOperation** crea un'operazione API.</span><span class="sxs-lookup"><span data-stu-id="66f19-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="66f19-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="66f19-107">EXAMPLES</span></span>

### <span data-ttu-id="66f19-108">Esempio 1: creare un'operazione di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="66f19-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="66f19-109">Questo comando crea un'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="66f19-110">Esempio 2: creare un'operazione di gestione delle API con i dettagli di richiesta e risposta</span><span class="sxs-lookup"><span data-stu-id="66f19-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="66f19-111">Questo esempio crea un'operazione di gestione delle API con i dettagli di richiesta e risposta.</span><span class="sxs-lookup"><span data-stu-id="66f19-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="66f19-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="66f19-112">PARAMETERS</span></span>

### <span data-ttu-id="66f19-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="66f19-113">-ApiId</span></span>
<span data-ttu-id="66f19-114">Specifica l'identificatore dell'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="66f19-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="66f19-115">-ApiRevision</span></span>
<span data-ttu-id="66f19-116">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="66f19-116">Identifier of API Revision.</span></span> <span data-ttu-id="66f19-117">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="66f19-117">This parameter is optional.</span></span> <span data-ttu-id="66f19-118">Se non viene specificato, l'operazione verrà associata alla revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="66f19-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="66f19-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="66f19-119">-Context</span></span>
<span data-ttu-id="66f19-120">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="66f19-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66f19-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f19-121">-DefaultProfile</span></span>
<span data-ttu-id="66f19-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="66f19-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66f19-123">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="66f19-123">-Description</span></span>
<span data-ttu-id="66f19-124">Specifica la descrizione della nuova operazione API.</span><span class="sxs-lookup"><span data-stu-id="66f19-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="66f19-125">-Method</span><span class="sxs-lookup"><span data-stu-id="66f19-125">-Method</span></span>
<span data-ttu-id="66f19-126">Specifica il metodo HTTP della nuova operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="66f19-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="66f19-127">-Name</span></span>
<span data-ttu-id="66f19-128">Specifica il nome visualizzato della nuova operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="66f19-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="66f19-129">-OperationId</span></span>
<span data-ttu-id="66f19-130">Specifica l'identificatore dell'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="66f19-131">-Request</span><span class="sxs-lookup"><span data-stu-id="66f19-131">-Request</span></span>
<span data-ttu-id="66f19-132">Specifica i dettagli dell'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f19-133">-Risposte</span><span class="sxs-lookup"><span data-stu-id="66f19-133">-Responses</span></span>
<span data-ttu-id="66f19-134">Specifica una matrice di possibili risposte alle operazioni di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="66f19-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f19-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="66f19-135">-TemplateParameters</span></span>
<span data-ttu-id="66f19-136">Specifica una matrice di parametri definita nel parametro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="66f19-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="66f19-137">Se non specifichi questo parametro, verrà generato un valore predefinito basato su *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="66f19-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f19-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="66f19-138">-UrlTemplate</span></span>
<span data-ttu-id="66f19-139">Specifica il modello di URL.</span><span class="sxs-lookup"><span data-stu-id="66f19-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="66f19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f19-140">CommonParameters</span></span>
<span data-ttu-id="66f19-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66f19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f19-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="66f19-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f19-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="66f19-143">INPUTS</span></span>

### <span data-ttu-id="66f19-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="66f19-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="66f19-145">System. String</span><span class="sxs-lookup"><span data-stu-id="66f19-145">System.String</span></span>

### <span data-ttu-id="66f19-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="66f19-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="66f19-147">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="66f19-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="66f19-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="66f19-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="66f19-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="66f19-149">OUTPUTS</span></span>

### <span data-ttu-id="66f19-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="66f19-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="66f19-151">Note</span><span class="sxs-lookup"><span data-stu-id="66f19-151">NOTES</span></span>

## <span data-ttu-id="66f19-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="66f19-152">RELATED LINKS</span></span>

[<span data-ttu-id="66f19-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="66f19-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="66f19-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="66f19-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="66f19-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="66f19-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)


