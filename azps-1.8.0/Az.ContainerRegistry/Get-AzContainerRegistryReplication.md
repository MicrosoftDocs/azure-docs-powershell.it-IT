---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistryreplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryReplication.md
ms.openlocfilehash: 21e821a4575fb918599ad2315c569a7f270e0a84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684645"
---
# <span data-ttu-id="f2ba9-101">Get-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f2ba9-101">Get-AzContainerRegistryReplication</span></span>

## <span data-ttu-id="f2ba9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2ba9-102">SYNOPSIS</span></span>
<span data-ttu-id="f2ba9-103">Ottiene una replica di un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-103">Gets a replication of a container registry.</span></span>

## <span data-ttu-id="f2ba9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2ba9-104">SYNTAX</span></span>

### <span data-ttu-id="f2ba9-105">ListReplicationByNameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2ba9-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2ba9-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2ba9-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2ba9-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2ba9-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2ba9-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2ba9-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryReplication -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2ba9-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2ba9-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f2ba9-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2ba9-110">DESCRIPTION</span></span>
<span data-ttu-id="f2ba9-111">Il cmdlet Get-AzContainerRegistryReplication ottiene una replica specificata di un registro di sistema contenitore o di tutte le repliche di un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-111">The Get-AzContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="f2ba9-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2ba9-112">EXAMPLES</span></span>

### <span data-ttu-id="f2ba9-113">Esempio 1: ottiene una replica specificata di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f2ba9-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="f2ba9-114">Ottiene una replica specificata di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f2ba9-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="f2ba9-115">Esempio 2: ottiene tutte le repliche di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f2ba9-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="f2ba9-116">Ottiene tutte le repliche di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f2ba9-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="f2ba9-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2ba9-117">PARAMETERS</span></span>

### <span data-ttu-id="f2ba9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2ba9-118">-DefaultProfile</span></span>
<span data-ttu-id="f2ba9-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2ba9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2ba9-120">-Name</span></span>
<span data-ttu-id="f2ba9-121">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="f2ba9-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f2ba9-122">-Registry</span></span>
<span data-ttu-id="f2ba9-123">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="f2ba9-124">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f2ba9-124">-RegistryName</span></span>
<span data-ttu-id="f2ba9-125">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="f2ba9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2ba9-126">-ResourceGroupName</span></span>
<span data-ttu-id="f2ba9-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f2ba9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2ba9-128">-ResourceId</span></span>
<span data-ttu-id="f2ba9-129">ID risorsa di replica del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f2ba9-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="f2ba9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2ba9-130">CommonParameters</span></span>
<span data-ttu-id="f2ba9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2ba9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2ba9-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2ba9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2ba9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2ba9-133">INPUTS</span></span>

### <span data-ttu-id="f2ba9-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f2ba9-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="f2ba9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f2ba9-135">System.String</span></span>

## <span data-ttu-id="f2ba9-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2ba9-136">OUTPUTS</span></span>

### <span data-ttu-id="f2ba9-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f2ba9-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="f2ba9-138">Note</span><span class="sxs-lookup"><span data-stu-id="f2ba9-138">NOTES</span></span>

## <span data-ttu-id="f2ba9-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2ba9-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2ba9-140">New-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f2ba9-140">New-AzContainerRegistryReplication</span></span>](New-AzContainerRegistryReplication.md)

[<span data-ttu-id="f2ba9-141">Remove-AzContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="f2ba9-141">Remove-AzContainerRegistryReplication</span></span>](Remove-AzContainerRegistryReplication.md)