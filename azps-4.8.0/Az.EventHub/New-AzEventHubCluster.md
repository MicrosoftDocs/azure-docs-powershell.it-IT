---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubCluster.md
ms.openlocfilehash: 2783b2c35cdae6afb2e0e73cd966dc2ddfa3e70c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190196"
---
# <span data-ttu-id="894d2-101">New-AzEventHubCluster</span><span class="sxs-lookup"><span data-stu-id="894d2-101">New-AzEventHubCluster</span></span>

## <span data-ttu-id="894d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="894d2-102">SYNOPSIS</span></span>
<span data-ttu-id="894d2-103">Crea un nuovo cluster di eventhub dedicato</span><span class="sxs-lookup"><span data-stu-id="894d2-103">Creates a new dedicated eventhub cluster</span></span>

## <span data-ttu-id="894d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="894d2-104">SYNTAX</span></span>

### <span data-ttu-id="894d2-105">ClusterPropertiesSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="894d2-105">ClusterPropertiesSet (Default)</span></span>
```
New-AzEventHubCluster [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Capacity <Int32>]
 [-Tag <Hashtable>] [[-ResourceId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="894d2-106">ClusterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="894d2-106">ClusterResourceIdParameterSet</span></span>
```
New-AzEventHubCluster [-Name] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="894d2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="894d2-107">DESCRIPTION</span></span>
<span data-ttu-id="894d2-108">Il cmdlet New-AzEventHubCluster crea il cluster eventhub dedicato nel gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="894d2-108">The New-AzEventHubCluster cmdlet creates the dedicated eventhub cluster in the given resource group</span></span>

## <span data-ttu-id="894d2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="894d2-109">EXAMPLES</span></span>

### <span data-ttu-id="894d2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="894d2-110">Example 1</span></span>
```powershell
PS C:\>  New-AzEventHubCluster -ResourceGroupName RSG-Cluster27651 -Name Eventhub-Cluster-5557 -Location southcentralus -Capacity 1

Id        : /subscriptions/SubId/resourceGroups/RSG-Cluster27651/providers/Microsoft.EventHub/clusters/Eventhub-Cluster-5557
Name      : Eventhub-Cluster-5557
Location  : southcentralus
CreatedAt : 09/10/2020 22:09:57
UpdatedAt : 09/11/2020 01:31:18
MetricId  :
Status    :
Sku       : Microsoft.Azure.Commands.EventHub.Models.PSEventHubsClusterSkuAttributes
Tags      : {[ClusterTag1, Tag1], [ClusterTag2, Tag2]}

```

<span data-ttu-id="894d2-111">Crea il cluster dedicato "Eventhub-cluster-5557" in ResourceGroup "RSG-Cluster27651" con posizione southcentralus e capacità come 1</span><span class="sxs-lookup"><span data-stu-id="894d2-111">Creates 'Eventhub-Cluster-5557' dedicated cluster in resourcegroup 'RSG-Cluster27651' with Location southcentralus and Capacity as 1</span></span>

## <span data-ttu-id="894d2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="894d2-112">PARAMETERS</span></span>

### <span data-ttu-id="894d2-113">-Capacità</span><span class="sxs-lookup"><span data-stu-id="894d2-113">-Capacity</span></span>
<span data-ttu-id="894d2-114">Capacità cluster (CU), curerntrly, valore consentito = 1</span><span class="sxs-lookup"><span data-stu-id="894d2-114">Cluster Capacity (CU), curerntrly, allowed value = 1</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="894d2-115">-DefaultProfile</span></span>
<span data-ttu-id="894d2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="894d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="894d2-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="894d2-117">-Location</span></span>
<span data-ttu-id="894d2-118">Posizione del cluster</span><span class="sxs-lookup"><span data-stu-id="894d2-118">Location of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894d2-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="894d2-119">-Name</span></span>
<span data-ttu-id="894d2-120">Nome cluster</span><span class="sxs-lookup"><span data-stu-id="894d2-120">Cluster Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894d2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="894d2-121">-ResourceGroupName</span></span>
<span data-ttu-id="894d2-122">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="894d2-122">Resource Group Name</span></span>

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

### <span data-ttu-id="894d2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="894d2-123">-ResourceId</span></span>
<span data-ttu-id="894d2-124">ID risorsa del cluster</span><span class="sxs-lookup"><span data-stu-id="894d2-124">Resource ID of Cluster</span></span>

```yaml
Type: System.String
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ClusterResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894d2-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="894d2-125">-Tag</span></span>
<span data-ttu-id="894d2-126">Hashtable che rappresenta i tag delle risorse per i cluster</span><span class="sxs-lookup"><span data-stu-id="894d2-126">Hashtables which represents resource Tags for Clusters</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ClusterPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="894d2-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="894d2-127">-Confirm</span></span>
<span data-ttu-id="894d2-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="894d2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="894d2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="894d2-129">-WhatIf</span></span>
<span data-ttu-id="894d2-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="894d2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="894d2-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="894d2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="894d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="894d2-132">CommonParameters</span></span>
<span data-ttu-id="894d2-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="894d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="894d2-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="894d2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="894d2-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="894d2-135">INPUTS</span></span>

### <span data-ttu-id="894d2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="894d2-136">System.String</span></span>

### <span data-ttu-id="894d2-137">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="894d2-137">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="894d2-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="894d2-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="894d2-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="894d2-139">OUTPUTS</span></span>

### <span data-ttu-id="894d2-140">Microsoft. Azure. Commands. EventHub. Models. PSEventHubClusterAttributes</span><span class="sxs-lookup"><span data-stu-id="894d2-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubClusterAttributes</span></span>

## <span data-ttu-id="894d2-141">Note</span><span class="sxs-lookup"><span data-stu-id="894d2-141">NOTES</span></span>

## <span data-ttu-id="894d2-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="894d2-142">RELATED LINKS</span></span>
