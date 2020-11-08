---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020119"
---
# <span data-ttu-id="b0dca-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b0dca-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="b0dca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0dca-102">SYNOPSIS</span></span>
<span data-ttu-id="b0dca-103">Rimuove un set di versioni dell'API specifico</span><span class="sxs-lookup"><span data-stu-id="b0dca-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="b0dca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0dca-104">SYNTAX</span></span>

### <span data-ttu-id="b0dca-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0dca-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b0dca-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0dca-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b0dca-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0dca-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0dca-108">DESCRIPTION</span></span>

<span data-ttu-id="b0dca-109">Il cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** rimuove un set di versioni dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="b0dca-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="b0dca-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0dca-110">EXAMPLES</span></span>

### <span data-ttu-id="b0dca-111">Esempio 1: rimuovere un set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="b0dca-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="b0dca-112">Questo comando rimuove il set di versioni dell'API con il ApiVersionSetId specificato.</span><span class="sxs-lookup"><span data-stu-id="b0dca-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="b0dca-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0dca-113">PARAMETERS</span></span>

### <span data-ttu-id="b0dca-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="b0dca-114">-ApiVersionSetId</span></span>
<span data-ttu-id="b0dca-115">Identificatore del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="b0dca-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="b0dca-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0dca-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b0dca-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b0dca-117">-Context</span></span>
<span data-ttu-id="b0dca-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b0dca-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b0dca-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0dca-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0dca-120">-DefaultProfile</span></span>
<span data-ttu-id="b0dca-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0dca-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0dca-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0dca-122">-InputObject</span></span>
<span data-ttu-id="b0dca-123">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b0dca-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="b0dca-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0dca-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0dca-125">-PassThru</span></span>
<span data-ttu-id="b0dca-126">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b0dca-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b0dca-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b0dca-127">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0dca-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b0dca-128">-ResourceId</span></span>
<span data-ttu-id="b0dca-129">ResourceId ARM di ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="b0dca-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="b0dca-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b0dca-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0dca-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0dca-131">-Confirm</span></span>
<span data-ttu-id="b0dca-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0dca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0dca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0dca-133">-WhatIf</span></span>
<span data-ttu-id="b0dca-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0dca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0dca-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0dca-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0dca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0dca-136">CommonParameters</span></span>
<span data-ttu-id="b0dca-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0dca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0dca-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b0dca-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0dca-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0dca-139">INPUTS</span></span>

### <span data-ttu-id="b0dca-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b0dca-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0dca-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b0dca-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="b0dca-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b0dca-142">System.String</span></span>

## <span data-ttu-id="b0dca-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0dca-143">OUTPUTS</span></span>

### <span data-ttu-id="b0dca-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b0dca-144">System.Boolean</span></span>

## <span data-ttu-id="b0dca-145">Note</span><span class="sxs-lookup"><span data-stu-id="b0dca-145">NOTES</span></span>

## <span data-ttu-id="b0dca-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0dca-146">RELATED LINKS</span></span>

[<span data-ttu-id="b0dca-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b0dca-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b0dca-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b0dca-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="b0dca-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="b0dca-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)