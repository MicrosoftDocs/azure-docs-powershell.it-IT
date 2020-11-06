---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 545c1f57d269b8cdb36e006a07c754811e0f2b04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517192"
---
# <span data-ttu-id="9b8f8-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9b8f8-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="9b8f8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b8f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b8f8-103">Crea un'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b8f8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b8f8-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b8f8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b8f8-105">DESCRIPTION</span></span>
<span data-ttu-id="9b8f8-106">Il cmdlet **New-AzureRmApiManagementOperation** crea un'operazione API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="9b8f8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b8f8-107">EXAMPLES</span></span>

### <span data-ttu-id="9b8f8-108">Esempio 1: creare un'operazione di gestione delle API</span><span class="sxs-lookup"><span data-stu-id="9b8f8-108">Example 1: Create an API management operation</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="9b8f8-109">Questo comando crea un'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="9b8f8-110">Esempio 2: creare un'operazione di gestione delle API con i dettagli di richiesta e risposta</span><span class="sxs-lookup"><span data-stu-id="9b8f8-110">Example 2: Create an API management operation with request and response details</span></span>
```
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
New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="9b8f8-111">Questo esempio crea un'operazione di gestione delle API con i dettagli di richiesta e risposta.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="9b8f8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b8f8-112">PARAMETERS</span></span>

### <span data-ttu-id="9b8f8-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9b8f8-113">-ApiId</span></span>
<span data-ttu-id="9b8f8-114">Specifica l'identificatore dell'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="9b8f8-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9b8f8-115">-Context</span></span>
<span data-ttu-id="9b8f8-116">Specifica l'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9b8f8-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9b8f8-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b8f8-117">-Description</span></span>
<span data-ttu-id="9b8f8-118">Specifica la descrizione della nuova operazione API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-118">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="9b8f8-119">-Method</span><span class="sxs-lookup"><span data-stu-id="9b8f8-119">-Method</span></span>
<span data-ttu-id="9b8f8-120">Specifica il metodo HTTP della nuova operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-120">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="9b8f8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b8f8-121">-Name</span></span>
<span data-ttu-id="9b8f8-122">Specifica il nome visualizzato della nuova operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-122">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="9b8f8-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="9b8f8-123">-OperationId</span></span>
<span data-ttu-id="9b8f8-124">Specifica l'identificatore dell'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-124">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="9b8f8-125">-Request</span><span class="sxs-lookup"><span data-stu-id="9b8f8-125">-Request</span></span>
<span data-ttu-id="9b8f8-126">Specifica i dettagli dell'operazione di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-126">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="9b8f8-127">-Risposte</span><span class="sxs-lookup"><span data-stu-id="9b8f8-127">-Responses</span></span>
<span data-ttu-id="9b8f8-128">Specifica una matrice di possibili risposte alle operazioni di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-128">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="9b8f8-129">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="9b8f8-129">-TemplateParameters</span></span>
<span data-ttu-id="9b8f8-130">Specifica una matrice di parametri definita nel parametro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-130">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="9b8f8-131">Se non specifichi questo parametro, verrà generato un valore predefinito basato su *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-131">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="9b8f8-132">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="9b8f8-132">-UrlTemplate</span></span>
<span data-ttu-id="9b8f8-133">Specifica il modello di URL.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-133">Specifies the URL template.</span></span>

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

### <span data-ttu-id="9b8f8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b8f8-134">-DefaultProfile</span></span>
<span data-ttu-id="9b8f8-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b8f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b8f8-136">CommonParameters</span></span>
<span data-ttu-id="9b8f8-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b8f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b8f8-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b8f8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b8f8-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b8f8-139">INPUTS</span></span>

## <span data-ttu-id="9b8f8-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b8f8-140">OUTPUTS</span></span>

### <span data-ttu-id="9b8f8-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9b8f8-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="9b8f8-142">Note</span><span class="sxs-lookup"><span data-stu-id="9b8f8-142">NOTES</span></span>

## <span data-ttu-id="9b8f8-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b8f8-143">RELATED LINKS</span></span>

[<span data-ttu-id="9b8f8-144">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9b8f8-144">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="9b8f8-145">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9b8f8-145">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="9b8f8-146">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="9b8f8-146">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


