---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 430c2aa7f38e6246c13ef6045f52346b580d20fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194350"
---
# <span data-ttu-id="4f1fd-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="4f1fd-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="4f1fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="4f1fd-103">Elenca gli host del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="4f1fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f1fd-104">SYNTAX</span></span>

### <span data-ttu-id="4f1fd-105">SetByNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f1fd-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f1fd-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f1fd-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f1fd-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f1fd-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4f1fd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f1fd-108">DESCRIPTION</span></span>
<span data-ttu-id="4f1fd-109">Il cmdlet **Get-AzHDInsightHost** elenca gli host del cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="4f1fd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f1fd-110">EXAMPLES</span></span>

### <span data-ttu-id="4f1fd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4f1fd-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="4f1fd-112">Questo elenco di comandi contiene gli host del cluster con il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="4f1fd-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4f1fd-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="4f1fd-114">Questo elenco di comandi degli host del cluster con pipeline.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="4f1fd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f1fd-115">PARAMETERS</span></span>

### <span data-ttu-id="4f1fd-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4f1fd-116">-ClusterName</span></span>
<span data-ttu-id="4f1fd-117">Ottiene o imposta il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f1fd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f1fd-118">-DefaultProfile</span></span>
<span data-ttu-id="4f1fd-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f1fd-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f1fd-120">-InputObject</span></span>
<span data-ttu-id="4f1fd-121">Ottiene o imposta l'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f1fd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f1fd-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f1fd-123">Ottiene o imposta il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f1fd-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f1fd-124">-ResourceId</span></span>
<span data-ttu-id="4f1fd-125">Ottiene o imposta l'ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f1fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f1fd-126">CommonParameters</span></span>
<span data-ttu-id="4f1fd-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f1fd-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f1fd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f1fd-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f1fd-129">INPUTS</span></span>

### <span data-ttu-id="4f1fd-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4f1fd-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="4f1fd-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f1fd-131">OUTPUTS</span></span>

### <span data-ttu-id="4f1fd-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="4f1fd-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="4f1fd-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f1fd-133">NOTES</span></span>

## <span data-ttu-id="4f1fd-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f1fd-134">RELATED LINKS</span></span>
