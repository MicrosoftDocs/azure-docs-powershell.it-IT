---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerInstance.dll-Help.xml
Module Name: Az.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerinstance/remove-azcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerInstance/ContainerInstance/help/Remove-AzContainerGroup.md
ms.openlocfilehash: fb9b2c23618d731f6f107f755ca6ef41dfe439ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684650"
---
# <span data-ttu-id="1822e-101">Remove-AzContainerGroup</span><span class="sxs-lookup"><span data-stu-id="1822e-101">Remove-AzContainerGroup</span></span>

## <span data-ttu-id="1822e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1822e-102">SYNOPSIS</span></span>
<span data-ttu-id="1822e-103">Rimuove un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="1822e-103">Removes a container group.</span></span>

## <span data-ttu-id="1822e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1822e-104">SYNTAX</span></span>

### <span data-ttu-id="1822e-105">RemoveContainerGroupByResourceGroupAndNameParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1822e-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1822e-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="1822e-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzContainerGroup -InputObject <PSContainerGroup> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1822e-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="1822e-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1822e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1822e-108">DESCRIPTION</span></span>
<span data-ttu-id="1822e-109">Il cmdlet **Remove-AzContainerGroup** rimuove un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="1822e-109">The **Remove-AzContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="1822e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1822e-110">EXAMPLES</span></span>

### <span data-ttu-id="1822e-111">Esempio 1: rimuove un gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="1822e-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="1822e-112">Questo comando rimuove il gruppo di contenitori specificato.</span><span class="sxs-lookup"><span data-stu-id="1822e-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="1822e-113">Esempio 2: rimuove un gruppo di contenitori per piping</span><span class="sxs-lookup"><span data-stu-id="1822e-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="1822e-114">Questo comando rimuove un gruppo di contenitori per piping.</span><span class="sxs-lookup"><span data-stu-id="1822e-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="1822e-115">Esempio 3: rimuove un gruppo di contenitori in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1822e-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzContainerGroup
```

<span data-ttu-id="1822e-116">Questo comando rimuove un gruppo di contenitori per ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1822e-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="1822e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1822e-117">PARAMETERS</span></span>

### <span data-ttu-id="1822e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1822e-118">-DefaultProfile</span></span>
<span data-ttu-id="1822e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1822e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1822e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1822e-120">-InputObject</span></span>
<span data-ttu-id="1822e-121">Gruppo contenitore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="1822e-121">The container group to remove.</span></span>

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

### <span data-ttu-id="1822e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1822e-122">-Name</span></span>
<span data-ttu-id="1822e-123">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="1822e-123">The container group name.</span></span>

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

### <span data-ttu-id="1822e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1822e-124">-PassThru</span></span>
<span data-ttu-id="1822e-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1822e-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1822e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1822e-126">-ResourceGroupName</span></span>
<span data-ttu-id="1822e-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1822e-127">The resource group name.</span></span>

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

### <span data-ttu-id="1822e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1822e-128">-ResourceId</span></span>
<span data-ttu-id="1822e-129">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1822e-129">The resource id.</span></span>

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

### <span data-ttu-id="1822e-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1822e-130">-Confirm</span></span>
<span data-ttu-id="1822e-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1822e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1822e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1822e-132">-WhatIf</span></span>
<span data-ttu-id="1822e-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1822e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1822e-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1822e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1822e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1822e-135">CommonParameters</span></span>
<span data-ttu-id="1822e-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1822e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1822e-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1822e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1822e-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1822e-138">INPUTS</span></span>

### <span data-ttu-id="1822e-139">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="1822e-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

### <span data-ttu-id="1822e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1822e-140">System.String</span></span>

## <span data-ttu-id="1822e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1822e-141">OUTPUTS</span></span>

### <span data-ttu-id="1822e-142">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="1822e-142">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="1822e-143">Note</span><span class="sxs-lookup"><span data-stu-id="1822e-143">NOTES</span></span>

## <span data-ttu-id="1822e-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1822e-144">RELATED LINKS</span></span>
