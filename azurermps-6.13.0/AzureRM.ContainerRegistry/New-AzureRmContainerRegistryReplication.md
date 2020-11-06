---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: eaab02fe0e0adbd54bc80b15e6520442d9eb3c11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507543"
---
# <span data-ttu-id="55c46-101">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55c46-101">New-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="55c46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55c46-102">SYNOPSIS</span></span>
<span data-ttu-id="55c46-103">Crea una replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-103">Creates a container registry replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55c46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55c46-104">SYNTAX</span></span>

### <span data-ttu-id="55c46-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="55c46-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 -Location <String> [-Name <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c46-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="55c46-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry> -Location <String> [-Name <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55c46-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="55c46-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryReplication -Location <String> [-Name <String>] [-Tag <Hashtable>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55c46-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55c46-108">DESCRIPTION</span></span>
<span data-ttu-id="55c46-109">Il cmdlet New-AzureRmContainerRegistryReplication crea una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-109">The New-AzureRmContainerRegistryReplication cmdlet creates a new container registry replication.</span></span>

## <span data-ttu-id="55c46-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55c46-110">EXAMPLES</span></span>

### <span data-ttu-id="55c46-111">Esempio 1: creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-111">Example 1: Create a new container registry replication.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name replication001 -Location 'west us' -Tag @{tagName='MyTag'}

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
replication001       westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="55c46-112">Creare una nuova replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-112">Create a new container registry replication.</span></span>

## <span data-ttu-id="55c46-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55c46-113">PARAMETERS</span></span>

### <span data-ttu-id="55c46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55c46-114">-DefaultProfile</span></span>
<span data-ttu-id="55c46-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55c46-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55c46-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="55c46-116">-Location</span></span>
<span data-ttu-id="55c46-117">Percorso del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-117">Container Registry Location.</span></span>
<span data-ttu-id="55c46-118">Impostazione predefinita per la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55c46-118">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="55c46-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="55c46-119">-Name</span></span>
<span data-ttu-id="55c46-120">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-120">Container Registry Replication Name.</span></span>
<span data-ttu-id="55c46-121">Impostazione predefinita per il nome della posizione.</span><span class="sxs-lookup"><span data-stu-id="55c46-121">Default to the location name.</span></span>

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

### <span data-ttu-id="55c46-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="55c46-122">-Registry</span></span>
<span data-ttu-id="55c46-123">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="55c46-124">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="55c46-124">-RegistryName</span></span>
<span data-ttu-id="55c46-125">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="55c46-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55c46-126">-ResourceGroupName</span></span>
<span data-ttu-id="55c46-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55c46-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="55c46-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="55c46-128">-ResourceId</span></span>
<span data-ttu-id="55c46-129">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="55c46-129">The container registry resource id</span></span>

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

### <span data-ttu-id="55c46-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="55c46-130">-Tag</span></span>
<span data-ttu-id="55c46-131">Tag del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="55c46-131">Container Registry Tags.</span></span>

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

### <span data-ttu-id="55c46-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55c46-132">-Confirm</span></span>
<span data-ttu-id="55c46-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55c46-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55c46-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55c46-134">-WhatIf</span></span>
<span data-ttu-id="55c46-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55c46-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55c46-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55c46-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55c46-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55c46-137">CommonParameters</span></span>
<span data-ttu-id="55c46-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55c46-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55c46-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55c46-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55c46-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55c46-140">INPUTS</span></span>

### <span data-ttu-id="55c46-141">System. String</span><span class="sxs-lookup"><span data-stu-id="55c46-141">System.String</span></span>

## <span data-ttu-id="55c46-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55c46-142">OUTPUTS</span></span>

### <span data-ttu-id="55c46-143">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55c46-143">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="55c46-144">Note</span><span class="sxs-lookup"><span data-stu-id="55c46-144">NOTES</span></span>

## <span data-ttu-id="55c46-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55c46-145">RELATED LINKS</span></span>

[<span data-ttu-id="55c46-146">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55c46-146">Get-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="55c46-147">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="55c46-147">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
