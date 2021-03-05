---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 3054c6ed8083d1108c853ab188903cc3b2ebd380
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004413"
---
# <span data-ttu-id="c5368-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c5368-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="c5368-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5368-102">SYNOPSIS</span></span>
<span data-ttu-id="c5368-103">Ottiene una replica di un Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="c5368-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="c5368-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5368-104">SYNTAX</span></span>

### <span data-ttu-id="c5368-105">ListReplicationByNameResourceGroupParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5368-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5368-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5368-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5368-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5368-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5368-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5368-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5368-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5368-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5368-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5368-110">DESCRIPTION</span></span>
<span data-ttu-id="c5368-111">Il Get-AzContainerRegistryReplication cmdlet ottiene una replica specificata di un Registro di sistema del contenitore o di tutte le replica di un registro contenitore.</span><span class="sxs-lookup"><span data-stu-id="c5368-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="c5368-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5368-112">EXAMPLES</span></span>

### <span data-ttu-id="c5368-113">Esempio 1: ottiene una replica specificata di un Registro di sistema del contenitore</span><span class="sxs-lookup"><span data-stu-id="c5368-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="c5368-114">Ottiene una replica specificata di un Registro di sistema del contenitore</span><span class="sxs-lookup"><span data-stu-id="c5368-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="c5368-115">Esempio 2: Ottiene tutte le replica di un Registro di sistema del contenitore</span><span class="sxs-lookup"><span data-stu-id="c5368-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="c5368-116">Ottiene tutte le replica di un Registro di sistema del contenitore</span><span class="sxs-lookup"><span data-stu-id="c5368-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="c5368-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5368-117">PARAMETERS</span></span>

### <span data-ttu-id="c5368-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5368-118">-DefaultProfile</span></span>
<span data-ttu-id="c5368-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5368-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5368-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c5368-120">-Name</span></span>
<span data-ttu-id="c5368-121">Nome della replica del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c5368-121">Container Registry Replication Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowReplicationByNameResourceGroupParameterSet, ShowReplicationByRegistryObjectParameterSet
Aliases: ReplicationName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5368-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="c5368-122">-Registry</span></span>
<span data-ttu-id="c5368-123">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="c5368-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowReplicationByRegistryObjectParameterSet, ListReplicationByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5368-124">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c5368-124">-RegistryName</span></span>
<span data-ttu-id="c5368-125">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="c5368-125">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5368-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5368-126">-ResourceGroupName</span></span>
<span data-ttu-id="c5368-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c5368-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListReplicationByNameResourceGroupParameterSet, ShowReplicationByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5368-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5368-128">-ResourceId</span></span>
<span data-ttu-id="c5368-129">ID risorsa replica del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="c5368-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="c5368-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5368-130">CommonParameters</span></span>
<span data-ttu-id="c5368-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5368-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5368-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5368-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5368-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5368-133">INPUTS</span></span>

### <span data-ttu-id="c5368-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="c5368-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="c5368-135">System.String</span><span class="sxs-lookup"><span data-stu-id="c5368-135">System.String</span></span>

## <span data-ttu-id="c5368-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5368-136">OUTPUTS</span></span>

### <span data-ttu-id="c5368-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c5368-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="c5368-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5368-138">NOTES</span></span>

## <span data-ttu-id="c5368-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5368-139">RELATED LINKS</span></span>

[<span data-ttu-id="c5368-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c5368-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="c5368-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="c5368-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)