---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029573"
---
# <span data-ttu-id="ea285-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ea285-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="ea285-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ea285-102">SYNOPSIS</span></span>
<span data-ttu-id="ea285-103">Rimuove un piano di ripristino del sito dal ripristino del sito.</span><span class="sxs-lookup"><span data-stu-id="ea285-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="ea285-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea285-104">SYNTAX</span></span>

### <span data-ttu-id="ea285-105">ByRPObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea285-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea285-106">ById</span><span class="sxs-lookup"><span data-stu-id="ea285-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea285-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea285-107">DESCRIPTION</span></span>
<span data-ttu-id="ea285-108">Il cmdlet **Remove-AzureSiteRecoveryRecoveryPlan** rimuove un piano di ripristino del sito dal ripristino del sito di Azure corrente.</span><span class="sxs-lookup"><span data-stu-id="ea285-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="ea285-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea285-109">EXAMPLES</span></span>

### <span data-ttu-id="ea285-110">Esempio 1: rimuovere un piano di ripristino</span><span class="sxs-lookup"><span data-stu-id="ea285-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="ea285-111">Il primo comando usa il cmdlet **Get-AzureSiteRecoveryRecoveryPlan** per ottenere il piano di ripristino del sito e lo archivia nella variabile $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="ea285-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="ea285-112">Il secondo comando rimuove il piano di ripristino in $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="ea285-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="ea285-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ea285-113">PARAMETERS</span></span>

### <span data-ttu-id="ea285-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ea285-114">-Force</span></span>
<span data-ttu-id="ea285-115">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ea285-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea285-116">-ID</span><span class="sxs-lookup"><span data-stu-id="ea285-116">-Id</span></span>
<span data-ttu-id="ea285-117">Specifica l'ID del piano di ripristino da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ea285-117">Specifies the ID of the recovery plan to remove.</span></span>

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

### <span data-ttu-id="ea285-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="ea285-118">-Profile</span></span>
<span data-ttu-id="ea285-119">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea285-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ea285-120">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="ea285-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ea285-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ea285-121">-RecoveryPlan</span></span>
<span data-ttu-id="ea285-122">Specifica il piano di ripristino da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ea285-122">Specifies the recovery plan to remove.</span></span>

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

### <span data-ttu-id="ea285-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ea285-123">-WaitForCompletion</span></span>
<span data-ttu-id="ea285-124">Indica che il cmdlet attende il completamento dell'operazione prima di restituire il controllo alla console di Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ea285-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="ea285-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ea285-125">-Confirm</span></span>
<span data-ttu-id="ea285-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea285-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea285-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea285-127">-WhatIf</span></span>
<span data-ttu-id="ea285-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea285-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea285-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea285-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea285-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea285-130">CommonParameters</span></span>
<span data-ttu-id="ea285-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea285-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea285-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea285-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea285-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ea285-133">INPUTS</span></span>

## <span data-ttu-id="ea285-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea285-134">OUTPUTS</span></span>

## <span data-ttu-id="ea285-135">Note</span><span class="sxs-lookup"><span data-stu-id="ea285-135">NOTES</span></span>

## <span data-ttu-id="ea285-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea285-136">RELATED LINKS</span></span>

[<span data-ttu-id="ea285-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ea285-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ea285-138">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ea285-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="ea285-139">Update-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="ea285-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


