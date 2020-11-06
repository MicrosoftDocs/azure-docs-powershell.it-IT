---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515835"
---
# <span data-ttu-id="0fba7-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0fba7-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="0fba7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fba7-102">SYNOPSIS</span></span>
<span data-ttu-id="0fba7-103">Imposta i dettagli dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="0fba7-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fba7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fba7-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0fba7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fba7-105">DESCRIPTION</span></span>
<span data-ttu-id="0fba7-106">Il cmdlet **set-AzureRmApiManagementOperation** imposta i dettagli dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="0fba7-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="0fba7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fba7-107">EXAMPLES</span></span>

### <span data-ttu-id="0fba7-108">Esempio 1: impostare i dettagli dell'operazione</span><span class="sxs-lookup"><span data-stu-id="0fba7-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="0fba7-109">Questo comando imposta i dettagli dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="0fba7-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="0fba7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fba7-110">PARAMETERS</span></span>

### <span data-ttu-id="0fba7-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0fba7-111">-ApiId</span></span>
<span data-ttu-id="0fba7-112">Specifica l'identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="0fba7-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="0fba7-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0fba7-113">-Context</span></span>
<span data-ttu-id="0fba7-114">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="0fba7-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="0fba7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fba7-115">-DefaultProfile</span></span>
<span data-ttu-id="0fba7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0fba7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="0fba7-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fba7-117">-Description</span></span>
<span data-ttu-id="0fba7-118">Specifica la descrizione della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="0fba7-118">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="0fba7-119">-Method</span><span class="sxs-lookup"><span data-stu-id="0fba7-119">-Method</span></span>
<span data-ttu-id="0fba7-120">Specifica il metodo HTTP della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="0fba7-120">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="0fba7-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0fba7-121">-Name</span></span>
<span data-ttu-id="0fba7-122">Specifica il nome visualizzato della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="0fba7-122">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="0fba7-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="0fba7-123">-OperationId</span></span>
<span data-ttu-id="0fba7-124">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="0fba7-124">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="0fba7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fba7-125">-PassThru</span></span>
<span data-ttu-id="0fba7-126">PassThru</span><span class="sxs-lookup"><span data-stu-id="0fba7-126">passthru</span></span>

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

### <span data-ttu-id="0fba7-127">-Request</span><span class="sxs-lookup"><span data-stu-id="0fba7-127">-Request</span></span>
<span data-ttu-id="0fba7-128">Specifica i dettagli delle richieste di operazione.</span><span class="sxs-lookup"><span data-stu-id="0fba7-128">Specifies the operation request details.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fba7-129">-Risposte</span><span class="sxs-lookup"><span data-stu-id="0fba7-129">-Responses</span></span>
<span data-ttu-id="0fba7-130">Specifica una matrice di possibili risposte alle operazioni.</span><span class="sxs-lookup"><span data-stu-id="0fba7-130">Specifies an array of possible operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fba7-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="0fba7-131">-TemplateParameters</span></span>
<span data-ttu-id="0fba7-132">Specifica una matrice o parametri definiti nel parametro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="0fba7-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="0fba7-133">Se non specifichi un valore, verrà generato un valore predefinito basato su UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="0fba7-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="0fba7-134">Usa il parametro per fornire altri dettagli su parametri come descrizione, tipo e altri valori possibili.</span><span class="sxs-lookup"><span data-stu-id="0fba7-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fba7-135">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="0fba7-135">-UrlTemplate</span></span>
<span data-ttu-id="0fba7-136">Specifica il modello di URL.</span><span class="sxs-lookup"><span data-stu-id="0fba7-136">Specifies the URL template.</span></span>
<span data-ttu-id="0fba7-137">Ad esempio: Customers/{CID}/Orders/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="0fba7-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="0fba7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fba7-138">CommonParameters</span></span>
<span data-ttu-id="0fba7-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fba7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fba7-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fba7-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fba7-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fba7-141">INPUTS</span></span>

### <span data-ttu-id="0fba7-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="0fba7-142">None</span></span>
<span data-ttu-id="0fba7-143">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="0fba7-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fba7-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fba7-144">OUTPUTS</span></span>

### <span data-ttu-id="0fba7-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0fba7-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="0fba7-146">Note</span><span class="sxs-lookup"><span data-stu-id="0fba7-146">NOTES</span></span>

## <span data-ttu-id="0fba7-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fba7-147">RELATED LINKS</span></span>

[<span data-ttu-id="0fba7-148">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0fba7-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0fba7-149">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0fba7-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="0fba7-150">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="0fba7-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


