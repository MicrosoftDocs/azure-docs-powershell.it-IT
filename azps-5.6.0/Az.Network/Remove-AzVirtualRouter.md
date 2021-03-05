---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6def67720ee11a2057267845ef458d0759aec589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005934"
---
# <span data-ttu-id="a3b5c-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a3b5c-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="a3b5c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3b5c-102">SYNOPSIS</span></span>
<span data-ttu-id="a3b5c-103">Elimina un Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="a3b5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3b5c-104">SYNTAX</span></span>

### <span data-ttu-id="a3b5c-105">VirtualRouterNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a3b5c-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b5c-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b5c-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3b5c-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3b5c-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3b5c-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a3b5c-108">DESCRIPTION</span></span>
<span data-ttu-id="a3b5c-109">Il cmdlet **Remove-AzVirtualRouter** elimina un Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a3b5c-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="a3b5c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3b5c-110">EXAMPLES</span></span>

### <span data-ttu-id="a3b5c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3b5c-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="a3b5c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a3b5c-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="a3b5c-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a3b5c-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="a3b5c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3b5c-114">PARAMETERS</span></span>

### <span data-ttu-id="a3b5c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3b5c-115">-AsJob</span></span>
<span data-ttu-id="a3b5c-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a3b5c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3b5c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3b5c-117">-DefaultProfile</span></span>
<span data-ttu-id="a3b5c-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3b5c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a3b5c-119">-Force</span></span>
<span data-ttu-id="a3b5c-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="a3b5c-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a3b5c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a3b5c-121">-InputObject</span></span>
<span data-ttu-id="a3b5c-122">Oggetto di input del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b5c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3b5c-123">-PassThru</span></span>
<span data-ttu-id="a3b5c-124">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="a3b5c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3b5c-125">-ResourceGroupName</span></span>
<span data-ttu-id="a3b5c-126">Nome del gruppo di risorse del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b5c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a3b5c-127">-ResourceId</span></span>
<span data-ttu-id="a3b5c-128">ID della risorsa del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b5c-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="a3b5c-129">-RouterName</span></span>
<span data-ttu-id="a3b5c-130">Il nome del router virtuale.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3b5c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3b5c-131">-Confirm</span></span>
<span data-ttu-id="a3b5c-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3b5c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3b5c-133">-WhatIf</span></span>
<span data-ttu-id="a3b5c-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3b5c-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3b5c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3b5c-136">CommonParameters</span></span>
<span data-ttu-id="a3b5c-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3b5c-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a3b5c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3b5c-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="a3b5c-139">INPUTS</span></span>

### <span data-ttu-id="a3b5c-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a3b5c-140">System.String</span></span>

### <span data-ttu-id="a3b5c-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="a3b5c-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="a3b5c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3b5c-142">OUTPUTS</span></span>

### <span data-ttu-id="a3b5c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a3b5c-143">System.Boolean</span></span>

## <span data-ttu-id="a3b5c-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="a3b5c-144">NOTES</span></span>

## <span data-ttu-id="a3b5c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3b5c-145">RELATED LINKS</span></span>
