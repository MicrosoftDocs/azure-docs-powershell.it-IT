---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488023"
---
# <span data-ttu-id="590e6-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="590e6-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="590e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="590e6-102">SYNOPSIS</span></span>
<span data-ttu-id="590e6-103">Crea una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="590e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="590e6-104">SYNTAX</span></span>

### <span data-ttu-id="590e6-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="590e6-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="590e6-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="590e6-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="590e6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="590e6-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="590e6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="590e6-108">DESCRIPTION</span></span>
<span data-ttu-id="590e6-109">Il cmdlet New-AzContainerRegistryReplication crea una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="590e6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="590e6-110">EXAMPLES</span></span>

### <span data-ttu-id="590e6-111">Esempio 1: creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="590e6-112">Creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="590e6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="590e6-113">PARAMETERS</span></span>

### <span data-ttu-id="590e6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="590e6-114">-DefaultProfile</span></span>
<span data-ttu-id="590e6-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="590e6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="590e6-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="590e6-116">-Location</span></span>
<span data-ttu-id="590e6-117">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-117">Container Registry Location.</span></span>
<span data-ttu-id="590e6-118">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="590e6-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="590e6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="590e6-119">-Name</span></span>
<span data-ttu-id="590e6-120">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="590e6-121">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="590e6-121">Default to the location name.</span></span>

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

### <span data-ttu-id="590e6-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="590e6-122">-Registry</span></span>
<span data-ttu-id="590e6-123">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="590e6-124">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="590e6-124">-RegistryName</span></span>
<span data-ttu-id="590e6-125">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="590e6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="590e6-126">-ResourceGroupName</span></span>
<span data-ttu-id="590e6-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="590e6-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="590e6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="590e6-128">-ResourceId</span></span>
<span data-ttu-id="590e6-129">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="590e6-129">The container registry resource id</span></span>

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

### <span data-ttu-id="590e6-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="590e6-130">-Tag</span></span>
<span data-ttu-id="590e6-131">Tag del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="590e6-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="590e6-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="590e6-132">-Confirm</span></span>
<span data-ttu-id="590e6-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="590e6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="590e6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="590e6-134">-WhatIf</span></span>
<span data-ttu-id="590e6-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="590e6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="590e6-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="590e6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="590e6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="590e6-137">CommonParameters</span></span>
<span data-ttu-id="590e6-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="590e6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="590e6-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="590e6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="590e6-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="590e6-140">INPUTS</span></span>

### <span data-ttu-id="590e6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="590e6-141">System.String</span></span>

## <span data-ttu-id="590e6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="590e6-142">OUTPUTS</span></span>

### <span data-ttu-id="590e6-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="590e6-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="590e6-144">Note</span><span class="sxs-lookup"><span data-stu-id="590e6-144">NOTES</span></span>

## <span data-ttu-id="590e6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="590e6-145">RELATED LINKS</span></span>

[<span data-ttu-id="590e6-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="590e6-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="590e6-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="590e6-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)