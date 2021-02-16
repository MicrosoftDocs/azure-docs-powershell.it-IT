---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryReplication.md
ms.openlocfilehash: 41bdf9bbc33239590f9d3a6db4ffaa88ddf752a1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199119"
---
# <span data-ttu-id="c6263-101">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6263-101">Remove-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="c6263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6263-102">SYNOPSIS</span></span>
<span data-ttu-id="c6263-103">Rimuove una replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6263-103">Removes a container registry replication.</span></span>

## <span data-ttu-id="c6263-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6263-104">SYNTAX</span></span>

### <span data-ttu-id="c6263-105">NameResourceGroupParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c6263-105">NameResourceGroupParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6263-106">ReplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6263-106">ReplicationObjectParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -Replication <PSContainerRegistryReplication> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6263-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c6263-107">ResourceIdParameterSet</span></span>
```
Remove-AzContainerRegistryReplication -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6263-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6263-108">DESCRIPTION</span></span>
<span data-ttu-id="c6263-109">Il cmdlet Remove-AzContainerRegistryReplication rimuove una replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6263-109">The Remove-AzContainerRegistryReplication cmdlet removes a container registry replication.</span></span>

## <span data-ttu-id="c6263-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6263-110">EXAMPLES</span></span>

### <span data-ttu-id="c6263-111">Esempio 1: rimuove una replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6263-111">Example 1: Removes a container registry replication.</span></span>
```powershell
PS C:\> Remove-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "replication001"
```

<span data-ttu-id="c6263-112">Rimuove una replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6263-112">Removes a container registry replication.</span></span>

## <span data-ttu-id="c6263-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6263-113">PARAMETERS</span></span>

### <span data-ttu-id="c6263-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6263-114">-DefaultProfile</span></span>
<span data-ttu-id="c6263-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6263-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6263-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c6263-116">-Name</span></span>
<span data-ttu-id="c6263-117">Nome della replica del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6263-117">Container Registry Replication Name.</span></span>
<span data-ttu-id="c6263-118">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="c6263-118">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6263-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6263-119">-PassThru</span></span>
<span data-ttu-id="c6263-120">Indica che questo cmdlet restituisce True se la rimozione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="c6263-120">Indicates that this cmdlet returns true if the removal was successful.</span></span>

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

### <span data-ttu-id="c6263-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c6263-121">-RegistryName</span></span>
<span data-ttu-id="c6263-122">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c6263-122">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6263-123">-Replica</span><span class="sxs-lookup"><span data-stu-id="c6263-123">-Replication</span></span>
<span data-ttu-id="c6263-124">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c6263-124">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication
Parameter Sets: ReplicationObjectParameterSet
Aliases: Replicatoin

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6263-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6263-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6263-126">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6263-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6263-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6263-127">-ResourceId</span></span>
<span data-ttu-id="c6263-128">ID risorsa replica del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="c6263-128">The container registry replication resource id</span></span>

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

### <span data-ttu-id="c6263-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6263-129">-Confirm</span></span>
<span data-ttu-id="c6263-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6263-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6263-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6263-131">-WhatIf</span></span>
<span data-ttu-id="c6263-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6263-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6263-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6263-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6263-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6263-134">CommonParameters</span></span>
<span data-ttu-id="c6263-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6263-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6263-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6263-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6263-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6263-137">INPUTS</span></span>

### <span data-ttu-id="c6263-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6263-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

### <span data-ttu-id="c6263-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c6263-139">System.String</span></span>

## <span data-ttu-id="c6263-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6263-140">OUTPUTS</span></span>

### <span data-ttu-id="c6263-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c6263-141">System.Boolean</span></span>

## <span data-ttu-id="c6263-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6263-142">NOTES</span></span>

## <span data-ttu-id="c6263-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6263-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6263-144">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6263-144">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="c6263-145">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c6263-145">Get-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)

