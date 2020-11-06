---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520362"
---
# <span data-ttu-id="9e1ae-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9e1ae-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="9e1ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e1ae-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1ae-103">Ottiene le informazioni sui provider di ripristino di Azure sito nel Vault.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e1ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e1ae-104">SYNTAX</span></span>

### <span data-ttu-id="9e1ae-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e1ae-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e1ae-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9e1ae-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e1ae-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="9e1ae-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e1ae-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e1ae-108">DESCRIPTION</span></span>
<span data-ttu-id="9e1ae-109">Il cmdlet **Get-AzureRmSiteRecoveryServicesProvider** ottiene le informazioni sui provider di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="9e1ae-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e1ae-110">EXAMPLES</span></span>

## <span data-ttu-id="9e1ae-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e1ae-111">PARAMETERS</span></span>

### <span data-ttu-id="9e1ae-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1ae-112">-DefaultProfile</span></span>
<span data-ttu-id="9e1ae-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1ae-114">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="9e1ae-114">-Fabric</span></span>
<span data-ttu-id="9e1ae-115">Specifica l'oggetto tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-115">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e1ae-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9e1ae-116">-FriendlyName</span></span>
<span data-ttu-id="9e1ae-117">Specifica il nome descrittivo del provider di ripristino di Azure sito ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e1ae-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e1ae-118">-Name</span></span>
<span data-ttu-id="9e1ae-119">Specifica il nome del provider di ripristino di Azure sito ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9e1ae-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1ae-120">CommonParameters</span></span>
<span data-ttu-id="9e1ae-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1ae-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1ae-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e1ae-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1ae-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e1ae-123">INPUTS</span></span>

### <span data-ttu-id="9e1ae-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="9e1ae-124">ASRFabric</span></span>
<span data-ttu-id="9e1ae-125">Il parametro "tessuto" accetta il valore di tipo "ASRFabric" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="9e1ae-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="9e1ae-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e1ae-126">OUTPUTS</span></span>

### <span data-ttu-id="9e1ae-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9e1ae-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="9e1ae-128">Note</span><span class="sxs-lookup"><span data-stu-id="9e1ae-128">NOTES</span></span>

## <span data-ttu-id="9e1ae-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e1ae-129">RELATED LINKS</span></span>

[<span data-ttu-id="9e1ae-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9e1ae-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="9e1ae-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="9e1ae-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
