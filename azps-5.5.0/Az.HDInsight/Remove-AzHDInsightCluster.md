---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 87B3C102-0A8C-4FFA-8429-594D2360AC32
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightCluster.md
ms.openlocfilehash: ab97162fb2651bce8e242ca0cef7b497ffcf1bef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200207"
---
# <span data-ttu-id="8baff-101">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8baff-101">Remove-AzHDInsightCluster</span></span>

## <span data-ttu-id="8baff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8baff-102">SYNOPSIS</span></span>
<span data-ttu-id="8baff-103">Rimuove il cluster HDInsight specificato dalla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="8baff-103">Removes the specified HDInsight cluster from the current subscription.</span></span>

## <span data-ttu-id="8baff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8baff-104">SYNTAX</span></span>

```
Remove-AzHDInsightCluster [-ClusterName] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8baff-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8baff-105">DESCRIPTION</span></span>
<span data-ttu-id="8baff-106">Il cmdlet **Remove-AzHDInsightCluster** rimuove il cluster di servizi HDInsight specificato da una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8baff-106">The **Remove-AzHDInsightCluster** cmdlet removes the specified HDInsight service cluster from a subscription.</span></span>
<span data-ttu-id="8baff-107">Questa operazione elimina anche tutti i dati archiviati nel file system distribuito Hadoop (HDFS) nel cluster.</span><span class="sxs-lookup"><span data-stu-id="8baff-107">This operation also deletes any data stored in the Hadoop Distributed File System (HDFS) on the cluster.</span></span>
<span data-ttu-id="8baff-108">I dati archiviati nell'account di archiviazione di Azure associato non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="8baff-108">Data stored in the associated Azure Storage account is not deleted.</span></span>
<span data-ttu-id="8baff-109">I dati archiviati in metastore esterni non vengono eliminati.</span><span class="sxs-lookup"><span data-stu-id="8baff-109">Data stored in external metastores is not deleted.</span></span>

## <span data-ttu-id="8baff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8baff-110">EXAMPLES</span></span>

### <span data-ttu-id="8baff-111">Esempio 1: Eliminare un cluster Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="8baff-111">Example 1: Delete an Azure HDInsight cluster</span></span>
```
PS C:\>Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

<span data-ttu-id="8baff-112">Questo comando rimuove il cluster denominato your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="8baff-112">This command removes the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="8baff-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8baff-113">PARAMETERS</span></span>

### <span data-ttu-id="8baff-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8baff-114">-ClusterName</span></span>
<span data-ttu-id="8baff-115">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="8baff-115">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="8baff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8baff-116">-DefaultProfile</span></span>
<span data-ttu-id="8baff-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8baff-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8baff-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8baff-118">-PassThru</span></span>
<span data-ttu-id="8baff-119">Se PassThru è presente, restituisce il risultato</span><span class="sxs-lookup"><span data-stu-id="8baff-119">If PassThru is present, output the result</span></span>

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

### <span data-ttu-id="8baff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8baff-120">-ResourceGroupName</span></span>
<span data-ttu-id="8baff-121">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8baff-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8baff-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8baff-122">CommonParameters</span></span>
<span data-ttu-id="8baff-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8baff-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8baff-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8baff-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8baff-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="8baff-125">INPUTS</span></span>

### <span data-ttu-id="8baff-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8baff-126">None</span></span>
## <span data-ttu-id="8baff-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8baff-127">OUTPUTS</span></span>

### <span data-ttu-id="8baff-128">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8baff-128">System.Boolean</span></span>
## <span data-ttu-id="8baff-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="8baff-129">NOTES</span></span>

## <span data-ttu-id="8baff-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8baff-130">RELATED LINKS</span></span>

[<span data-ttu-id="8baff-131">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8baff-131">Get-AzHDInsightCluster</span></span>](./Get-AzHDInsightCluster.md)

[<span data-ttu-id="8baff-132">Use-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8baff-132">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


