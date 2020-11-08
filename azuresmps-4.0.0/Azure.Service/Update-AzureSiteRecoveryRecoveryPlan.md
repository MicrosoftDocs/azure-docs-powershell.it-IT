---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 5625ED47-BD85-4BF5-9044-2012E5A67BA4
online version: ''
schema: 2.0.0
ms.openlocfilehash: d1c680adf1d9d850f89cb81e1525a0e0e06eb6c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029476"
---
# <span data-ttu-id="a539f-101">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a539f-101">Update-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="a539f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a539f-102">SYNOPSIS</span></span>
<span data-ttu-id="a539f-103">Aggiorna un piano di ripristino nel ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="a539f-103">Updates a recovery plan in Site Recovery.</span></span>

## <span data-ttu-id="a539f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a539f-104">SYNTAX</span></span>

```
Update-AzureSiteRecoveryRecoveryPlan -File <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="a539f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a539f-105">DESCRIPTION</span></span>
<span data-ttu-id="a539f-106">Il cmdlet **Update-AzureSiteRecoveryRecoveryPlan** aggiorna un piano di ripristino in Azure Site Recovery e lo pubblica.</span><span class="sxs-lookup"><span data-stu-id="a539f-106">The **Update-AzureSiteRecoveryRecoveryPlan** cmdlet updates a recovery plan in Azure Site Recovery and then publishes it.</span></span>

## <span data-ttu-id="a539f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a539f-107">EXAMPLES</span></span>

### <span data-ttu-id="a539f-108">Esempio 1: aggiornare un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="a539f-108">Example 1: Update a recovery plan</span></span>
```
PS C:\> Update-AzureSiteRecoveryRecoveryPlan -File "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

<span data-ttu-id="a539f-109">Questo comando Aggiorna il piano di ripristino specificato e lo pubblica.</span><span class="sxs-lookup"><span data-stu-id="a539f-109">This command updates the specified recovery plan, and then publishes it.</span></span>

## <span data-ttu-id="a539f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a539f-110">PARAMETERS</span></span>

### <span data-ttu-id="a539f-111">-File</span><span class="sxs-lookup"><span data-stu-id="a539f-111">-File</span></span>
<span data-ttu-id="a539f-112">Specifica il file del piano di ripristino del piano di ripristino che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="a539f-112">Specifies the recovery plan file of the recovery plan that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a539f-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="a539f-113">-Profile</span></span>
<span data-ttu-id="a539f-114">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a539f-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a539f-115">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="a539f-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a539f-116">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a539f-116">-WaitForCompletion</span></span>
<span data-ttu-id="a539f-117">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a539f-117">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="a539f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a539f-118">CommonParameters</span></span>
<span data-ttu-id="a539f-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a539f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a539f-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a539f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a539f-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a539f-121">INPUTS</span></span>

## <span data-ttu-id="a539f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a539f-122">OUTPUTS</span></span>

## <span data-ttu-id="a539f-123">Note</span><span class="sxs-lookup"><span data-stu-id="a539f-123">NOTES</span></span>

## <span data-ttu-id="a539f-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a539f-124">RELATED LINKS</span></span>

[<span data-ttu-id="a539f-125">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a539f-125">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a539f-126">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a539f-126">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="a539f-127">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="a539f-127">Remove-AzureSiteRecoveryRecoveryPlan</span></span>](./Remove-AzureSiteRecoveryRecoveryPlan.md)


