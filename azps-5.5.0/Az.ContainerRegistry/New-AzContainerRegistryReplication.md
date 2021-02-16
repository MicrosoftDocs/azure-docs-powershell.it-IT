---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199143"
---
# <span data-ttu-id="cf855-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cf855-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="cf855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf855-102">SYNOPSIS</span></span>
<span data-ttu-id="cf855-103">Crea una replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf855-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="cf855-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf855-104">SYNTAX</span></span>

### <span data-ttu-id="cf855-105">NameResourceGroupParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf855-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cf855-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf855-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cf855-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf855-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf855-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cf855-108">DESCRIPTION</span></span>
<span data-ttu-id="cf855-109">Il cmdlet New-AzContainerRegistryReplication crea una nuova replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf855-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="cf855-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf855-110">EXAMPLES</span></span>

### <span data-ttu-id="cf855-111">Esempio 1: Creare una nuova replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf855-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="cf855-112">Creare una nuova replica del Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf855-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="cf855-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cf855-113">PARAMETERS</span></span>

### <span data-ttu-id="cf855-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf855-114">-DefaultProfile</span></span>
<span data-ttu-id="cf855-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cf855-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cf855-116">-Location</span><span class="sxs-lookup"><span data-stu-id="cf855-116">-Location</span></span>
<span data-ttu-id="cf855-117">Posizione del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf855-117">Container Registry Location.</span></span>
<span data-ttu-id="cf855-118">Impostazione predefinita per il percorso del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf855-118">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationLocation

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf855-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cf855-119">-Name</span></span>
<span data-ttu-id="cf855-120">Nome della replica del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf855-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="cf855-121">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="cf855-121">Default to the location name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ReplicationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf855-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="cf855-122">-Registry</span></span>
<span data-ttu-id="cf855-123">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="cf855-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="cf855-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="cf855-124">-RegistryName</span></span>
<span data-ttu-id="cf855-125">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="cf855-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf855-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf855-126">-ResourceGroupName</span></span>
<span data-ttu-id="cf855-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cf855-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="cf855-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf855-128">-ResourceId</span></span>
<span data-ttu-id="cf855-129">ID risorsa del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="cf855-129">The container registry resource id</span></span>

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

### <span data-ttu-id="cf855-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="cf855-130">-Tag</span></span>
<span data-ttu-id="cf855-131">Tag container del Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="cf855-131">Container Registry Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf855-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cf855-132">-Confirm</span></span>
<span data-ttu-id="cf855-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf855-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf855-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf855-134">-WhatIf</span></span>
<span data-ttu-id="cf855-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf855-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf855-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf855-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf855-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf855-137">CommonParameters</span></span>
<span data-ttu-id="cf855-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf855-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf855-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cf855-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf855-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="cf855-140">INPUTS</span></span>

### <span data-ttu-id="cf855-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cf855-141">System.String</span></span>

## <span data-ttu-id="cf855-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf855-142">OUTPUTS</span></span>

### <span data-ttu-id="cf855-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cf855-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="cf855-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="cf855-144">NOTES</span></span>

## <span data-ttu-id="cf855-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf855-145">RELATED LINKS</span></span>

[<span data-ttu-id="cf855-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cf855-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="cf855-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="cf855-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)