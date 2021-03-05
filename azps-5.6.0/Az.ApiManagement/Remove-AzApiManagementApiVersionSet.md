---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 8f505496bc94d7cd0fc4ca69e6a81324a82871d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001950"
---
# <span data-ttu-id="f3130-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3130-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="f3130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3130-102">SYNOPSIS</span></span>
<span data-ttu-id="f3130-103">Rimuove un particolare set di versioni api</span><span class="sxs-lookup"><span data-stu-id="f3130-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="f3130-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3130-104">SYNTAX</span></span>

### <span data-ttu-id="f3130-105">ExpandedParameter (Default)</span><span class="sxs-lookup"><span data-stu-id="f3130-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3130-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f3130-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3130-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f3130-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3130-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3130-108">DESCRIPTION</span></span>

<span data-ttu-id="f3130-109">Il cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** rimuove un set di versioni dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="f3130-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="f3130-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3130-110">EXAMPLES</span></span>

### <span data-ttu-id="f3130-111">Esempio 1: Rimuovere un set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="f3130-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="f3130-112">Questo comando rimuove il set di versioni dell'API con il valore ApiVersionSetId specificato.</span><span class="sxs-lookup"><span data-stu-id="f3130-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="f3130-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3130-113">PARAMETERS</span></span>

### <span data-ttu-id="f3130-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="f3130-114">-ApiVersionSetId</span></span>
<span data-ttu-id="f3130-115">Identificatore del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="f3130-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="f3130-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3130-116">This parameter is required.</span></span>

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

### <span data-ttu-id="f3130-117">-Context</span><span class="sxs-lookup"><span data-stu-id="f3130-117">-Context</span></span>
<span data-ttu-id="f3130-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f3130-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f3130-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3130-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f3130-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3130-120">-DefaultProfile</span></span>
<span data-ttu-id="f3130-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3130-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3130-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3130-122">-InputObject</span></span>
<span data-ttu-id="f3130-123">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f3130-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="f3130-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3130-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f3130-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3130-125">-PassThru</span></span>
<span data-ttu-id="f3130-126">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="f3130-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="f3130-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f3130-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="f3130-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3130-128">-ResourceId</span></span>
<span data-ttu-id="f3130-129">Arm ResourceId di ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="f3130-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="f3130-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f3130-130">This parameter is required.</span></span>

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

### <span data-ttu-id="f3130-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3130-131">-Confirm</span></span>
<span data-ttu-id="f3130-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3130-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3130-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3130-133">-WhatIf</span></span>
<span data-ttu-id="f3130-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3130-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3130-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3130-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3130-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3130-136">CommonParameters</span></span>
<span data-ttu-id="f3130-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3130-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3130-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3130-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3130-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3130-139">INPUTS</span></span>

### <span data-ttu-id="f3130-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f3130-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f3130-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3130-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="f3130-142">System.String</span><span class="sxs-lookup"><span data-stu-id="f3130-142">System.String</span></span>

## <span data-ttu-id="f3130-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3130-143">OUTPUTS</span></span>

### <span data-ttu-id="f3130-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f3130-144">System.Boolean</span></span>

## <span data-ttu-id="f3130-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3130-145">NOTES</span></span>

## <span data-ttu-id="f3130-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3130-146">RELATED LINKS</span></span>

[<span data-ttu-id="f3130-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3130-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="f3130-148">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3130-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="f3130-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="f3130-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)