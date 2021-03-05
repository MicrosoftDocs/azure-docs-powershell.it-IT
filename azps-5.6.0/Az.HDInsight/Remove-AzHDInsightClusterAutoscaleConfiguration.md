---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: c18567cac6edbeb55b0f7442b45748bc3d62bc86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980413"
---
# <span data-ttu-id="98c21-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="98c21-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="98c21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98c21-102">SYNOPSIS</span></span>
<span data-ttu-id="98c21-103">Rimuove la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="98c21-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="98c21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98c21-104">SYNTAX</span></span>

### <span data-ttu-id="98c21-105">RemoveByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98c21-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c21-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c21-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c21-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98c21-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c21-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="98c21-108">DESCRIPTION</span></span>
<span data-ttu-id="98c21-109">Il cmdlet **Remove-AzHDInsightClusterAutoscaleConfiguration** rimuove la configurazione di gradazione automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="98c21-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="98c21-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98c21-110">EXAMPLES</span></span>

### <span data-ttu-id="98c21-111">Esempio 1: Rimuovere la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="98c21-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="98c21-112">Questo comando rimuove la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="98c21-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="98c21-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98c21-113">PARAMETERS</span></span>

### <span data-ttu-id="98c21-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98c21-114">-AsJob</span></span>
<span data-ttu-id="98c21-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="98c21-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98c21-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="98c21-116">-ClusterName</span></span>
<span data-ttu-id="98c21-117">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="98c21-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="98c21-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c21-118">-DefaultProfile</span></span>
<span data-ttu-id="98c21-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98c21-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98c21-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98c21-120">-InputObject</span></span>
<span data-ttu-id="98c21-121">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="98c21-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="98c21-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c21-122">-ResourceGroupName</span></span>
<span data-ttu-id="98c21-123">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="98c21-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="98c21-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98c21-124">-ResourceId</span></span>
<span data-ttu-id="98c21-125">Ottiene o imposta l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="98c21-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="98c21-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98c21-126">-Confirm</span></span>
<span data-ttu-id="98c21-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c21-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c21-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c21-128">-WhatIf</span></span>
<span data-ttu-id="98c21-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98c21-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98c21-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98c21-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c21-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c21-131">CommonParameters</span></span>
<span data-ttu-id="98c21-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c21-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c21-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98c21-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c21-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="98c21-134">INPUTS</span></span>

### <span data-ttu-id="98c21-135">System.String</span><span class="sxs-lookup"><span data-stu-id="98c21-135">System.String</span></span>

### <span data-ttu-id="98c21-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="98c21-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="98c21-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98c21-137">OUTPUTS</span></span>

### <span data-ttu-id="98c21-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98c21-138">System.Boolean</span></span>

## <span data-ttu-id="98c21-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="98c21-139">NOTES</span></span>

## <span data-ttu-id="98c21-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98c21-140">RELATED LINKS</span></span>

<span data-ttu-id="98c21-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="98c21-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
