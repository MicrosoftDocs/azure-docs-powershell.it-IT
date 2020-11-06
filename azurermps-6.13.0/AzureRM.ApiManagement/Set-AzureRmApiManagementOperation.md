---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509432"
---
# <span data-ttu-id="c58f2-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c58f2-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="c58f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c58f2-102">SYNOPSIS</span></span>
<span data-ttu-id="c58f2-103">Imposta i dettagli dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="c58f2-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c58f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c58f2-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c58f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c58f2-105">DESCRIPTION</span></span>
<span data-ttu-id="c58f2-106">Il cmdlet **set-AzureRmApiManagementOperation** imposta i dettagli dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="c58f2-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="c58f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c58f2-107">EXAMPLES</span></span>

### <span data-ttu-id="c58f2-108">Esempio 1: impostare i dettagli dell'operazione</span><span class="sxs-lookup"><span data-stu-id="c58f2-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="c58f2-109">Questo comando imposta i dettagli dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="c58f2-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="c58f2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c58f2-110">PARAMETERS</span></span>

### <span data-ttu-id="c58f2-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c58f2-111">-ApiId</span></span>
<span data-ttu-id="c58f2-112">Specifica l'identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="c58f2-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="c58f2-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c58f2-113">-ApiRevision</span></span>
<span data-ttu-id="c58f2-114">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="c58f2-114">Identifier of API Revision.</span></span> <span data-ttu-id="c58f2-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c58f2-115">This parameter is optional.</span></span> <span data-ttu-id="c58f2-116">Se non specificato, l'operazione verrà aggiornata nella revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="c58f2-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="c58f2-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c58f2-117">-Context</span></span>
<span data-ttu-id="c58f2-118">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="c58f2-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="c58f2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c58f2-119">-DefaultProfile</span></span>
<span data-ttu-id="c58f2-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c58f2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c58f2-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="c58f2-121">-Description</span></span>
<span data-ttu-id="c58f2-122">Specifica la descrizione della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="c58f2-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="c58f2-123">-Method</span><span class="sxs-lookup"><span data-stu-id="c58f2-123">-Method</span></span>
<span data-ttu-id="c58f2-124">Specifica il metodo HTTP della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="c58f2-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="c58f2-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="c58f2-125">-Name</span></span>
<span data-ttu-id="c58f2-126">Specifica il nome visualizzato della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="c58f2-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="c58f2-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="c58f2-127">-OperationId</span></span>
<span data-ttu-id="c58f2-128">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="c58f2-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="c58f2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c58f2-129">-PassThru</span></span>
<span data-ttu-id="c58f2-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="c58f2-130">passthru</span></span>

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

### <span data-ttu-id="c58f2-131">-Request</span><span class="sxs-lookup"><span data-stu-id="c58f2-131">-Request</span></span>
<span data-ttu-id="c58f2-132">Specifica i dettagli delle richieste di operazione.</span><span class="sxs-lookup"><span data-stu-id="c58f2-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="c58f2-133">-Risposte</span><span class="sxs-lookup"><span data-stu-id="c58f2-133">-Responses</span></span>
<span data-ttu-id="c58f2-134">Specifica una matrice di possibili risposte alle operazioni.</span><span class="sxs-lookup"><span data-stu-id="c58f2-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="c58f2-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="c58f2-135">-TemplateParameters</span></span>
<span data-ttu-id="c58f2-136">Specifica una matrice o parametri definiti nel parametro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="c58f2-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="c58f2-137">Se non specifichi un valore, verrà generato un valore predefinito basato su UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="c58f2-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="c58f2-138">Usa il parametro per fornire altri dettagli su parametri come descrizione, tipo e altri valori possibili.</span><span class="sxs-lookup"><span data-stu-id="c58f2-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="c58f2-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="c58f2-139">-UrlTemplate</span></span>
<span data-ttu-id="c58f2-140">Specifica il modello di URL.</span><span class="sxs-lookup"><span data-stu-id="c58f2-140">Specifies the URL template.</span></span>
<span data-ttu-id="c58f2-141">Ad esempio: Customers/{CID}/Orders/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="c58f2-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="c58f2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58f2-142">CommonParameters</span></span>
<span data-ttu-id="c58f2-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c58f2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58f2-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c58f2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58f2-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c58f2-145">INPUTS</span></span>

### <span data-ttu-id="c58f2-146">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c58f2-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c58f2-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c58f2-147">System.String</span></span>

### <span data-ttu-id="c58f2-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="c58f2-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="c58f2-149">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="c58f2-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="c58f2-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="c58f2-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="c58f2-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c58f2-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c58f2-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c58f2-152">OUTPUTS</span></span>

### <span data-ttu-id="c58f2-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c58f2-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="c58f2-154">Note</span><span class="sxs-lookup"><span data-stu-id="c58f2-154">NOTES</span></span>

## <span data-ttu-id="c58f2-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c58f2-155">RELATED LINKS</span></span>

[<span data-ttu-id="c58f2-156">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c58f2-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="c58f2-157">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c58f2-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="c58f2-158">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="c58f2-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


