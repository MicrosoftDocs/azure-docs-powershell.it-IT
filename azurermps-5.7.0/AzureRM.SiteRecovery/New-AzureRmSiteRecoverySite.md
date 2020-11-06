---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517936"
---
# <span data-ttu-id="ff6c2-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ff6c2-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="ff6c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ff6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ff6c2-103">Crea un sito di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff6c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ff6c2-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff6c2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff6c2-105">DESCRIPTION</span></span>
<span data-ttu-id="ff6c2-106">Il cmdlet **New-AzureRmSiteRecoverySite** crea un sito di ripristino di Azure sito nel Vault corrente.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="ff6c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ff6c2-107">EXAMPLES</span></span>

## <span data-ttu-id="ff6c2-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ff6c2-108">PARAMETERS</span></span>

### <span data-ttu-id="ff6c2-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff6c2-109">-DefaultProfile</span></span>
<span data-ttu-id="ff6c2-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff6c2-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="ff6c2-111">-Name</span></span>
<span data-ttu-id="ff6c2-112">Specifica il nome del sito.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff6c2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff6c2-113">CommonParameters</span></span>
<span data-ttu-id="ff6c2-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff6c2-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff6c2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff6c2-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ff6c2-116">INPUTS</span></span>

### <span data-ttu-id="ff6c2-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ff6c2-117">None</span></span>
<span data-ttu-id="ff6c2-118">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ff6c2-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff6c2-119">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ff6c2-119">OUTPUTS</span></span>

## <span data-ttu-id="ff6c2-120">Note</span><span class="sxs-lookup"><span data-stu-id="ff6c2-120">NOTES</span></span>

## <span data-ttu-id="ff6c2-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ff6c2-121">RELATED LINKS</span></span>

[<span data-ttu-id="ff6c2-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ff6c2-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="ff6c2-123">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="ff6c2-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
