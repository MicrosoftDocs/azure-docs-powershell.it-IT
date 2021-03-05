---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: f1c8589663008b0ebc640a052199a11c82d3b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996307"
---
# <span data-ttu-id="57bc2-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="57bc2-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="57bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="57bc2-103">Elimina un gruppo IpGroup di Azure.</span><span class="sxs-lookup"><span data-stu-id="57bc2-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="57bc2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57bc2-104">SYNTAX</span></span>

### <span data-ttu-id="57bc2-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="57bc2-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57bc2-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="57bc2-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57bc2-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="57bc2-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57bc2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="57bc2-108">DESCRIPTION</span></span>
<span data-ttu-id="57bc2-109">Il cmdlet **Remove-AzIpGroup** elimina un gruppo IpGroup di Azure</span><span class="sxs-lookup"><span data-stu-id="57bc2-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="57bc2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57bc2-110">EXAMPLES</span></span>

### <span data-ttu-id="57bc2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="57bc2-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="57bc2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="57bc2-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="57bc2-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="57bc2-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="57bc2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57bc2-114">PARAMETERS</span></span>

### <span data-ttu-id="57bc2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57bc2-115">-AsJob</span></span>
<span data-ttu-id="57bc2-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="57bc2-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57bc2-117">-DefaultProfile</span></span>
<span data-ttu-id="57bc2-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="57bc2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="57bc2-119">-Force</span></span>
<span data-ttu-id="57bc2-120">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="57bc2-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="57bc2-121">-IpGroup</span></span>
<span data-ttu-id="57bc2-122">Oggetto di input ipGroup.</span><span class="sxs-lookup"><span data-stu-id="57bc2-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="57bc2-123">-Name</span></span>
<span data-ttu-id="57bc2-124">Nome del gruppo ipgroup.</span><span class="sxs-lookup"><span data-stu-id="57bc2-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57bc2-125">-PassThru</span></span>
<span data-ttu-id="57bc2-126">Restituisce un oggetto che rappresenta l'elemento su cui viene eseguita l'operazione.</span><span class="sxs-lookup"><span data-stu-id="57bc2-126">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57bc2-127">-ResourceGroupName</span></span>
<span data-ttu-id="57bc2-128">Nome del gruppo di risorse dell'ipgroup.</span><span class="sxs-lookup"><span data-stu-id="57bc2-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57bc2-129">-ResourceId</span></span>
<span data-ttu-id="57bc2-130">ID della risorsa ipgroup.</span><span class="sxs-lookup"><span data-stu-id="57bc2-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57bc2-131">-Confirm</span></span>
<span data-ttu-id="57bc2-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57bc2-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57bc2-133">-WhatIf</span></span>
<span data-ttu-id="57bc2-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57bc2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57bc2-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="57bc2-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57bc2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57bc2-136">CommonParameters</span></span>
<span data-ttu-id="57bc2-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57bc2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57bc2-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="57bc2-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57bc2-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="57bc2-139">INPUTS</span></span>

### <span data-ttu-id="57bc2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="57bc2-140">System.String</span></span>

### <span data-ttu-id="57bc2-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="57bc2-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="57bc2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57bc2-142">OUTPUTS</span></span>

### <span data-ttu-id="57bc2-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="57bc2-143">System.Boolean</span></span>

## <span data-ttu-id="57bc2-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="57bc2-144">NOTES</span></span>

## <span data-ttu-id="57bc2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57bc2-145">RELATED LINKS</span></span>
