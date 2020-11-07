---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685164"
---
# <span data-ttu-id="50a5d-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="50a5d-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="50a5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50a5d-102">SYNOPSIS</span></span>
<span data-ttu-id="50a5d-103">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="50a5d-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="50a5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50a5d-104">SYNTAX</span></span>

### <span data-ttu-id="50a5d-105">UpdateRuns_Rerun (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50a5d-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50a5d-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="50a5d-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50a5d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50a5d-107">DESCRIPTION</span></span>
<span data-ttu-id="50a5d-108">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="50a5d-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="50a5d-109">Le esecuzioni di aggiornamento riprese verranno riattivate nel punto in cui sono state eseguite l'ultima operazione</span><span class="sxs-lookup"><span data-stu-id="50a5d-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="50a5d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50a5d-110">EXAMPLES</span></span>

### <span data-ttu-id="50a5d-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="50a5d-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="50a5d-112">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="50a5d-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="50a5d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50a5d-113">PARAMETERS</span></span>

### <span data-ttu-id="50a5d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50a5d-114">-AsJob</span></span>
<span data-ttu-id="50a5d-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="50a5d-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="50a5d-116">-Force</span><span class="sxs-lookup"><span data-stu-id="50a5d-116">-Force</span></span>
<span data-ttu-id="50a5d-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="50a5d-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="50a5d-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="50a5d-118">-Location</span></span>
<span data-ttu-id="50a5d-119">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="50a5d-119">The name of the update location.</span></span>

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

### <span data-ttu-id="50a5d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="50a5d-120">-Name</span></span>
<span data-ttu-id="50a5d-121">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="50a5d-121">Update run identifier.</span></span>

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

### <span data-ttu-id="50a5d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50a5d-122">-ResourceGroupName</span></span>
<span data-ttu-id="50a5d-123">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="50a5d-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="50a5d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50a5d-124">-ResourceId</span></span>
<span data-ttu-id="50a5d-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="50a5d-125">The resource id.</span></span>

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

### <span data-ttu-id="50a5d-126">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="50a5d-126">-UpdateName</span></span>
<span data-ttu-id="50a5d-127">Nome visualizzato dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="50a5d-127">Display name of the update.</span></span>

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

### <span data-ttu-id="50a5d-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50a5d-128">-Confirm</span></span>
<span data-ttu-id="50a5d-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50a5d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a5d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a5d-130">-WhatIf</span></span>
<span data-ttu-id="50a5d-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50a5d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a5d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50a5d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a5d-133">CommonParameters</span></span>
<span data-ttu-id="50a5d-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50a5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a5d-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50a5d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a5d-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50a5d-136">INPUTS</span></span>

## <span data-ttu-id="50a5d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50a5d-137">OUTPUTS</span></span>

## <span data-ttu-id="50a5d-138">Note</span><span class="sxs-lookup"><span data-stu-id="50a5d-138">NOTES</span></span>

## <span data-ttu-id="50a5d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50a5d-139">RELATED LINKS</span></span>

