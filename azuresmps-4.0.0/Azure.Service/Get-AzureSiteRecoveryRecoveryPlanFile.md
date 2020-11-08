---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023541"
---
# <span data-ttu-id="c8d56-101">Get-AzureSiteRecoveryRecoveryPlanFile</span><span class="sxs-lookup"><span data-stu-id="c8d56-101">Get-AzureSiteRecoveryRecoveryPlanFile</span></span>

## <span data-ttu-id="c8d56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8d56-102">SYNOPSIS</span></span>
<span data-ttu-id="c8d56-103">Scarica un piano di ripristino di un sito Azure in formato XML.</span><span class="sxs-lookup"><span data-stu-id="c8d56-103">Downloads an Azure Site Recovery plan in XML format.</span></span>

## <span data-ttu-id="c8d56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8d56-104">SYNTAX</span></span>

### <span data-ttu-id="c8d56-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8d56-105">ByRPObject (Default)</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c8d56-106">ById</span><span class="sxs-lookup"><span data-stu-id="c8d56-106">ById</span></span>
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8d56-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8d56-107">DESCRIPTION</span></span>
<span data-ttu-id="c8d56-108">Il cmdlet **Get-AzureSiteRecoveryRecoveryPlanFile** Scarica un piano di ripristino del sito di Azure in formato XML.</span><span class="sxs-lookup"><span data-stu-id="c8d56-108">The **Get-AzureSiteRecoveryRecoveryPlanFile** cmdlet downloads an Azure Site Recovery plan in XML format.</span></span>
<span data-ttu-id="c8d56-109">È possibile usare questo file per aggiornare il piano di ripristino e quindi caricarlo nel server di ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="c8d56-109">You can use this file to update the recovery plan and then upload it to the Site Recovery server.</span></span>

<span data-ttu-id="c8d56-110">Un piano di ripristino raccoglie le macchine virtuali in un gruppo per scopi di failover e ripristino.</span><span class="sxs-lookup"><span data-stu-id="c8d56-110">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="c8d56-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8d56-111">EXAMPLES</span></span>

### <span data-ttu-id="c8d56-112">Esempio 1: ottenere un file piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="c8d56-112">Example 1: Get a recovery plan file</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="c8d56-113">Questo comando usa il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** per ottenere il piano di ripristino e lo archivia nella variabile $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="c8d56-113">This command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="c8d56-114">Il secondo comando usa il cmdlet **GetAzureSiteRecoveryRecoveryPlanFile** per ottenere il file XML del piano di ripristino del sito in $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="c8d56-114">The second command uses the **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet to get the site recovery plan XML file in $RecoveryPlan.</span></span>
<span data-ttu-id="c8d56-115">Il comando Archivia il file XML nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="c8d56-115">The command stores the XML file at the specified path.</span></span>

## <span data-ttu-id="c8d56-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8d56-116">PARAMETERS</span></span>

### <span data-ttu-id="c8d56-117">-ID</span><span class="sxs-lookup"><span data-stu-id="c8d56-117">-Id</span></span>
<span data-ttu-id="c8d56-118">Specifica l'ID del piano di ripristino da ottenere.</span><span class="sxs-lookup"><span data-stu-id="c8d56-118">Specifies the ID of the recovery plan to get.</span></span>

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

### <span data-ttu-id="c8d56-119">-Path</span><span class="sxs-lookup"><span data-stu-id="c8d56-119">-Path</span></span>
<span data-ttu-id="c8d56-120">Specifica il percorso completo in cui archiviare il file XML del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c8d56-120">Specifies the full path to store the recovery plan XML file.</span></span>

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

### <span data-ttu-id="c8d56-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="c8d56-121">-Profile</span></span>
<span data-ttu-id="c8d56-122">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8d56-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c8d56-123">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="c8d56-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c8d56-124">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8d56-124">-RecoveryPlan</span></span>
<span data-ttu-id="c8d56-125">Specifica un oggetto **ASRRecoveryPlan** da cui ottenere il piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="c8d56-125">Specifies an **ASRRecoveryPlan** object from which to get the recovery plan.</span></span>
<span data-ttu-id="c8d56-126">Per ottenere un oggetto **ASRRecoveryPlan** , usa il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="c8d56-126">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8d56-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8d56-127">CommonParameters</span></span>
<span data-ttu-id="c8d56-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8d56-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8d56-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8d56-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8d56-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8d56-130">INPUTS</span></span>

## <span data-ttu-id="c8d56-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8d56-131">OUTPUTS</span></span>

## <span data-ttu-id="c8d56-132">Note</span><span class="sxs-lookup"><span data-stu-id="c8d56-132">NOTES</span></span>

## <span data-ttu-id="c8d56-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8d56-133">RELATED LINKS</span></span>

[<span data-ttu-id="c8d56-134">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c8d56-134">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)


