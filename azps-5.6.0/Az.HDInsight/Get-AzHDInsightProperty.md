---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009086"
---
# <span data-ttu-id="c27e6-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="c27e6-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="c27e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c27e6-102">SYNOPSIS</span></span>
<span data-ttu-id="c27e6-103">Ottiene le proprietà relative al servizio HDInsight, ad esempio le posizioni disponibili e la capacità.</span><span class="sxs-lookup"><span data-stu-id="c27e6-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="c27e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c27e6-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c27e6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c27e6-105">DESCRIPTION</span></span>
<span data-ttu-id="c27e6-106">Il cmdlet **Get-AzHDInsightProperty** ottiene proprietà specifiche di Azure HDInsight, ad esempio l'elenco delle posizioni disponibili, le versioni del cluster HDInsight e la capacità di calcolo disponibile.</span><span class="sxs-lookup"><span data-stu-id="c27e6-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="c27e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c27e6-107">EXAMPLES</span></span>

### <span data-ttu-id="c27e6-108">Esempio 1: Ottenere le proprietà di un cluster Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="c27e6-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="c27e6-109">Questo comando recupera le proprietà da un servizio HDInsight dalla località Stati Uniti orientali 2.</span><span class="sxs-lookup"><span data-stu-id="c27e6-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="c27e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c27e6-110">PARAMETERS</span></span>

### <span data-ttu-id="c27e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c27e6-111">-DefaultProfile</span></span>
<span data-ttu-id="c27e6-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c27e6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c27e6-113">-Location</span><span class="sxs-lookup"><span data-stu-id="c27e6-113">-Location</span></span>
<span data-ttu-id="c27e6-114">Specifica la posizione per cui recuperare le proprietà HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c27e6-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="c27e6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c27e6-115">CommonParameters</span></span>
<span data-ttu-id="c27e6-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c27e6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c27e6-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c27e6-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c27e6-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="c27e6-118">INPUTS</span></span>

### <span data-ttu-id="c27e6-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c27e6-119">None</span></span>
## <span data-ttu-id="c27e6-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c27e6-120">OUTPUTS</span></span>

### <span data-ttu-id="c27e6-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="c27e6-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="c27e6-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="c27e6-122">NOTES</span></span>

## <span data-ttu-id="c27e6-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c27e6-123">RELATED LINKS</span></span>
