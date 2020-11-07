---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: a10f7ffb1b05474e5d2b86fa7d7a55f825aaad25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688255"
---
# <span data-ttu-id="29695-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="29695-101">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="29695-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29695-102">SYNOPSIS</span></span>
<span data-ttu-id="29695-103">Ottiene un piano di ripristino o tutti i piani di ripristino nel Vault di servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="29695-103">Gets a recovery plan or all the recovery plans in the Recovery Services vault</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29695-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29695-104">SYNTAX</span></span>

### <span data-ttu-id="29695-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29695-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan [<CommonParameters>]
```

### <span data-ttu-id="29695-106">ByName</span><span class="sxs-lookup"><span data-stu-id="29695-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [[-Path] <String>] [<CommonParameters>]
```

### <span data-ttu-id="29695-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="29695-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrRecoveryPlan -FriendlyName <String> [[-Path] <String>] [<CommonParameters>]
```

## <span data-ttu-id="29695-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29695-108">DESCRIPTION</span></span>
<span data-ttu-id="29695-109">Il cmdlet **Get-AzureRmRecoveryServicesAsrRecoveryPlan** consente di ottenere i dettagli del piano di ripristino specificato o di tutti i piani di ripristino nel Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="29695-109">The **Get-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet gets the details of the specified recovery plan or all recovery plans in the Recovery Services vault.</span></span>

## <span data-ttu-id="29695-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29695-110">EXAMPLES</span></span>

### <span data-ttu-id="29695-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="29695-111">Example 1</span></span>
```
PS C:\> $RP = Get-AzureRmRecoveryServicesAsrRecoveryPlan -Name $RPName
```

<span data-ttu-id="29695-112">Ottiene il piano di ripristino con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="29695-112">Gets the recovery plan with the specified name.</span></span>

## <span data-ttu-id="29695-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29695-113">PARAMETERS</span></span>

### <span data-ttu-id="29695-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="29695-114">-FriendlyName</span></span>
<span data-ttu-id="29695-115">Specifica il nome descrittivo del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="29695-115">Specifies the friendly name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="29695-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="29695-116">-Name</span></span>
<span data-ttu-id="29695-117">Specifica il nome del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="29695-117">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="29695-118">-Path</span><span class="sxs-lookup"><span data-stu-id="29695-118">-Path</span></span>
<span data-ttu-id="29695-119">Specifica il percorso del file a cui questo cmdlet salva la definizione JSON del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="29695-119">Specifies the file path to which this cmdlet saves the recovery plan json definition.</span></span> <span data-ttu-id="29695-120">La definizione JSON può essere modificata per modificare il piano di ripristino e usato per aggiornare il piano di ripristino tramite il cmdlet Update-AzureRmRecoveryServicesASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="29695-120">The json definition can be edited to modify the recovery plan and used to update the recovery plan through the Update-AzureRmRecoveryServicesASRRecoveryPlan cmdlet</span></span>

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

### <span data-ttu-id="29695-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29695-121">CommonParameters</span></span>
<span data-ttu-id="29695-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29695-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29695-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29695-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29695-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29695-124">INPUTS</span></span>

### <span data-ttu-id="29695-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="29695-125">None</span></span>

## <span data-ttu-id="29695-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29695-126">OUTPUTS</span></span>

### <span data-ttu-id="29695-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="29695-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="29695-128">Note</span><span class="sxs-lookup"><span data-stu-id="29695-128">NOTES</span></span>

## <span data-ttu-id="29695-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29695-129">RELATED LINKS</span></span>

[<span data-ttu-id="29695-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="29695-130">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="29695-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="29695-131">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="29695-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="29695-132">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)
