---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 92848cb2daa0976d8206549fc16d1a6f039199a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022136"
---
# <span data-ttu-id="ecc39-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ecc39-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="ecc39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ecc39-102">SYNOPSIS</span></span>
<span data-ttu-id="ecc39-103">Imposta i dettagli dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="ecc39-103">Sets API operation details.</span></span>

## <span data-ttu-id="ecc39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecc39-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecc39-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecc39-105">DESCRIPTION</span></span>
<span data-ttu-id="ecc39-106">Il cmdlet **set-AzApiManagementOperation** imposta i dettagli dell'operazione API.</span><span class="sxs-lookup"><span data-stu-id="ecc39-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="ecc39-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecc39-107">EXAMPLES</span></span>

### <span data-ttu-id="ecc39-108">Esempio 1: impostare i dettagli dell'operazione</span><span class="sxs-lookup"><span data-stu-id="ecc39-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="ecc39-109">Questo comando imposta i dettagli dell'operazione per la gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="ecc39-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="ecc39-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ecc39-110">PARAMETERS</span></span>

### <span data-ttu-id="ecc39-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ecc39-111">-ApiId</span></span>
<span data-ttu-id="ecc39-112">Specifica l'identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="ecc39-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="ecc39-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ecc39-113">-ApiRevision</span></span>
<span data-ttu-id="ecc39-114">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="ecc39-114">Identifier of API Revision.</span></span> <span data-ttu-id="ecc39-115">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="ecc39-115">This parameter is optional.</span></span> <span data-ttu-id="ecc39-116">Se non specificato, l'operazione verrà aggiornata nella revisione API attualmente attiva.</span><span class="sxs-lookup"><span data-stu-id="ecc39-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="ecc39-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ecc39-117">-Context</span></span>
<span data-ttu-id="ecc39-118">Specifica un'istanza di **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="ecc39-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="ecc39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecc39-119">-DefaultProfile</span></span>
<span data-ttu-id="ecc39-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecc39-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ecc39-121">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ecc39-121">-Description</span></span>
<span data-ttu-id="ecc39-122">Specifica la descrizione della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="ecc39-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="ecc39-123">-Method</span><span class="sxs-lookup"><span data-stu-id="ecc39-123">-Method</span></span>
<span data-ttu-id="ecc39-124">Specifica il metodo HTTP della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="ecc39-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="ecc39-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecc39-125">-Name</span></span>
<span data-ttu-id="ecc39-126">Specifica il nome visualizzato della nuova operazione.</span><span class="sxs-lookup"><span data-stu-id="ecc39-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="ecc39-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ecc39-127">-OperationId</span></span>
<span data-ttu-id="ecc39-128">Specifica l'identificatore dell'operazione esistente.</span><span class="sxs-lookup"><span data-stu-id="ecc39-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="ecc39-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ecc39-129">-PassThru</span></span>
<span data-ttu-id="ecc39-130">PassThru</span><span class="sxs-lookup"><span data-stu-id="ecc39-130">passthru</span></span>

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

### <span data-ttu-id="ecc39-131">-Request</span><span class="sxs-lookup"><span data-stu-id="ecc39-131">-Request</span></span>
<span data-ttu-id="ecc39-132">Specifica i dettagli delle richieste di operazione.</span><span class="sxs-lookup"><span data-stu-id="ecc39-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="ecc39-133">-Risposte</span><span class="sxs-lookup"><span data-stu-id="ecc39-133">-Responses</span></span>
<span data-ttu-id="ecc39-134">Specifica una matrice di possibili risposte alle operazioni.</span><span class="sxs-lookup"><span data-stu-id="ecc39-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="ecc39-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="ecc39-135">-TemplateParameters</span></span>
<span data-ttu-id="ecc39-136">Specifica una matrice o parametri definiti nel parametro *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="ecc39-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="ecc39-137">Se non specifichi un valore, verrà generato un valore predefinito basato su UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="ecc39-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="ecc39-138">Usa il parametro per fornire altri dettagli su parametri come descrizione, tipo e altri valori possibili.</span><span class="sxs-lookup"><span data-stu-id="ecc39-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="ecc39-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="ecc39-139">-UrlTemplate</span></span>
<span data-ttu-id="ecc39-140">Specifica il modello di URL.</span><span class="sxs-lookup"><span data-stu-id="ecc39-140">Specifies the URL template.</span></span>
<span data-ttu-id="ecc39-141">Ad esempio: Customers/{CID}/Orders/{OID}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="ecc39-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="ecc39-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ecc39-142">-Confirm</span></span>
<span data-ttu-id="ecc39-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecc39-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc39-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecc39-144">-WhatIf</span></span>
<span data-ttu-id="ecc39-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecc39-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecc39-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecc39-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecc39-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecc39-147">CommonParameters</span></span>
<span data-ttu-id="ecc39-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecc39-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecc39-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecc39-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecc39-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ecc39-150">INPUTS</span></span>

### <span data-ttu-id="ecc39-151">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ecc39-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ecc39-152">System. String</span><span class="sxs-lookup"><span data-stu-id="ecc39-152">System.String</span></span>

### <span data-ttu-id="ecc39-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="ecc39-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="ecc39-154">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="ecc39-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="ecc39-155">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="ecc39-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="ecc39-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ecc39-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ecc39-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecc39-157">OUTPUTS</span></span>

### <span data-ttu-id="ecc39-158">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ecc39-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="ecc39-159">Note</span><span class="sxs-lookup"><span data-stu-id="ecc39-159">NOTES</span></span>

## <span data-ttu-id="ecc39-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecc39-160">RELATED LINKS</span></span>

[<span data-ttu-id="ecc39-161">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ecc39-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="ecc39-162">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ecc39-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="ecc39-163">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="ecc39-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


