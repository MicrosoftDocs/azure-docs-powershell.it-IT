---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030526"
---
# <span data-ttu-id="5e08f-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="5e08f-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="5e08f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e08f-102">SYNOPSIS</span></span>
<span data-ttu-id="5e08f-103">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5e08f-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="5e08f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e08f-104">SYNTAX</span></span>

### <span data-ttu-id="5e08f-105">UpdateRuns_Rerun (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5e08f-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e08f-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e08f-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e08f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e08f-107">DESCRIPTION</span></span>
<span data-ttu-id="5e08f-108">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5e08f-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="5e08f-109">Le esecuzioni di aggiornamento riprese verranno riattivate nel punto in cui sono state eseguite l'ultima operazione</span><span class="sxs-lookup"><span data-stu-id="5e08f-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="5e08f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e08f-110">EXAMPLES</span></span>

### <span data-ttu-id="5e08f-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="5e08f-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="5e08f-112">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="5e08f-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="5e08f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e08f-113">PARAMETERS</span></span>

### <span data-ttu-id="5e08f-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e08f-114">-Name</span></span>
<span data-ttu-id="5e08f-115">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5e08f-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-116">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5e08f-116">-Location</span></span>
<span data-ttu-id="5e08f-117">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5e08f-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e08f-118">-ResourceGroupName</span></span>
<span data-ttu-id="5e08f-119">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e08f-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="5e08f-120">-UpdateName</span></span>
<span data-ttu-id="5e08f-121">Nome visualizzato dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="5e08f-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e08f-122">-AsJob</span></span>
<span data-ttu-id="5e08f-123">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="5e08f-123">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e08f-124">-ResourceId</span></span>
<span data-ttu-id="5e08f-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5e08f-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="5e08f-126">-Force</span></span>
<span data-ttu-id="5e08f-127">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="5e08f-127">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e08f-128">-WhatIf</span></span>
<span data-ttu-id="5e08f-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e08f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e08f-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e08f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e08f-131">-Confirm</span></span>
<span data-ttu-id="5e08f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e08f-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e08f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e08f-133">CommonParameters</span></span>
<span data-ttu-id="5e08f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e08f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e08f-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e08f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e08f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e08f-136">INPUTS</span></span>

## <span data-ttu-id="5e08f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e08f-137">OUTPUTS</span></span>

## <span data-ttu-id="5e08f-138">Note</span><span class="sxs-lookup"><span data-stu-id="5e08f-138">NOTES</span></span>

## <span data-ttu-id="5e08f-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e08f-139">RELATED LINKS</span></span>
