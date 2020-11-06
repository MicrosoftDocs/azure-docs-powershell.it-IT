---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507964"
---
# <span data-ttu-id="730c1-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="730c1-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="730c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="730c1-102">SYNOPSIS</span></span>
<span data-ttu-id="730c1-103">Crea un tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="730c1-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="730c1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="730c1-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="730c1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="730c1-105">DESCRIPTION</span></span>
<span data-ttu-id="730c1-106">Il cmdlet **New-AzureRmSiteRecoveryFabric** crea un tessuto di recupero del sito di Azure del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="730c1-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="730c1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="730c1-107">EXAMPLES</span></span>

## <span data-ttu-id="730c1-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="730c1-108">PARAMETERS</span></span>

### <span data-ttu-id="730c1-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="730c1-109">-DefaultProfile</span></span>
<span data-ttu-id="730c1-110">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="730c1-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="730c1-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="730c1-111">-Name</span></span>
<span data-ttu-id="730c1-112">Specifica il nome del tessuto di ripristino del sito di Azure</span><span class="sxs-lookup"><span data-stu-id="730c1-112">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="730c1-113">-Digitare</span><span class="sxs-lookup"><span data-stu-id="730c1-113">-Type</span></span>
<span data-ttu-id="730c1-114">Specifica il tipo di tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="730c1-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="730c1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="730c1-115">CommonParameters</span></span>
<span data-ttu-id="730c1-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="730c1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="730c1-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="730c1-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="730c1-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="730c1-118">INPUTS</span></span>

### <span data-ttu-id="730c1-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="730c1-119">None</span></span>
<span data-ttu-id="730c1-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="730c1-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="730c1-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="730c1-121">OUTPUTS</span></span>

### <span data-ttu-id="730c1-122">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="730c1-122">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="730c1-123">Note</span><span class="sxs-lookup"><span data-stu-id="730c1-123">NOTES</span></span>

## <span data-ttu-id="730c1-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="730c1-124">RELATED LINKS</span></span>

[<span data-ttu-id="730c1-125">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="730c1-125">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="730c1-126">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="730c1-126">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
