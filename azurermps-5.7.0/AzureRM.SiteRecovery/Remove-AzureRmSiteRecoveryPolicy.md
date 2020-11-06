---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507960"
---
# <span data-ttu-id="5ef28-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5ef28-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="5ef28-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ef28-102">SYNOPSIS</span></span>
<span data-ttu-id="5ef28-103">Rimuove un criterio di replica del ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="5ef28-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ef28-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ef28-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ef28-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ef28-105">DESCRIPTION</span></span>
<span data-ttu-id="5ef28-106">Il cmdlet **Remove-AzureRMSiteRecoveryPolicy** rimuove un criterio di replica di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="5ef28-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="5ef28-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ef28-107">EXAMPLES</span></span>

## <span data-ttu-id="5ef28-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ef28-108">PARAMETERS</span></span>

### <span data-ttu-id="5ef28-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ef28-109">-DefaultProfile</span></span>
<span data-ttu-id="5ef28-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ef28-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ef28-111">-Policy</span><span class="sxs-lookup"><span data-stu-id="5ef28-111">-Policy</span></span>
<span data-ttu-id="5ef28-112">Specifica l'oggetto Criteri di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="5ef28-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ef28-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ef28-113">CommonParameters</span></span>
<span data-ttu-id="5ef28-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ef28-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ef28-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ef28-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ef28-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ef28-116">INPUTS</span></span>

### <span data-ttu-id="5ef28-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="5ef28-117">ASRPolicy</span></span>
<span data-ttu-id="5ef28-118">Il parametro ' Policy ' accetta il valore di tipo ' ASRPolicy ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5ef28-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="5ef28-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ef28-119">OUTPUTS</span></span>

## <span data-ttu-id="5ef28-120">Note</span><span class="sxs-lookup"><span data-stu-id="5ef28-120">NOTES</span></span>

## <span data-ttu-id="5ef28-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ef28-121">RELATED LINKS</span></span>

[<span data-ttu-id="5ef28-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5ef28-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="5ef28-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="5ef28-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
