---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2F749E4A-149F-44E0-8AEB-F2C416140906
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7d1162ed2c9126942cc6ae31cbe31fdc2ef130d8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023934"
---
# <span data-ttu-id="a8ee4-101">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8ee4-101">New-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="a8ee4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ee4-103">Crea un piano di ripristino del sito nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-103">Creates a site recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="a8ee4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8ee4-104">SYNTAX</span></span>

```
New-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8ee4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ee4-106">Il cmdlet **New-AzureSiteRecoveryRecoveryPlan** crea un piano di ripristino in Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-106">The **New-AzureSiteRecoveryRecoveryPlan** cmdlet creates a recovery plan in Azure Site Recovery.</span></span>

<span data-ttu-id="a8ee4-107">Un piano di ripristino raccoglie le macchine virtuali in un gruppo per scopi di failover e ripristino.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-107">A recovery plan gathers virtual machines in a group for the purposes of failover and recovery.</span></span>

## <span data-ttu-id="a8ee4-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8ee4-108">EXAMPLES</span></span>

### <span data-ttu-id="a8ee4-109">Esempio 1: aggiungere un piano di ripristino a un Vault di ripristino del sito</span><span class="sxs-lookup"><span data-stu-id="a8ee4-109">Example 1: Add a recovery plan to a Site Recovery vault</span></span>
```
PS C:\> New-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="a8ee4-110">Questo comando aggiunge il piano di ripristino denominato RecoveryPlan.xml all'archivio di ripristino del sito di Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-110">This command adds the recovery plan named RecoveryPlan.xml to the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="a8ee4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8ee4-111">PARAMETERS</span></span>

### <span data-ttu-id="a8ee4-112">-File</span><span class="sxs-lookup"><span data-stu-id="a8ee4-112">-File</span></span>
<span data-ttu-id="a8ee4-113">Specifica il percorso del file del piano di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-113">Specifies the path of the recovery plan file.</span></span>

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

### <span data-ttu-id="a8ee4-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="a8ee4-114">-Profile</span></span>
<span data-ttu-id="a8ee4-115">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a8ee4-116">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a8ee4-117">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a8ee4-117">-WaitForCompletion</span></span>
<span data-ttu-id="a8ee4-118">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-118">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ee4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ee4-119">CommonParameters</span></span>
<span data-ttu-id="a8ee4-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ee4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ee4-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ee4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ee4-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8ee4-122">INPUTS</span></span>

## <span data-ttu-id="a8ee4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8ee4-123">OUTPUTS</span></span>

## <span data-ttu-id="a8ee4-124">Note</span><span class="sxs-lookup"><span data-stu-id="a8ee4-124">NOTES</span></span>

## <span data-ttu-id="a8ee4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8ee4-125">RELATED LINKS</span></span>

[<span data-ttu-id="a8ee4-126">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8ee4-126">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a8ee4-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8ee4-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a8ee4-128">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a8ee4-128">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


