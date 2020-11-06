---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverystorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2d215afda7c2c26aa178421fb52ddaff8c6ac831
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517932"
---
# <span data-ttu-id="d36d1-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d36d1-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="d36d1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d36d1-102">SYNOPSIS</span></span>
<span data-ttu-id="d36d1-103">Rimuove un mapping di classificazione dello spazio di archiviazione dal ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="d36d1-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d36d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d36d1-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d36d1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d36d1-105">DESCRIPTION</span></span>
<span data-ttu-id="d36d1-106">Il cmdlet **Remove-AzureRmSiteRecoveryStorageClassificationMapping** rimuove un mapping di classificazione dello spazio di archiviazione dal ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="d36d1-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="d36d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d36d1-107">EXAMPLES</span></span>

## <span data-ttu-id="d36d1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d36d1-108">PARAMETERS</span></span>

### <span data-ttu-id="d36d1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d36d1-109">-DefaultProfile</span></span>
<span data-ttu-id="d36d1-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d36d1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d36d1-111">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d36d1-111">-StorageClassificationMapping</span></span>
<span data-ttu-id="d36d1-112">Specifica un mapping di classificazione dello spazio di archiviazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d36d1-112">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d36d1-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d36d1-113">CommonParameters</span></span>
<span data-ttu-id="d36d1-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d36d1-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d36d1-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d36d1-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d36d1-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d36d1-116">INPUTS</span></span>

### <span data-ttu-id="d36d1-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d36d1-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="d36d1-118">Il parametro ' StorageClassificationMapping ' accetta il valore di tipo ' ASRStorageClassificationMapping ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d36d1-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="d36d1-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d36d1-119">OUTPUTS</span></span>

### <span data-ttu-id="d36d1-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d36d1-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d36d1-121">Note</span><span class="sxs-lookup"><span data-stu-id="d36d1-121">NOTES</span></span>

## <span data-ttu-id="d36d1-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d36d1-122">RELATED LINKS</span></span>

[<span data-ttu-id="d36d1-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d36d1-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="d36d1-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="d36d1-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
