---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/get-azurermhdinsightproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightProperties.md
ms.openlocfilehash: 4b3437f9df1be7e458aaa528769de406d755a071
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519466"
---
# <span data-ttu-id="944bb-101">Get-AzureRmHDInsightProperties</span><span class="sxs-lookup"><span data-stu-id="944bb-101">Get-AzureRmHDInsightProperties</span></span>

## <span data-ttu-id="944bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="944bb-102">SYNOPSIS</span></span>
<span data-ttu-id="944bb-103">Ottiene le proprietà relative al servizio HDInsight, ad esempio posizioni e capacità disponibili.</span><span class="sxs-lookup"><span data-stu-id="944bb-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="944bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="944bb-104">SYNTAX</span></span>

```
Get-AzureRmHDInsightProperties [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="944bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="944bb-105">DESCRIPTION</span></span>
<span data-ttu-id="944bb-106">Il cmdlet **Get-AzureRmHDInsightProperties** ottiene le proprietà specifiche di Azure HDInsight, ad esempio l'elenco di posizioni disponibili, le versioni di cluster HDInsight e la capacità di calcolo disponibile.</span><span class="sxs-lookup"><span data-stu-id="944bb-106">The **Get-AzureRmHDInsightProperties** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="944bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="944bb-107">EXAMPLES</span></span>

### <span data-ttu-id="944bb-108">Esempio 1: ottenere le proprietà di un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="944bb-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzureRmHDInsightProperties -Location "East US 2"
```

<span data-ttu-id="944bb-109">Questo comando consente di ottenere le proprietà da un servizio HDInsight dalla posizione East US 2.</span><span class="sxs-lookup"><span data-stu-id="944bb-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="944bb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="944bb-110">PARAMETERS</span></span>

### <span data-ttu-id="944bb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="944bb-111">-DefaultProfile</span></span>
<span data-ttu-id="944bb-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="944bb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="944bb-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="944bb-113">-Location</span></span>
<span data-ttu-id="944bb-114">Specifica la posizione per cui recuperare le proprietà di HDInsight.</span><span class="sxs-lookup"><span data-stu-id="944bb-114">Specifies the location for which to fetch HDInsight properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="944bb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="944bb-115">CommonParameters</span></span>
<span data-ttu-id="944bb-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="944bb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="944bb-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="944bb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="944bb-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="944bb-118">INPUTS</span></span>

### <span data-ttu-id="944bb-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="944bb-119">None</span></span>
<span data-ttu-id="944bb-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="944bb-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="944bb-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="944bb-121">OUTPUTS</span></span>

### <span data-ttu-id="944bb-122">Microsoft. Azure. Management. HDInsight. Models. CapabilitiesResponse</span><span class="sxs-lookup"><span data-stu-id="944bb-122">Microsoft.Azure.Management.HDInsight.Models.CapabilitiesResponse</span></span>

## <span data-ttu-id="944bb-123">Note</span><span class="sxs-lookup"><span data-stu-id="944bb-123">NOTES</span></span>

## <span data-ttu-id="944bb-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="944bb-124">RELATED LINKS</span></span>

