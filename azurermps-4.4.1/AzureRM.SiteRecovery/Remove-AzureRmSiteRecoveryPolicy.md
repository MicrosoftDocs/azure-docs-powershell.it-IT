---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686145"
---
# <span data-ttu-id="53159-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="53159-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="53159-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53159-102">SYNOPSIS</span></span>
<span data-ttu-id="53159-103">Rimuove un criterio di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="53159-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53159-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53159-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="53159-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53159-105">DESCRIPTION</span></span>
<span data-ttu-id="53159-106">Il cmdlet **Remove-AzureRMSiteRecoveryPolicy** rimuove un criterio di replica di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="53159-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="53159-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53159-107">EXAMPLES</span></span>

## <span data-ttu-id="53159-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53159-108">PARAMETERS</span></span>

### <span data-ttu-id="53159-109">-Policy</span><span class="sxs-lookup"><span data-stu-id="53159-109">-Policy</span></span>
<span data-ttu-id="53159-110">Specifica l'oggetto Criteri di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="53159-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53159-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53159-111">-DefaultProfile</span></span>
<span data-ttu-id="53159-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53159-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53159-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53159-113">CommonParameters</span></span>
<span data-ttu-id="53159-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53159-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53159-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53159-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53159-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53159-116">INPUTS</span></span>

### <span data-ttu-id="53159-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="53159-117">ASRPolicy</span></span>
<span data-ttu-id="53159-118">Il parametro ' Policy ' accetta il valore di tipo ' ASRPolicy ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="53159-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="53159-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53159-119">OUTPUTS</span></span>

## <span data-ttu-id="53159-120">Note</span><span class="sxs-lookup"><span data-stu-id="53159-120">NOTES</span></span>

## <span data-ttu-id="53159-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53159-121">RELATED LINKS</span></span>

[<span data-ttu-id="53159-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="53159-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="53159-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="53159-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
