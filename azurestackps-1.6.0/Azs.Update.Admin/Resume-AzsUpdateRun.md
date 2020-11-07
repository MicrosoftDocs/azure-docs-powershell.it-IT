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
ms.locfileid: "93685230"
---
# <span data-ttu-id="71277-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="71277-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="71277-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71277-102">SYNOPSIS</span></span>
<span data-ttu-id="71277-103">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="71277-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="71277-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71277-104">SYNTAX</span></span>

### <span data-ttu-id="71277-105">UpdateRuns_Rerun (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71277-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71277-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="71277-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71277-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71277-107">DESCRIPTION</span></span>
<span data-ttu-id="71277-108">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="71277-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="71277-109">Le esecuzioni di aggiornamento riprese verranno riattivate nel punto in cui sono state eseguite l'ultima operazione</span><span class="sxs-lookup"><span data-stu-id="71277-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="71277-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71277-110">EXAMPLES</span></span>

### <span data-ttu-id="71277-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="71277-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="71277-112">Riprende una fase di aggiornamento avviata in precedenza che non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="71277-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="71277-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71277-113">PARAMETERS</span></span>

### <span data-ttu-id="71277-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="71277-114">-AsJob</span></span>
<span data-ttu-id="71277-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="71277-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="71277-116">-Force</span><span class="sxs-lookup"><span data-stu-id="71277-116">-Force</span></span>
<span data-ttu-id="71277-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="71277-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="71277-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="71277-118">-Location</span></span>
<span data-ttu-id="71277-119">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="71277-119">The name of the update location.</span></span>

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

### <span data-ttu-id="71277-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="71277-120">-Name</span></span>
<span data-ttu-id="71277-121">Identificatore esecuzione aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="71277-121">Update run identifier.</span></span>

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

### <span data-ttu-id="71277-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71277-122">-ResourceGroupName</span></span>
<span data-ttu-id="71277-123">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="71277-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="71277-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71277-124">-ResourceId</span></span>
<span data-ttu-id="71277-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="71277-125">The resource id.</span></span>

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

### <span data-ttu-id="71277-126">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="71277-126">-UpdateName</span></span>
<span data-ttu-id="71277-127">Nome visualizzato dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="71277-127">Display name of the update.</span></span>

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

### <span data-ttu-id="71277-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71277-128">-Confirm</span></span>
<span data-ttu-id="71277-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71277-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71277-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71277-130">-WhatIf</span></span>
<span data-ttu-id="71277-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71277-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71277-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71277-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71277-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71277-133">CommonParameters</span></span>
<span data-ttu-id="71277-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71277-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71277-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71277-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71277-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71277-136">INPUTS</span></span>

## <span data-ttu-id="71277-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71277-137">OUTPUTS</span></span>

## <span data-ttu-id="71277-138">Note</span><span class="sxs-lookup"><span data-stu-id="71277-138">NOTES</span></span>

## <span data-ttu-id="71277-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71277-139">RELATED LINKS</span></span>

