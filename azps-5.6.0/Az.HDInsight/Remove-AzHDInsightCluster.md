---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: 5baf67bfec2c4e18e718241dbb973bb8b2050bbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965901"
---
# <span data-ttu-id="9e9ca-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9e9ca-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="9e9ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="9e9ca-103">Rimuove il cluster HDInsight specificato dalla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="9e9ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e9ca-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e9ca-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9e9ca-105">DESCRIPTION</span></span>
<span data-ttu-id="9e9ca-106">Il cmdlet **Remove-AzHDInsightCluster** rimuove il cluster di servizi HDInsight specificato da una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="9e9ca-107">Questa operazione elimina anche tutti i dati archiviati nel file system distribuito Hadoop (HDFS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="9e9ca-108">I dati archiviati nell'account di archiviazione di Azure associato non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="9e9ca-109">I dati archiviati in metastore esterni non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="9e9ca-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e9ca-110">EXAMPLES</span></span>

### <span data-ttu-id="9e9ca-111">Esempio 1: Eliminare un cluster Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="9e9ca-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="9e9ca-112">Questo comando rimuove il cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="9e9ca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e9ca-113">PARAMETERS</span></span>

### <span data-ttu-id="9e9ca-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9e9ca-114">-ClusterName</span></span>
<span data-ttu-id="9e9ca-115">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-115">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e9ca-116">-DefaultProfile</span></span>
<span data-ttu-id="9e9ca-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9e9ca-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e9ca-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e9ca-118">-PassThru</span></span>
<span data-ttu-id="9e9ca-119">Se PassThru è presente, genera l'output del risultato</span><span class="sxs-lookup"><span data-stu-id="9e9ca-119">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="9e9ca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e9ca-120">-ResourceGroupName</span></span>
<span data-ttu-id="9e9ca-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-121">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e9ca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e9ca-122">CommonParameters</span></span>
<span data-ttu-id="9e9ca-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e9ca-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e9ca-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e9ca-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="9e9ca-125">INPUTS</span></span>

### <span data-ttu-id="9e9ca-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9e9ca-126">None</span></span>
## <span data-ttu-id="9e9ca-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e9ca-127">OUTPUTS</span></span>

### <span data-ttu-id="9e9ca-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9e9ca-128">System.Boolean</span></span>
## <span data-ttu-id="9e9ca-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="9e9ca-129">NOTES</span></span>

## <span data-ttu-id="9e9ca-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e9ca-130">RELATED LINKS</span></span>

[<span data-ttu-id="9e9ca-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9e9ca-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="9e9ca-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="9e9ca-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


