---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: 6f3b3006bfb51a90d5919c4cba2e2bc4295d4a76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181487"
---
# <span data-ttu-id="32305-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="32305-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="32305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32305-102">SYNOPSIS</span></span>
<span data-ttu-id="32305-103">Rimuove un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="32305-103">Removes a container group.</span></span>

## <span data-ttu-id="32305-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32305-104">SYNTAX</span></span>

### <span data-ttu-id="32305-105">RemoveContainerGroupByResourceGroupAndNameParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32305-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32305-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="32305-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32305-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="32305-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32305-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="32305-108">DESCRIPTION</span></span>
<span data-ttu-id="32305-109">Il cmdlet **Remove-AzContainerGroup** rimuove un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="32305-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="32305-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32305-110">EXAMPLES</span></span>

### <span data-ttu-id="32305-111">Esempio 1: Rimuovere un gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="32305-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="32305-112">Questo comando rimuove il gruppo di contenitori specificato.</span><span class="sxs-lookup"><span data-stu-id="32305-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="32305-113">Esempio 2: Rimuovere un gruppo di contenitori tramite piping</span><span class="sxs-lookup"><span data-stu-id="32305-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="32305-114">Questo comando rimuove un gruppo di contenitori tramite piping.</span><span class="sxs-lookup"><span data-stu-id="32305-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="32305-115">Esempio 3: rimuove un gruppo di contenitori in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="32305-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="32305-116">Questo comando rimuove un gruppo di contenitori in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="32305-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="32305-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32305-117">PARAMETERS</span></span>

### <span data-ttu-id="32305-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32305-118">-DefaultProfile</span></span>
<span data-ttu-id="32305-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32305-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32305-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32305-120">-InputObject</span></span>
<span data-ttu-id="32305-121">Il gruppo di contenitori da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="32305-121">The container group to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup
Parameter Sets: RemoveContainerGroupByPSContainerGroupParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32305-122">-Name</span><span class="sxs-lookup"><span data-stu-id="32305-122">-Name</span></span>
<span data-ttu-id="32305-123">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="32305-123">The container group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32305-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32305-124">-PassThru</span></span>
<span data-ttu-id="32305-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="32305-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="32305-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32305-126">-ResourceGroupName</span></span>
<span data-ttu-id="32305-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="32305-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceGroupAndNameParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32305-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32305-128">-ResourceId</span></span>
<span data-ttu-id="32305-129">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="32305-129">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveContainerGroupByResourceIdParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32305-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32305-130">-Confirm</span></span>
<span data-ttu-id="32305-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32305-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32305-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32305-132">-WhatIf</span></span>
<span data-ttu-id="32305-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32305-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32305-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32305-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32305-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32305-135">CommonParameters</span></span>
<span data-ttu-id="32305-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32305-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32305-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32305-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32305-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="32305-138">INPUTS</span></span>

### <span data-ttu-id="32305-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="32305-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="32305-140">System.String</span><span class="sxs-lookup"><span data-stu-id="32305-140">System.String</span></span>

## <span data-ttu-id="32305-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32305-141">OUTPUTS</span></span>

### <span data-ttu-id="32305-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="32305-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="32305-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="32305-143">NOTES</span></span>

## <span data-ttu-id="32305-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32305-144">RELATED LINKS</span></span>
