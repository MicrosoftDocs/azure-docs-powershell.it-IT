---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032520"
---
# <span data-ttu-id="b5957-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="b5957-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="b5957-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5957-102">SYNOPSIS</span></span>
<span data-ttu-id="b5957-103">Rimuove la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5957-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="b5957-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5957-104">SYNTAX</span></span>

### <span data-ttu-id="b5957-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b5957-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5957-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5957-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5957-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5957-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5957-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5957-108">DESCRIPTION</span></span>
<span data-ttu-id="b5957-109">Il cmdlet **Remove-AzHDInsightClusterAutoscaleConfiguration** rimuove la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5957-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="b5957-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5957-110">EXAMPLES</span></span>

### <span data-ttu-id="b5957-111">Esempio 1: rimuovere la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5957-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="b5957-112">Questo comando rimuove la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="b5957-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="b5957-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5957-113">PARAMETERS</span></span>

### <span data-ttu-id="b5957-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5957-114">-AsJob</span></span>
<span data-ttu-id="b5957-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b5957-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5957-116">-Clustername</span><span class="sxs-lookup"><span data-stu-id="b5957-116">-ClusterName</span></span>
<span data-ttu-id="b5957-117">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="b5957-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5957-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5957-118">-DefaultProfile</span></span>
<span data-ttu-id="b5957-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b5957-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5957-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5957-120">-InputObject</span></span>
<span data-ttu-id="b5957-121">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="b5957-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5957-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5957-122">-ResourceGroupName</span></span>
<span data-ttu-id="b5957-123">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5957-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5957-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5957-124">-ResourceId</span></span>
<span data-ttu-id="b5957-125">Ottiene o imposta l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="b5957-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5957-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b5957-126">-Confirm</span></span>
<span data-ttu-id="b5957-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5957-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5957-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5957-128">-WhatIf</span></span>
<span data-ttu-id="b5957-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5957-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5957-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b5957-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5957-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5957-131">CommonParameters</span></span>
<span data-ttu-id="b5957-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5957-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5957-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b5957-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5957-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5957-134">INPUTS</span></span>

### <span data-ttu-id="b5957-135">System. String</span><span class="sxs-lookup"><span data-stu-id="b5957-135">System.String</span></span>

### <span data-ttu-id="b5957-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="b5957-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="b5957-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5957-137">OUTPUTS</span></span>

### <span data-ttu-id="b5957-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b5957-138">System.Boolean</span></span>

## <span data-ttu-id="b5957-139">Note</span><span class="sxs-lookup"><span data-stu-id="b5957-139">NOTES</span></span>

## <span data-ttu-id="b5957-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5957-140">RELATED LINKS</span></span>

<span data-ttu-id="b5957-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="b5957-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
