---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2520dd90eed1362f4d499eb88ce88dec33f1338c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510300"
---
# <span data-ttu-id="ab313-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ab313-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="ab313-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab313-102">SYNOPSIS</span></span>
<span data-ttu-id="ab313-103">Crea un mapping di classificazione dello spazio di archiviazione nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="ab313-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab313-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab313-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab313-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab313-105">DESCRIPTION</span></span>
<span data-ttu-id="ab313-106">Il cmdlet **New-AzureRmSiteRecoveryStorageClassificationMapping** crea un mapping di classificazione dello spazio di archiviazione nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab313-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="ab313-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab313-107">EXAMPLES</span></span>

## <span data-ttu-id="ab313-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab313-108">PARAMETERS</span></span>

### <span data-ttu-id="ab313-109">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab313-109">-Name</span></span>
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

### <span data-ttu-id="ab313-110">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ab313-110">-PrimaryStorageClassification</span></span>
<span data-ttu-id="ab313-111">Specifica il mapping della classificazione dello spazio di archiviazione principale.</span><span class="sxs-lookup"><span data-stu-id="ab313-111">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab313-112">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ab313-112">-RecoveryStorageClassification</span></span>
<span data-ttu-id="ab313-113">Specifica un mapping di classificazione dello storage di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ab313-113">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab313-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab313-114">-DefaultProfile</span></span>
<span data-ttu-id="ab313-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab313-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab313-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab313-116">CommonParameters</span></span>
<span data-ttu-id="ab313-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab313-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab313-118">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab313-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab313-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab313-119">INPUTS</span></span>

### <span data-ttu-id="ab313-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="ab313-120">ASRStorageClassification</span></span>
<span data-ttu-id="ab313-121">Il parametro ' PrimaryStorageClassification ' accetta il valore di tipo ' ASRStorageClassification ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ab313-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="ab313-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab313-122">OUTPUTS</span></span>

### <span data-ttu-id="ab313-123">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ab313-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ab313-124">Note</span><span class="sxs-lookup"><span data-stu-id="ab313-124">NOTES</span></span>

## <span data-ttu-id="ab313-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab313-125">RELATED LINKS</span></span>

[<span data-ttu-id="ab313-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ab313-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="ab313-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="ab313-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
