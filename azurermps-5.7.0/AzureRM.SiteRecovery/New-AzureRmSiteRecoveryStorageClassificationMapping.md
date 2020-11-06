---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 86d8cc4b48342b49e807635e6fb51c5f4028b172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512263"
---
# <span data-ttu-id="eed81-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="eed81-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="eed81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eed81-102">SYNOPSIS</span></span>
<span data-ttu-id="eed81-103">Crea un mapping di classificazione dello spazio di archiviazione nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="eed81-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eed81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eed81-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eed81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eed81-105">DESCRIPTION</span></span>
<span data-ttu-id="eed81-106">Il cmdlet **New-AzureRmSiteRecoveryStorageClassificationMapping** crea un mapping di classificazione dello spazio di archiviazione nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="eed81-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="eed81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eed81-107">EXAMPLES</span></span>

## <span data-ttu-id="eed81-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eed81-108">PARAMETERS</span></span>

### <span data-ttu-id="eed81-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed81-109">-DefaultProfile</span></span>
<span data-ttu-id="eed81-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eed81-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eed81-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="eed81-111">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed81-112">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="eed81-112">-PrimaryStorageClassification</span></span>
<span data-ttu-id="eed81-113">Specifica il mapping della classificazione dello spazio di archiviazione principale.</span><span class="sxs-lookup"><span data-stu-id="eed81-113">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eed81-114">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="eed81-114">-RecoveryStorageClassification</span></span>
<span data-ttu-id="eed81-115">Specifica un mapping di classificazione dello storage di ripristino.</span><span class="sxs-lookup"><span data-stu-id="eed81-115">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed81-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed81-116">CommonParameters</span></span>
<span data-ttu-id="eed81-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed81-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed81-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eed81-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed81-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eed81-119">INPUTS</span></span>

### <span data-ttu-id="eed81-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="eed81-120">ASRStorageClassification</span></span>
<span data-ttu-id="eed81-121">Il parametro ' PrimaryStorageClassification ' accetta il valore di tipo ' ASRStorageClassification ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="eed81-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="eed81-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eed81-122">OUTPUTS</span></span>

### <span data-ttu-id="eed81-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="eed81-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="eed81-124">Note</span><span class="sxs-lookup"><span data-stu-id="eed81-124">NOTES</span></span>

## <span data-ttu-id="eed81-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eed81-125">RELATED LINKS</span></span>

[<span data-ttu-id="eed81-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="eed81-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="eed81-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="eed81-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
