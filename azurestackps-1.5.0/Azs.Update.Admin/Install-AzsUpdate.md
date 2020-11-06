---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491545"
---
# <span data-ttu-id="1f134-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="1f134-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="1f134-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f134-102">SYNOPSIS</span></span>
<span data-ttu-id="1f134-103">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1f134-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="1f134-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f134-104">SYNTAX</span></span>

### <span data-ttu-id="1f134-105">Applica (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f134-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f134-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f134-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f134-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f134-107">DESCRIPTION</span></span>
<span data-ttu-id="1f134-108">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1f134-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="1f134-109">Dopo aver richiamato, Get-AzsUpdateRun può essere usato per modificare lo stato dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1f134-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="1f134-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f134-110">EXAMPLES</span></span>

### <span data-ttu-id="1f134-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1f134-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="1f134-112">Applicare un aggiornamento specifico in una posizione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1f134-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="1f134-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f134-113">PARAMETERS</span></span>

### <span data-ttu-id="1f134-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f134-114">-AsJob</span></span>
<span data-ttu-id="1f134-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="1f134-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1f134-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1f134-116">-Force</span></span>
<span data-ttu-id="1f134-117">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="1f134-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1f134-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1f134-118">-Location</span></span>
<span data-ttu-id="1f134-119">Il nome del percorso di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1f134-119">The name of the update location.</span></span>

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

### <span data-ttu-id="1f134-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f134-120">-Name</span></span>
<span data-ttu-id="1f134-121">Nome dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="1f134-121">Name of the update.</span></span>

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

### <span data-ttu-id="1f134-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f134-122">-ResourceGroupName</span></span>
<span data-ttu-id="1f134-123">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f134-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="1f134-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f134-124">-ResourceId</span></span>
<span data-ttu-id="1f134-125">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f134-125">The resource id.</span></span>

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

### <span data-ttu-id="1f134-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f134-126">-Confirm</span></span>
<span data-ttu-id="1f134-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f134-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f134-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f134-128">-WhatIf</span></span>
<span data-ttu-id="1f134-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f134-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f134-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f134-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f134-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f134-131">CommonParameters</span></span>
<span data-ttu-id="1f134-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f134-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f134-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f134-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f134-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f134-134">INPUTS</span></span>

## <span data-ttu-id="1f134-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f134-135">OUTPUTS</span></span>

### <span data-ttu-id="1f134-136">Microsoft. AzureStack. Management. Update. admin. Models. Update</span><span class="sxs-lookup"><span data-stu-id="1f134-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="1f134-137">Note</span><span class="sxs-lookup"><span data-stu-id="1f134-137">NOTES</span></span>

## <span data-ttu-id="1f134-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f134-138">RELATED LINKS</span></span>
