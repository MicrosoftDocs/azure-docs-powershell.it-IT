---
external help file: Microsoft.Azure.Commands.ContainerInstance.dll-Help.xml
Module Name: AzureRM.ContainerInstance
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerinstance/remove-azurermcontainergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerInstance/Commands.ContainerInstance/help/Remove-AzureRmContainerGroup.md
ms.openlocfilehash: f1971f8bf0e7d8e779743739b8dd041effe3ba5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509256"
---
# <span data-ttu-id="c7838-101">Remove-AzureRmContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c7838-101">Remove-AzureRmContainerGroup</span></span>

## <span data-ttu-id="c7838-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7838-102">SYNOPSIS</span></span>
<span data-ttu-id="c7838-103">Rimuove un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="c7838-103">Removes a container group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7838-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7838-104">SYNTAX</span></span>

### <span data-ttu-id="c7838-105">RemoveContainerGroupByResourceGroupAndNameParamSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7838-105">RemoveContainerGroupByResourceGroupAndNameParamSet (Default)</span></span>
```
Remove-AzureRmContainerGroup [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7838-106">RemoveContainerGroupByPSContainerGroupParamSet</span><span class="sxs-lookup"><span data-stu-id="c7838-106">RemoveContainerGroupByPSContainerGroupParamSet</span></span>
```
Remove-AzureRmContainerGroup -InputObject <PSContainerGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7838-107">RemoveContainerGroupByResourceIdParamSet</span><span class="sxs-lookup"><span data-stu-id="c7838-107">RemoveContainerGroupByResourceIdParamSet</span></span>
```
Remove-AzureRmContainerGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7838-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7838-108">DESCRIPTION</span></span>
<span data-ttu-id="c7838-109">Il cmdlet **Remove-AzureRmContainerGroup** rimuove un gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="c7838-109">The **Remove-AzureRmContainerGroup** cmdlet removes a container group.</span></span>

## <span data-ttu-id="c7838-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7838-110">EXAMPLES</span></span>

### <span data-ttu-id="c7838-111">Esempio 1: rimuove un gruppo di contenitori</span><span class="sxs-lookup"><span data-stu-id="c7838-111">Example 1: Removes a container group</span></span>
```
PS C:\> Remove-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer
```

<span data-ttu-id="c7838-112">Questo comando rimuove il gruppo di contenitori specificato.</span><span class="sxs-lookup"><span data-stu-id="c7838-112">This command removes the specified container group.</span></span>

### <span data-ttu-id="c7838-113">Esempio 2: rimuove un gruppo di contenitori per piping</span><span class="sxs-lookup"><span data-stu-id="c7838-113">Example 2: Removes a container group by piping</span></span>
```
PS C:\> Get-AzureRmContainerGroup -ResourceGroupName MyResourceGroup -Name MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="c7838-114">Questo comando rimuove un gruppo di contenitori per piping.</span><span class="sxs-lookup"><span data-stu-id="c7838-114">This command removes a container group by piping.</span></span>

### <span data-ttu-id="c7838-115">Esempio 3: rimuove un gruppo di contenitori in base all'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7838-115">Example 3: Removes a container group by resource Id.</span></span>
```
PS C:\> Find-AzureRmResource -ResourceGroupEquals MyResourceGroup -ResourceNameEquals MyContainer | Remove-AzureRmContainerGroup
```

<span data-ttu-id="c7838-116">Questo comando rimuove un gruppo di contenitori per ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7838-116">This command removes a container group by resource Id.</span></span>

## <span data-ttu-id="c7838-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7838-117">PARAMETERS</span></span>

### <span data-ttu-id="c7838-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7838-118">-DefaultProfile</span></span>
<span data-ttu-id="c7838-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7838-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7838-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7838-120">-InputObject</span></span>
<span data-ttu-id="c7838-121">Gruppo contenitore da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c7838-121">The container group to remove.</span></span>

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

### <span data-ttu-id="c7838-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7838-122">-Name</span></span>
<span data-ttu-id="c7838-123">Nome del gruppo di contenitori.</span><span class="sxs-lookup"><span data-stu-id="c7838-123">The container group name.</span></span>

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

### <span data-ttu-id="c7838-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7838-124">-PassThru</span></span>
<span data-ttu-id="c7838-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="c7838-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c7838-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7838-126">-ResourceGroupName</span></span>
<span data-ttu-id="c7838-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7838-127">The resource group name.</span></span>

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

### <span data-ttu-id="c7838-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7838-128">-ResourceId</span></span>
<span data-ttu-id="c7838-129">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="c7838-129">The resource id.</span></span>

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

### <span data-ttu-id="c7838-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7838-130">-Confirm</span></span>
<span data-ttu-id="c7838-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7838-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7838-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7838-132">-WhatIf</span></span>
<span data-ttu-id="c7838-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7838-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7838-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7838-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7838-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7838-135">CommonParameters</span></span>
<span data-ttu-id="c7838-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7838-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7838-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7838-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7838-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7838-138">INPUTS</span></span>

### <span data-ttu-id="c7838-139">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c7838-139">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>
<span data-ttu-id="c7838-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c7838-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c7838-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c7838-141">System.String</span></span>

## <span data-ttu-id="c7838-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7838-142">OUTPUTS</span></span>

### <span data-ttu-id="c7838-143">Microsoft. Azure. Commands. ContainerInstance. Models. PSContainerGroup</span><span class="sxs-lookup"><span data-stu-id="c7838-143">Microsoft.Azure.Commands.ContainerInstance.Models.PSContainerGroup</span></span>

## <span data-ttu-id="c7838-144">Note</span><span class="sxs-lookup"><span data-stu-id="c7838-144">NOTES</span></span>

## <span data-ttu-id="c7838-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7838-145">RELATED LINKS</span></span>
