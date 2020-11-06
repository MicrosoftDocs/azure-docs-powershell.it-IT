---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: f232d1df7bef3800fc54b2469a51f3f69c8d4fa8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515303"
---
# <span data-ttu-id="903a4-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="903a4-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="903a4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="903a4-102">SYNOPSIS</span></span>
<span data-ttu-id="903a4-103">Ottiene ed elenca tutti i cluster di Azure HDInsight associati all'abbonamento corrente o a un gruppo di risorse specificato oppure recupera un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="903a4-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903a4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="903a4-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="903a4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="903a4-105">DESCRIPTION</span></span>
<span data-ttu-id="903a4-106">Il cmdlet **Get-AzureRmHDInsightCluster** elenca i cluster di servizi di Azure HDInsight per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="903a4-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="903a4-107">Usa il parametro *clustername* per ottenere informazioni dettagliate su un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="903a4-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="903a4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="903a4-108">EXAMPLES</span></span>

### <span data-ttu-id="903a4-109">Esempio 1: elenca tutti i cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="903a4-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="903a4-110">Questo comando elenca tutti i cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="903a4-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="903a4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="903a4-111">PARAMETERS</span></span>

### <span data-ttu-id="903a4-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="903a4-112">-ClusterName</span></span>
<span data-ttu-id="903a4-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="903a4-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="903a4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903a4-114">-DefaultProfile</span></span>
<span data-ttu-id="903a4-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="903a4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903a4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="903a4-116">-ResourceGroupName</span></span>
<span data-ttu-id="903a4-117">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="903a4-117">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="903a4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903a4-118">CommonParameters</span></span>
<span data-ttu-id="903a4-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903a4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903a4-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903a4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903a4-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="903a4-121">INPUTS</span></span>

### <span data-ttu-id="903a4-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="903a4-122">None</span></span>

## <span data-ttu-id="903a4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="903a4-123">OUTPUTS</span></span>

### <span data-ttu-id="903a4-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="903a4-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="903a4-125">Note</span><span class="sxs-lookup"><span data-stu-id="903a4-125">NOTES</span></span>

## <span data-ttu-id="903a4-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="903a4-126">RELATED LINKS</span></span>

[<span data-ttu-id="903a4-127">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="903a4-127">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="903a4-128">Usare-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="903a4-128">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


