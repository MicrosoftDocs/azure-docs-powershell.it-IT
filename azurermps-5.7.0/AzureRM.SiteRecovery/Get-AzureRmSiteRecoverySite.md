---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 4a710507321d2f4eb2a605846928f66c5bdb6a4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687438"
---
# <span data-ttu-id="fbba1-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="fbba1-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="fbba1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fbba1-102">SYNOPSIS</span></span>
<span data-ttu-id="fbba1-103">Ottiene i siti Hyper-V dall'archivio di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="fbba1-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fbba1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbba1-104">SYNTAX</span></span>

### <span data-ttu-id="fbba1-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fbba1-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbba1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="fbba1-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fbba1-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="fbba1-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbba1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fbba1-108">DESCRIPTION</span></span>
<span data-ttu-id="fbba1-109">Il cmdlet **Get-AzureRmSiteRecoverySite** ottiene i siti Hyper-V nel Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="fbba1-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="fbba1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbba1-110">EXAMPLES</span></span>

## <span data-ttu-id="fbba1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fbba1-111">PARAMETERS</span></span>

### <span data-ttu-id="fbba1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbba1-112">-DefaultProfile</span></span>
<span data-ttu-id="fbba1-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbba1-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbba1-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="fbba1-114">-FriendlyName</span></span>
<span data-ttu-id="fbba1-115">Specifica il nome descrittivo del sito.</span><span class="sxs-lookup"><span data-stu-id="fbba1-115">Specifies the friendly name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbba1-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fbba1-116">-Name</span></span>
<span data-ttu-id="fbba1-117">Specifica il nome del sito.</span><span class="sxs-lookup"><span data-stu-id="fbba1-117">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbba1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbba1-118">CommonParameters</span></span>
<span data-ttu-id="fbba1-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbba1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbba1-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbba1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbba1-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fbba1-121">INPUTS</span></span>

### <span data-ttu-id="fbba1-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fbba1-122">None</span></span>
<span data-ttu-id="fbba1-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fbba1-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fbba1-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbba1-124">OUTPUTS</span></span>

### <span data-ttu-id="fbba1-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="fbba1-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="fbba1-126">Note</span><span class="sxs-lookup"><span data-stu-id="fbba1-126">NOTES</span></span>

## <span data-ttu-id="fbba1-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbba1-127">RELATED LINKS</span></span>

[<span data-ttu-id="fbba1-128">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="fbba1-128">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="fbba1-129">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="fbba1-129">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
