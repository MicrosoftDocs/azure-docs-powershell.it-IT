---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightCluster.md
ms.openlocfilehash: ff789a04be2a6f448d4850891f368cbb7ca91c4b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865470"
---
# <span data-ttu-id="f01ce-101">Get-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f01ce-101">Get-AzHDInsightCluster</span></span>

## <span data-ttu-id="f01ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f01ce-102">SYNOPSIS</span></span>
<span data-ttu-id="f01ce-103">Ottiene ed elenca tutti i cluster di Azure HDInsight associati all'abbonamento corrente o a un gruppo di risorse specificato oppure recupera un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="f01ce-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

## <span data-ttu-id="f01ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f01ce-104">SYNTAX</span></span>

```
Get-AzHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f01ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f01ce-105">DESCRIPTION</span></span>
<span data-ttu-id="f01ce-106">Il cmdlet **Get-AzHDInsightCluster** elenca i cluster di servizi di Azure HDInsight per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="f01ce-106">The **Get-AzHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="f01ce-107">Usa il parametro *clustername* per ottenere informazioni dettagliate su un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="f01ce-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="f01ce-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f01ce-108">EXAMPLES</span></span>

### <span data-ttu-id="f01ce-109">Esempio 1: elenca tutti i cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="f01ce-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzHDInsightCluster
```

<span data-ttu-id="f01ce-110">Questo comando elenca tutti i cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="f01ce-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="f01ce-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f01ce-111">PARAMETERS</span></span>

### <span data-ttu-id="f01ce-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="f01ce-112">-ClusterName</span></span>
<span data-ttu-id="f01ce-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="f01ce-113">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f01ce-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f01ce-114">-DefaultProfile</span></span>
<span data-ttu-id="f01ce-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f01ce-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f01ce-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f01ce-116">-ResourceGroupName</span></span>
<span data-ttu-id="f01ce-117">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f01ce-117">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f01ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f01ce-118">CommonParameters</span></span>
<span data-ttu-id="f01ce-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f01ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f01ce-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f01ce-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f01ce-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f01ce-121">INPUTS</span></span>

### <span data-ttu-id="f01ce-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f01ce-122">None</span></span>

## <span data-ttu-id="f01ce-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f01ce-123">OUTPUTS</span></span>

### <span data-ttu-id="f01ce-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f01ce-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="f01ce-125">Note</span><span class="sxs-lookup"><span data-stu-id="f01ce-125">NOTES</span></span>

## <span data-ttu-id="f01ce-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f01ce-126">RELATED LINKS</span></span>

[<span data-ttu-id="f01ce-127">Remove-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f01ce-127">Remove-AzHDInsightCluster</span></span>](./Remove-AzHDInsightCluster.md)

[<span data-ttu-id="f01ce-128">Usare-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="f01ce-128">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


