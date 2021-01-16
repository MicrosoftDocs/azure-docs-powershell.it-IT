---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8CD55A33-5964-409A-BDA5-EDAE9A21E0C1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 91e5a0fbb92ced1c79717aecb01d5896bb422280
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357318"
---
# <span data-ttu-id="09496-101">Get-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="09496-101">Get-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="09496-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09496-102">SYNOPSIS</span></span>
<span data-ttu-id="09496-103">Ottiene la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="09496-103">Gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="09496-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09496-104">SYNTAX</span></span>

### <span data-ttu-id="09496-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09496-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09496-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09496-106">GetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="09496-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09496-107">GetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09496-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09496-108">DESCRIPTION</span></span>
<span data-ttu-id="09496-109">Il cmdlet **Get-AzHDInsightClusterAutoscaleConfiguration** ottiene la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="09496-109">The **Get-AzHDInsightClusterAutoscaleConfiguration** cmdlet gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="09496-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09496-110">EXAMPLES</span></span>

### <span data-ttu-id="09496-111">Esempio 1: ottenere la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="09496-111">Example 1: Get the autoscale configuration of HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Get-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="09496-112">Questo comando consente di ottenere la configurazione di scala automatica del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="09496-112">This command gets the autoscale configuration of HDInsight cluster.</span></span>

## <span data-ttu-id="09496-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09496-113">PARAMETERS</span></span>

### <span data-ttu-id="09496-114">-Clustername</span><span class="sxs-lookup"><span data-stu-id="09496-114">-ClusterName</span></span>
<span data-ttu-id="09496-115">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="09496-115">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="09496-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09496-116">-DefaultProfile</span></span>
<span data-ttu-id="09496-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09496-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09496-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09496-118">-InputObject</span></span>
<span data-ttu-id="09496-119">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="09496-119">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="09496-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09496-120">-ResourceGroupName</span></span>
<span data-ttu-id="09496-121">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09496-121">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="09496-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09496-122">-ResourceId</span></span>
<span data-ttu-id="09496-123">Ottiene o imposta l'ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="09496-123">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="09496-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09496-124">CommonParameters</span></span>
<span data-ttu-id="09496-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09496-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09496-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09496-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09496-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09496-127">INPUTS</span></span>

### <span data-ttu-id="09496-128">System. String</span><span class="sxs-lookup"><span data-stu-id="09496-128">System.String</span></span>

### <span data-ttu-id="09496-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="09496-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="09496-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09496-130">OUTPUTS</span></span>

### <span data-ttu-id="09496-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightAutoscale</span><span class="sxs-lookup"><span data-stu-id="09496-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale</span></span>

## <span data-ttu-id="09496-132">Note</span><span class="sxs-lookup"><span data-stu-id="09496-132">NOTES</span></span>

## <span data-ttu-id="09496-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09496-133">RELATED LINKS</span></span>

<span data-ttu-id="09496-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="09496-134">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Remove-AzHDInsightClusterAutoscaleConfiguration](./Remove-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
