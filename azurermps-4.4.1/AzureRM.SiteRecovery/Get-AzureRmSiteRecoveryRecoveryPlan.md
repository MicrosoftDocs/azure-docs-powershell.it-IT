---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: 2d9f087b87d99003b559fc363265fdb4b996c3f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512900"
---
# <span data-ttu-id="6b972-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b972-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="6b972-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b972-102">SYNOPSIS</span></span>
<span data-ttu-id="6b972-103">Ottiene un piano di ripristino nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="6b972-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b972-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b972-104">SYNTAX</span></span>

### <span data-ttu-id="6b972-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b972-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b972-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6b972-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b972-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b972-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b972-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b972-108">DESCRIPTION</span></span>
<span data-ttu-id="6b972-109">Il cmdlet **Get-AzureRmSiteRecoveryRecoveryPlan** ottiene un piano di ripristino nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="6b972-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="6b972-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b972-110">EXAMPLES</span></span>

## <span data-ttu-id="6b972-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b972-111">PARAMETERS</span></span>

### <span data-ttu-id="6b972-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b972-112">-FriendlyName</span></span>
<span data-ttu-id="6b972-113">Specifica il nome descrittivo del piano di ripristino ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b972-113">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6b972-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6b972-114">-Name</span></span>
<span data-ttu-id="6b972-115">Specifica il nome del piano di ripristino ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b972-115">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6b972-116">-Path</span><span class="sxs-lookup"><span data-stu-id="6b972-116">-Path</span></span>
<span data-ttu-id="6b972-117">Specifica il percorso del file a cui questo cmdlet salva il piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6b972-117">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b972-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b972-118">-DefaultProfile</span></span>
<span data-ttu-id="6b972-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b972-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b972-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b972-120">CommonParameters</span></span>
<span data-ttu-id="6b972-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b972-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b972-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b972-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b972-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b972-123">INPUTS</span></span>

## <span data-ttu-id="6b972-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b972-124">OUTPUTS</span></span>

### <span data-ttu-id="6b972-125">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="6b972-125">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="6b972-126">Note</span><span class="sxs-lookup"><span data-stu-id="6b972-126">NOTES</span></span>

## <span data-ttu-id="6b972-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b972-127">RELATED LINKS</span></span>

[<span data-ttu-id="6b972-128">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b972-128">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6b972-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b972-129">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="6b972-130">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="6b972-130">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
