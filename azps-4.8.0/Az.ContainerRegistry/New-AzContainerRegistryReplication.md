---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryReplication.md
ms.openlocfilehash: aadac0f7d408efd5f635d77d14f9afabfbd444d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190353"
---
# <span data-ttu-id="e3c52-101">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e3c52-101">New-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="e3c52-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3c52-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c52-103">Crea una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-103">Creates a container registry replication.</span></span>

## <span data-ttu-id="e3c52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3c52-104">SYNTAX</span></span>

### <span data-ttu-id="e3c52-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3c52-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String> -Location <String>
 [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3c52-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3c52-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3c52-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3c52-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3c52-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3c52-108">DESCRIPTION</span></span>
<span data-ttu-id="e3c52-109">Il cmdlet New-AzContainerRegistryReplication crea una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-109">The New-AzContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="e3c52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3c52-110">EXAMPLES</span></span>

### <span data-ttu-id="e3c52-111">Esempio 1: creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="e3c52-112">Creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="e3c52-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3c52-113">PARAMETERS</span></span>

### <span data-ttu-id="e3c52-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c52-114">-DefaultProfile</span></span>
<span data-ttu-id="e3c52-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c52-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c52-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e3c52-116">-Location</span></span>
<span data-ttu-id="e3c52-117">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-117">Container Registry Location.</span></span>
<span data-ttu-id="e3c52-118">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3c52-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="e3c52-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3c52-119">-Name</span></span>
<span data-ttu-id="e3c52-120">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="e3c52-121">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="e3c52-121">Default to the location name.</span></span>

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

### <span data-ttu-id="e3c52-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e3c52-122">-Registry</span></span>
<span data-ttu-id="e3c52-123">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="e3c52-124">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e3c52-124">-RegistryName</span></span>
<span data-ttu-id="e3c52-125">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="e3c52-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3c52-126">-ResourceGroupName</span></span>
<span data-ttu-id="e3c52-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3c52-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="e3c52-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3c52-128">-ResourceId</span></span>
<span data-ttu-id="e3c52-129">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="e3c52-129">The container registry resource id</span></span>

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

### <span data-ttu-id="e3c52-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="e3c52-130">-Tag</span></span>
<span data-ttu-id="e3c52-131">Tag del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e3c52-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="e3c52-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3c52-132">-Confirm</span></span>
<span data-ttu-id="e3c52-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c52-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c52-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c52-134">-WhatIf</span></span>
<span data-ttu-id="e3c52-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c52-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c52-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c52-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c52-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c52-137">CommonParameters</span></span>
<span data-ttu-id="e3c52-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c52-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c52-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3c52-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c52-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3c52-140">INPUTS</span></span>

### <span data-ttu-id="e3c52-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e3c52-141">System.String</span></span>

## <span data-ttu-id="e3c52-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3c52-142">OUTPUTS</span></span>

### <span data-ttu-id="e3c52-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e3c52-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="e3c52-144">Note</span><span class="sxs-lookup"><span data-stu-id="e3c52-144">NOTES</span></span>

## <span data-ttu-id="e3c52-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3c52-145">RELATED LINKS</span></span>

[<span data-ttu-id="e3c52-146">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e3c52-146">Get-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="e3c52-147">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="e3c52-147">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)