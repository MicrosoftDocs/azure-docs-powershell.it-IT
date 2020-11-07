---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 59ae0324a5e42e87192e655352fce074413907ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686777"
---
# <span data-ttu-id="9a4c9-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9a4c9-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="9a4c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a4c9-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4c9-103">Rimuove un mapping di classificazione dello spazio di archiviazione dal ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="9a4c9-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a4c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a4c9-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a4c9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a4c9-105">DESCRIPTION</span></span>
<span data-ttu-id="9a4c9-106">Il cmdlet **Remove-AzureRmSiteRecoveryStorageClassificationMapping** rimuove un mapping di classificazione dello spazio di archiviazione dal ripristino del sito Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4c9-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="9a4c9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a4c9-107">EXAMPLES</span></span>

## <span data-ttu-id="9a4c9-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a4c9-108">PARAMETERS</span></span>

### <span data-ttu-id="9a4c9-109">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9a4c9-109">-StorageClassificationMapping</span></span>
<span data-ttu-id="9a4c9-110">Specifica un mapping di classificazione dello spazio di archiviazione rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a4c9-110">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4c9-111">-DefaultProfile</span></span>
<span data-ttu-id="9a4c9-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a4c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a4c9-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4c9-113">CommonParameters</span></span>
<span data-ttu-id="9a4c9-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a4c9-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4c9-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4c9-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4c9-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a4c9-116">INPUTS</span></span>

### <span data-ttu-id="9a4c9-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9a4c9-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="9a4c9-118">Il parametro ' StorageClassificationMapping ' accetta il valore di tipo ' ASRStorageClassificationMapping ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9a4c9-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="9a4c9-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a4c9-119">OUTPUTS</span></span>

### <span data-ttu-id="9a4c9-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9a4c9-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9a4c9-121">Note</span><span class="sxs-lookup"><span data-stu-id="9a4c9-121">NOTES</span></span>

## <span data-ttu-id="9a4c9-122">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a4c9-122">RELATED LINKS</span></span>

[<span data-ttu-id="9a4c9-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9a4c9-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="9a4c9-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="9a4c9-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
