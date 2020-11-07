---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865465"
---
# <span data-ttu-id="69393-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="69393-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="69393-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69393-102">SYNOPSIS</span></span>
<span data-ttu-id="69393-103">Ottiene le proprietà relative al servizio HDInsight, ad esempio posizioni e capacità disponibili.</span><span class="sxs-lookup"><span data-stu-id="69393-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="69393-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69393-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69393-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69393-105">DESCRIPTION</span></span>
<span data-ttu-id="69393-106">Il cmdlet **Get-AzHDInsightProperty** ottiene le proprietà specifiche di Azure HDInsight, ad esempio l'elenco di posizioni disponibili, le versioni di cluster HDInsight e la capacità di calcolo disponibile.</span><span class="sxs-lookup"><span data-stu-id="69393-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="69393-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69393-107">EXAMPLES</span></span>

### <span data-ttu-id="69393-108">Esempio 1: ottenere le proprietà di un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="69393-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="69393-109">Questo comando consente di ottenere le proprietà da un servizio HDInsight dalla posizione East US 2.</span><span class="sxs-lookup"><span data-stu-id="69393-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="69393-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69393-110">PARAMETERS</span></span>

### <span data-ttu-id="69393-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69393-111">-DefaultProfile</span></span>
<span data-ttu-id="69393-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="69393-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69393-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="69393-113">-Location</span></span>
<span data-ttu-id="69393-114">Specifica la posizione per cui recuperare le proprietà di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="69393-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="69393-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69393-115">CommonParameters</span></span>
<span data-ttu-id="69393-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69393-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69393-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69393-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69393-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69393-118">INPUTS</span></span>

### <span data-ttu-id="69393-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="69393-119">None</span></span>
## <span data-ttu-id="69393-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69393-120">OUTPUTS</span></span>

### <span data-ttu-id="69393-121">Microsoft. Azure. Management. HDInsight. Models. AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="69393-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="69393-122">Note</span><span class="sxs-lookup"><span data-stu-id="69393-122">NOTES</span></span>

## <span data-ttu-id="69393-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69393-123">RELATED LINKS</span></span>
