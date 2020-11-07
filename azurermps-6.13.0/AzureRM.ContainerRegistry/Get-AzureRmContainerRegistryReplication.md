---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryReplication.md
ms.openlocfilehash: d2cac696382f807a1fc4afe94f9d2d61ea65cece
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685439"
---
# <span data-ttu-id="add37-101">Get-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="add37-101">Get-AzureRmContainerRegistryReplication</span></span>

## <span data-ttu-id="add37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="add37-102">SYNOPSIS</span></span>
<span data-ttu-id="add37-103">Ottiene una replica di un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="add37-103">Gets a replication of a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="add37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="add37-104">SYNTAX</span></span>

### <span data-ttu-id="add37-105">ListReplicationByNameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="add37-105">ListReplicationByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryReplication [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add37-106">ShowReplicationByNameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="add37-106">ShowReplicationByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add37-107">ShowReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="add37-107">ShowReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication [-Name] <String> -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add37-108">ListReplicationByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="add37-108">ListReplicationByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -Registry <PSContainerRegistry>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="add37-109">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="add37-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryReplication -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="add37-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="add37-110">DESCRIPTION</span></span>
<span data-ttu-id="add37-111">Il cmdlet Get-AzureRmContainerRegistryReplication ottiene una replica specificata di un registro di sistema contenitore o di tutte le repliche di un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="add37-111">The Get-AzureRmContainerRegistryReplication cmdlet gets a specified replication of a container registry or all the replications of a container registry.</span></span>

## <span data-ttu-id="add37-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="add37-112">EXAMPLES</span></span>

### <span data-ttu-id="add37-113">Esempio 1: ottiene una replica specificata di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="add37-113">Example 1: Gets a specified replication of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "myreplication"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
myreplication       westus     Succeeded  Ready                 11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="add37-114">Ottiene una replica specificata di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="add37-114">Gets a specified replication of a container registry</span></span>

### <span data-ttu-id="add37-115">Esempio 2: ottiene tutte le repliche di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="add37-115">Example 2: Gets all the replications of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryReplication -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name                 Location   Provisioni Status               StatusTimestamp                Tags
                                ngState
----                 --------   ---------- ------               ---------------                ----
eastus               eastus     Succeeded  Ready                11/6/2017 6:14:47 PM           {}
myreplication        westus     Succeeded  Ready                11/17/2017 10:19:45 PM         {[tagName, MyTag]}
```

<span data-ttu-id="add37-116">Ottiene tutte le repliche di un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="add37-116">Gets all the replications of a container registry</span></span>

## <span data-ttu-id="add37-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="add37-117">PARAMETERS</span></span>

### <span data-ttu-id="add37-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="add37-118">-DefaultProfile</span></span>
<span data-ttu-id="add37-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="add37-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="add37-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="add37-120">-Name</span></span>
<span data-ttu-id="add37-121">Nome della replica del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="add37-121">Container Registry Replication Name.</span></span>

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

### <span data-ttu-id="add37-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="add37-122">-Registry</span></span>
<span data-ttu-id="add37-123">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="add37-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="add37-124">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="add37-124">-RegistryName</span></span>
<span data-ttu-id="add37-125">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="add37-125">Container Registry Name.</span></span>

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

### <span data-ttu-id="add37-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="add37-126">-ResourceGroupName</span></span>
<span data-ttu-id="add37-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="add37-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="add37-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="add37-128">-ResourceId</span></span>
<span data-ttu-id="add37-129">ID risorsa di replica del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="add37-129">The container registry replication resource id</span></span>

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

### <span data-ttu-id="add37-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="add37-130">CommonParameters</span></span>
<span data-ttu-id="add37-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="add37-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="add37-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="add37-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="add37-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="add37-133">INPUTS</span></span>

### <span data-ttu-id="add37-134">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="add37-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="add37-135">Parametri: Registro di sistema (ByValue)</span><span class="sxs-lookup"><span data-stu-id="add37-135">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="add37-136">System. String</span><span class="sxs-lookup"><span data-stu-id="add37-136">System.String</span></span>

## <span data-ttu-id="add37-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="add37-137">OUTPUTS</span></span>

### <span data-ttu-id="add37-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="add37-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryReplication</span></span>

## <span data-ttu-id="add37-139">Note</span><span class="sxs-lookup"><span data-stu-id="add37-139">NOTES</span></span>

## <span data-ttu-id="add37-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="add37-140">RELATED LINKS</span></span>

[<span data-ttu-id="add37-141">New-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="add37-141">New-AzureRmContainerRegistryReplication</span></span>](New-AzureRmContainerRegistryReplication.md)

[<span data-ttu-id="add37-142">Remove-AzureRmContainerRegistryReplication</span><span class="sxs-lookup"><span data-stu-id="add37-142">Remove-AzureRmContainerRegistryReplication</span></span>](Remove-AzureRmContainerRegistryReplication.md)
