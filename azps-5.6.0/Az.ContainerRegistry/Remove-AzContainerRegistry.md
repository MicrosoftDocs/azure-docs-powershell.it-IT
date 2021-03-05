---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistry.md
ms.openlocfilehash: 49da6e1efbd1bb0e6b0ac4dc693d51fe5b58bfac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015389"
---
# <span data-ttu-id="b1248-101">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b1248-101">Remove-AzContainerRegistry</span></span>

## <span data-ttu-id="b1248-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1248-102">SYNOPSIS</span></span>
<span data-ttu-id="b1248-103">Rimuove un registro di contenitore.</span><span class="sxs-lookup"><span data-stu-id="b1248-103">Removes a container registry.</span></span>

## <span data-ttu-id="b1248-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1248-104">SYNTAX</span></span>

### <span data-ttu-id="b1248-105">NameResourceGroupParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="b1248-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1248-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1248-106">RegistryObjectParameterSet</span></span>
```
Remove-AzContainerRegistry -Registry <PSContainerRegistry> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1248-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1248-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistry -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1248-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b1248-108">DESCRIPTION</span></span>
<span data-ttu-id="b1248-109">Il cmdlet Remove-AzContainerRegistry rimuove un contenitore del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b1248-109">The Remove-AzContainerRegistry cmdlet removes a container registry.</span></span>

## <span data-ttu-id="b1248-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1248-110">EXAMPLES</span></span>

### <span data-ttu-id="b1248-111">Esempio 1: Rimuovere un contenitore specificato nel Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="b1248-111">Example 1: Remove a specified container registry</span></span>
```powershell
PS C:\>Remove-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"
```

<span data-ttu-id="b1248-112">Questo comando rimuove il Registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="b1248-112">This command removes the specified container registry.</span></span>

## <span data-ttu-id="b1248-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1248-113">PARAMETERS</span></span>

### <span data-ttu-id="b1248-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1248-114">-DefaultProfile</span></span>
<span data-ttu-id="b1248-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b1248-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b1248-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b1248-116">-Name</span></span>
<span data-ttu-id="b1248-117">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="b1248-117">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1248-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1248-118">-PassThru</span></span>
<span data-ttu-id="b1248-119">Indica che questo cmdlet restituisce True se la rimozione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b1248-119">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="b1248-120">-Registry</span><span class="sxs-lookup"><span data-stu-id="b1248-120">-Registry</span></span>
<span data-ttu-id="b1248-121">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="b1248-121">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1248-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1248-122">-ResourceGroupName</span></span>
<span data-ttu-id="b1248-123">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1248-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1248-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1248-124">-ResourceId</span></span>
<span data-ttu-id="b1248-125">ID risorsa del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="b1248-125">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1248-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1248-126">-Confirm</span></span>
<span data-ttu-id="b1248-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1248-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1248-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1248-128">-WhatIf</span></span>
<span data-ttu-id="b1248-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1248-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1248-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1248-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1248-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1248-131">CommonParameters</span></span>
<span data-ttu-id="b1248-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1248-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1248-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b1248-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1248-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="b1248-134">INPUTS</span></span>

### <span data-ttu-id="b1248-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b1248-135">System.String</span></span>

## <span data-ttu-id="b1248-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1248-136">OUTPUTS</span></span>

### <span data-ttu-id="b1248-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b1248-137">System.Boolean</span></span>

## <span data-ttu-id="b1248-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="b1248-138">NOTES</span></span>

## <span data-ttu-id="b1248-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1248-139">RELATED LINKS</span></span>

[<span data-ttu-id="b1248-140">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b1248-140">New-AzContainerRegistry</span></span>]()

[<span data-ttu-id="b1248-141">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b1248-141">Get-AzContainerRegistry</span></span>]()

[<span data-ttu-id="b1248-142">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b1248-142">Update-AzContainerRegistry</span></span>]()

