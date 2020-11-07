---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2020
ms.locfileid: "93858826"
---
# <span data-ttu-id="42a7c-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="42a7c-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="42a7c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="42a7c-103">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="42a7c-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="42a7c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42a7c-104">SYNTAX</span></span>

### <span data-ttu-id="42a7c-105">Applica (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42a7c-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42a7c-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a7c-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42a7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42a7c-107">DESCRIPTION</span></span>
<span data-ttu-id="42a7c-108">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="42a7c-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="42a7c-109">Dopo aver richiamato, Get-AzsUpdateRun può essere usato per modificare lo stato dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="42a7c-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="42a7c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42a7c-110">EXAMPLES</span></span>

### <span data-ttu-id="42a7c-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="42a7c-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="42a7c-112">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="42a7c-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="42a7c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42a7c-113">PARAMETERS</span></span>

### <span data-ttu-id="42a7c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="42a7c-114">-Name</span></span>
<span data-ttu-id="42a7c-115">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="42a7c-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a7c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42a7c-116">-ResourceGroupName</span></span>
<span data-ttu-id="42a7c-117">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="42a7c-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a7c-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="42a7c-118">-Location</span></span>
<span data-ttu-id="42a7c-119">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="42a7c-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42a7c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42a7c-120">-AsJob</span></span>
<span data-ttu-id="42a7c-121">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="42a7c-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="42a7c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42a7c-122">-ResourceId</span></span>
<span data-ttu-id="42a7c-123">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="42a7c-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42a7c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="42a7c-124">-Force</span></span>
<span data-ttu-id="42a7c-125">Contrassegna per rimuovere l'elemento senza conferma.</span><span class="sxs-lookup"><span data-stu-id="42a7c-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="42a7c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42a7c-126">-WhatIf</span></span>
<span data-ttu-id="42a7c-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42a7c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42a7c-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="42a7c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42a7c-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="42a7c-129">-Confirm</span></span>
<span data-ttu-id="42a7c-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42a7c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42a7c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42a7c-131">CommonParameters</span></span>
<span data-ttu-id="42a7c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42a7c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42a7c-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42a7c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42a7c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42a7c-134">INPUTS</span></span>

## <span data-ttu-id="42a7c-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42a7c-135">OUTPUTS</span></span>

### <span data-ttu-id="42a7c-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="42a7c-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="42a7c-137">Note</span><span class="sxs-lookup"><span data-stu-id="42a7c-137">NOTES</span></span>

## <span data-ttu-id="42a7c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42a7c-138">RELATED LINKS</span></span>
