---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207355"
---
# <span data-ttu-id="be90a-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="be90a-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="be90a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="be90a-102">SYNOPSIS</span></span>
<span data-ttu-id="be90a-103">Ottiene la configurazione della scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="be90a-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="be90a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be90a-104">SYNTAX</span></span>

### <span data-ttu-id="be90a-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be90a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be90a-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="be90a-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="be90a-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be90a-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be90a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="be90a-108">DESCRIPTION</span></span>
<span data-ttu-id="be90a-109">Il cmdlet **Get-AzHDInsightClusterAutoscaleConfiguration** ottiene la configurazione della scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="be90a-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="be90a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be90a-110">EXAMPLES</span></span>

### <span data-ttu-id="be90a-111">Esempio 1: Ottenere la configurazione della scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="be90a-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="be90a-112">Questo comando recupera la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="be90a-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="be90a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="be90a-113">PARAMETERS</span></span>

### <span data-ttu-id="be90a-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="be90a-114">-ClusterName</span></span>
<span data-ttu-id="be90a-115">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="be90a-115">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be90a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be90a-116">-DefaultProfile</span></span>
<span data-ttu-id="be90a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be90a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be90a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be90a-118">-InputObject</span></span>
<span data-ttu-id="be90a-119">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="be90a-119">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be90a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be90a-120">-ResourceGroupName</span></span>
<span data-ttu-id="be90a-121">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="be90a-121">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be90a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be90a-122">-ResourceId</span></span>
<span data-ttu-id="be90a-123">Ottiene o imposta l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be90a-123">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be90a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be90a-124">CommonParameters</span></span>
<span data-ttu-id="be90a-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be90a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be90a-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="be90a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be90a-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="be90a-127">INPUTS</span></span>

### <span data-ttu-id="be90a-128">System.String</span><span class="sxs-lookup"><span data-stu-id="be90a-128">System.String</span></span>

### <span data-ttu-id="be90a-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="be90a-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="be90a-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be90a-130">OUTPUTS</span></span>

### <span data-ttu-id="be90a-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="be90a-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="be90a-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="be90a-132">NOTES</span></span>

## <span data-ttu-id="be90a-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be90a-133">RELATED LINKS</span></span>

<span data-ttu-id="be90a-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="be90a-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
