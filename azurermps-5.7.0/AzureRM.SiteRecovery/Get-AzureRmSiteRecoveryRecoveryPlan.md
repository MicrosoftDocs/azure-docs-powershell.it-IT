---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3B879056-5BF3-4262-8BAA-E79589149370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryRecoveryPlan.md
ms.openlocfilehash: ae5a1d5a70064b3849bc8f38cab46ecfabaf4968
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687443"
---
# <span data-ttu-id="69825-101">Get-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69825-101">Get-AzureRmSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="69825-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69825-102">SYNOPSIS</span></span>
<span data-ttu-id="69825-103">Ottiene un piano di ripristino nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="69825-103">Gets a recovery plan in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69825-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69825-104">SYNTAX</span></span>

### <span data-ttu-id="69825-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="69825-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69825-106">ByName</span><span class="sxs-lookup"><span data-stu-id="69825-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -Name <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="69825-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="69825-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryRecoveryPlan -FriendlyName <String> [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69825-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69825-108">DESCRIPTION</span></span>
<span data-ttu-id="69825-109">Il cmdlet **Get-AzureRmSiteRecoveryRecoveryPlan** ottiene un piano di ripristino nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="69825-109">The **Get-AzureRmSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="69825-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69825-110">EXAMPLES</span></span>

## <span data-ttu-id="69825-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69825-111">PARAMETERS</span></span>

### <span data-ttu-id="69825-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69825-112">-DefaultProfile</span></span>
<span data-ttu-id="69825-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69825-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69825-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="69825-114">-FriendlyName</span></span>
<span data-ttu-id="69825-115">Specifica il nome descrittivo del piano di ripristino ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69825-115">Specifies the friendly name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69825-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="69825-116">-Name</span></span>
<span data-ttu-id="69825-117">Specifica il nome del piano di ripristino ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69825-117">Specifies the name of the recovery plan that this cmdlet gets.</span></span>

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

### <span data-ttu-id="69825-118">-Path</span><span class="sxs-lookup"><span data-stu-id="69825-118">-Path</span></span>
<span data-ttu-id="69825-119">Specifica il percorso del file a cui questo cmdlet salva il piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="69825-119">Specifies the file path to which this cmdlet saves the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByName, ByFriendlyName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69825-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69825-120">CommonParameters</span></span>
<span data-ttu-id="69825-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69825-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69825-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69825-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69825-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69825-123">INPUTS</span></span>

### <span data-ttu-id="69825-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="69825-124">None</span></span>
<span data-ttu-id="69825-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="69825-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69825-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69825-126">OUTPUTS</span></span>

### <span data-ttu-id="69825-127">System. Collections. Generic. IEnumerable ' 1 [Microsoft. Azure. Commands. SiteRecovery. ASRRecoveryPlan]</span><span class="sxs-lookup"><span data-stu-id="69825-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan]</span></span>

## <span data-ttu-id="69825-128">Note</span><span class="sxs-lookup"><span data-stu-id="69825-128">NOTES</span></span>

## <span data-ttu-id="69825-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69825-129">RELATED LINKS</span></span>

[<span data-ttu-id="69825-130">New-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69825-130">New-AzureRmSiteRecoveryRecoveryPlan</span></span>](./New-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="69825-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69825-131">Remove-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureRmSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="69825-132">Update-AzureRmSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="69825-132">Update-AzureRmSiteRecoveryRecoveryPlan</span></span>](./Update-AzureRmSiteRecoveryRecoveryPlan.md)
