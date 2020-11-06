---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: FA154E07-EA26-4688-986E-C53C3A9E4F06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightCluster.md
ms.openlocfilehash: 81f25eeb8d0e6b704c4ee6ef71cd2aebcf3624ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519178"
---
# <span data-ttu-id="05af3-101">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="05af3-101">Get-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="05af3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05af3-102">SYNOPSIS</span></span>
<span data-ttu-id="05af3-103">Ottiene ed elenca tutti i cluster di Azure HDInsight associati all'abbonamento corrente o a un gruppo di risorse specificato oppure recupera un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="05af3-103">Gets and lists all of the Azure HDInsight clusters associated with the current subscription or a specified resource group, or retrieves a specific cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05af3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05af3-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightCluster [[-ResourceGroupName] <String>] [[-ClusterName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05af3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05af3-105">DESCRIPTION</span></span>
<span data-ttu-id="05af3-106">Il cmdlet **Get-AzureRmHDInsightCluster** elenca i cluster di servizi di Azure HDInsight per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="05af3-106">The **Get-AzureRmHDInsightCluster** cmdlet lists the Azure HDInsight service clusters for the current subscription.</span></span>
<span data-ttu-id="05af3-107">Usa il parametro *clustername* per ottenere informazioni dettagliate su un cluster specifico.</span><span class="sxs-lookup"><span data-stu-id="05af3-107">Use the *ClusterName* parameter to get details for a specific cluster.</span></span>

## <span data-ttu-id="05af3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05af3-108">EXAMPLES</span></span>

### <span data-ttu-id="05af3-109">Esempio 1: elenca tutti i cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="05af3-109">Example 1: List all Azure HDInsight clusters</span></span>
```
PS C:\>Get-AzureRmHDInsightCluster
```

<span data-ttu-id="05af3-110">Questo comando elenca tutti i cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="05af3-110">This command lists all the Azure HDInsight clusters.</span></span>

## <span data-ttu-id="05af3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05af3-111">PARAMETERS</span></span>

### <span data-ttu-id="05af3-112">-Clustername</span><span class="sxs-lookup"><span data-stu-id="05af3-112">-ClusterName</span></span>
<span data-ttu-id="05af3-113">Specifica il nome del cluster.</span><span class="sxs-lookup"><span data-stu-id="05af3-113">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="05af3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05af3-114">-ResourceGroupName</span></span>
<span data-ttu-id="05af3-115">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="05af3-115">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="05af3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05af3-116">-DefaultProfile</span></span>
<span data-ttu-id="05af3-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05af3-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05af3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05af3-118">CommonParameters</span></span>
<span data-ttu-id="05af3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05af3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05af3-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05af3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05af3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05af3-121">INPUTS</span></span>

## <span data-ttu-id="05af3-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05af3-122">OUTPUTS</span></span>

### <span data-ttu-id="05af3-123">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster]</span><span class="sxs-lookup"><span data-stu-id="05af3-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster]</span></span>

## <span data-ttu-id="05af3-124">Note</span><span class="sxs-lookup"><span data-stu-id="05af3-124">NOTES</span></span>

## <span data-ttu-id="05af3-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05af3-125">RELATED LINKS</span></span>

[<span data-ttu-id="05af3-126">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="05af3-126">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)

[<span data-ttu-id="05af3-127">Usare-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="05af3-127">Use-AzureRmHDInsightCluster</span></span>](./Use-AzureRmHDInsightCluster.md)


