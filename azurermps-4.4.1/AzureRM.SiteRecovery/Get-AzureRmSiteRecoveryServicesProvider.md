---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e61136122873f7837120065194252aba145ea733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520750"
---
# <span data-ttu-id="a4870-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a4870-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="a4870-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a4870-102">SYNOPSIS</span></span>
<span data-ttu-id="a4870-103">Ottiene le informazioni sui provider di ripristino di Azure sito nel Vault.</span><span class="sxs-lookup"><span data-stu-id="a4870-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4870-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4870-104">SYNTAX</span></span>

### <span data-ttu-id="a4870-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a4870-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4870-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a4870-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4870-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a4870-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4870-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a4870-108">DESCRIPTION</span></span>
<span data-ttu-id="a4870-109">Il cmdlet **Get-AzureRmSiteRecoveryServicesProvider** ottiene le informazioni sui provider di ripristino del sito di Azure nel Vault.</span><span class="sxs-lookup"><span data-stu-id="a4870-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="a4870-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4870-110">EXAMPLES</span></span>

## <span data-ttu-id="a4870-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a4870-111">PARAMETERS</span></span>

### <span data-ttu-id="a4870-112">-Tessuto</span><span class="sxs-lookup"><span data-stu-id="a4870-112">-Fabric</span></span>
<span data-ttu-id="a4870-113">Specifica l'oggetto tessuto di recupero sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4870-113">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4870-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a4870-114">-FriendlyName</span></span>
<span data-ttu-id="a4870-115">Specifica il nome descrittivo del provider di ripristino di Azure sito ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4870-115">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4870-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="a4870-116">-Name</span></span>
<span data-ttu-id="a4870-117">Specifica il nome del provider di ripristino di Azure sito ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4870-117">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4870-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4870-118">-DefaultProfile</span></span>
<span data-ttu-id="a4870-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a4870-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4870-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4870-120">CommonParameters</span></span>
<span data-ttu-id="a4870-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4870-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4870-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4870-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4870-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a4870-123">INPUTS</span></span>

### <span data-ttu-id="a4870-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a4870-124">ASRFabric</span></span>
<span data-ttu-id="a4870-125">Il parametro "tessuto" accetta il valore di tipo "ASRFabric" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="a4870-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="a4870-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4870-126">OUTPUTS</span></span>

### <span data-ttu-id="a4870-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryServicesProvider, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a4870-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a4870-128">Note</span><span class="sxs-lookup"><span data-stu-id="a4870-128">NOTES</span></span>

## <span data-ttu-id="a4870-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4870-129">RELATED LINKS</span></span>

[<span data-ttu-id="a4870-130">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a4870-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="a4870-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a4870-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
