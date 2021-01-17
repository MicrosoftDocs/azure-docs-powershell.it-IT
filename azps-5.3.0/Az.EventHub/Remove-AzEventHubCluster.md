---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubCluster.md
ms.openlocfilehash: e67d70f91e523cd46755035abe951682b1764cbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386931"
---
# <span data-ttu-id="5d015-101">Remove-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="5d015-101">Remove-AzEventHubCluster</span></span>

## <span data-ttu-id="5d015-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d015-102">SYNOPSIS</span></span>
<span data-ttu-id="5d015-103">Elimina il cluster di Eventhub dedicato specificato da ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d015-103">Deletes the specified Dedicated Eventhub Cluster from the ResourceGroup</span></span>

## <span data-ttu-id="5d015-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d015-104">SYNTAX</span></span>

### <span data-ttu-id="5d015-105">ClusterPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d015-105">ClusterPropertiesSet (Default)</span></span>
```
Remove-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d015-106">ClusterInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5d015-106">ClusterInputObjectSet</span></span>
```
Remove-AzEventHubCluster [-InputObject] <PSEventHubAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5d015-107">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d015-107">ClusterResourceIdParameterSet</span></span>
```
Remove-AzEventHubCluster [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d015-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d015-108">DESCRIPTION</span></span>
<span data-ttu-id="5d015-109">Il cmdlet Remove-AzEventHubCluster Elimina il nome del cluster eventhub dedicato assegnato dall'ResourceGroup specificata</span><span class="sxs-lookup"><span data-stu-id="5d015-109">The Remove-AzEventHubCluster cmdlet deletes the given dedicated eventhub Cluster name from the given resourcegroup</span></span>

## <span data-ttu-id="5d015-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d015-110">EXAMPLES</span></span>

### <span data-ttu-id="5d015-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d015-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557
```

<span data-ttu-id="5d015-112">Elimina Eventhub-cluster-5557 cluster da RSG-Cluster27651 ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5d015-112">Deletes Eventhub-Cluster-5557 Cluster from RSG-Cluster27651 resourcegroup</span></span>

## <span data-ttu-id="5d015-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d015-113">PARAMETERS</span></span>

### <span data-ttu-id="5d015-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d015-114">-AsJob</span></span>
<span data-ttu-id="5d015-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5d015-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d015-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d015-116">-DefaultProfile</span></span>
<span data-ttu-id="5d015-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d015-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d015-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d015-118">-InputObject</span></span>
<span data-ttu-id="5d015-119">Oggetto cluster</span><span class="sxs-lookup"><span data-stu-id="5d015-119">Cluster Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: ClusterInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d015-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d015-120">-Name</span></span>
<span data-ttu-id="5d015-121">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="5d015-121">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d015-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d015-122">-PassThru</span></span>
<span data-ttu-id="5d015-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="5d015-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="5d015-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d015-124">-ResourceGroupName</span></span>
<span data-ttu-id="5d015-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5d015-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d015-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5d015-126">-ResourceId</span></span>
<span data-ttu-id="5d015-127">ID risorsa cluster</span><span class="sxs-lookup"><span data-stu-id="5d015-127">Cluster Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d015-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5d015-128">-Confirm</span></span>
<span data-ttu-id="5d015-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5d015-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d015-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d015-130">-WhatIf</span></span>
<span data-ttu-id="5d015-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d015-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d015-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5d015-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d015-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d015-133">CommonParameters</span></span>
<span data-ttu-id="5d015-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d015-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d015-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d015-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d015-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d015-136">INPUTS</span></span>

### <span data-ttu-id="5d015-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5d015-137">System.String</span></span>

### <span data-ttu-id="5d015-138">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="5d015-138">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="5d015-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d015-139">OUTPUTS</span></span>

### <span data-ttu-id="5d015-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d015-140">System.Boolean</span></span>

## <span data-ttu-id="5d015-141">Note</span><span class="sxs-lookup"><span data-stu-id="5d015-141">NOTES</span></span>

## <span data-ttu-id="5d015-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d015-142">RELATED LINKS</span></span>
