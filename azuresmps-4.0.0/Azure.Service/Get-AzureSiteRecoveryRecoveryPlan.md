---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8557B04E-DE35-473E-8F5D-B72B70300AA6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1949d30d6bbea16e1626954bf241df36d81533e1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023543"
---
# <span data-ttu-id="5f200-101">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5f200-101">Get-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="5f200-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f200-102">SYNOPSIS</span></span>
<span data-ttu-id="5f200-103">Ottiene un piano di ripristino nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="5f200-103">Gets a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="5f200-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f200-104">SYNTAX</span></span>

### <span data-ttu-id="5f200-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f200-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5f200-106">ById</span><span class="sxs-lookup"><span data-stu-id="5f200-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5f200-107">ByName</span><span class="sxs-lookup"><span data-stu-id="5f200-107">ByName</span></span>
```
Get-AzureSiteRecoveryRecoveryPlan -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5f200-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f200-108">DESCRIPTION</span></span>
<span data-ttu-id="5f200-109">Il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** ottiene un piano di ripristino nel ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="5f200-109">The **Get-AzureSiteRecoveryRecoveryPlan** cmdlet gets a recovery plan in Azure Site Recovery.</span></span>

## <span data-ttu-id="5f200-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f200-110">EXAMPLES</span></span>

### <span data-ttu-id="5f200-111">Esempio 1: ottenere un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="5f200-111">Example 1: Get a recovery plan</span></span>
```
PS C:\> Get-AzureSiteRecoveryRecoveryPlan
ID                            Name                          ServerId                      TargetServerId
--                            ----                          --------                      --------------
71de8ebc-1e9a-4242-aec3-ee... ContosoPlan                   4a94c4a9-c856-4577-afbd-36... 78facf56-b273-4941-82fd-cc...
```

<span data-ttu-id="5f200-112">Questo comando consente di ottenere informazioni sul piano di ripristino per l'attuale archivio di ripristino di Azure sito.</span><span class="sxs-lookup"><span data-stu-id="5f200-112">This command gets information about the recovery plan for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="5f200-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f200-113">PARAMETERS</span></span>

### <span data-ttu-id="5f200-114">-ID</span><span class="sxs-lookup"><span data-stu-id="5f200-114">-Id</span></span>
<span data-ttu-id="5f200-115">Specifica l'ID del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5f200-115">Specifies the ID of the recovery plan to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f200-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5f200-116">-Name</span></span>
<span data-ttu-id="5f200-117">Specifica il nome del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5f200-117">Specifies the name of the recovery plan to get.</span></span>

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

### <span data-ttu-id="5f200-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="5f200-118">-Profile</span></span>
<span data-ttu-id="5f200-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f200-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5f200-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="5f200-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f200-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f200-121">CommonParameters</span></span>
<span data-ttu-id="5f200-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f200-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f200-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f200-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f200-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f200-124">INPUTS</span></span>

## <span data-ttu-id="5f200-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f200-125">OUTPUTS</span></span>

## <span data-ttu-id="5f200-126">Note</span><span class="sxs-lookup"><span data-stu-id="5f200-126">NOTES</span></span>

## <span data-ttu-id="5f200-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f200-127">RELATED LINKS</span></span>

[<span data-ttu-id="5f200-128">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5f200-128">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5f200-129">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5f200-129">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="5f200-130">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5f200-130">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


