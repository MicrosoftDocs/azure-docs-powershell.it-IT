---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93854086"
---
# <span data-ttu-id="16894-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="16894-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="16894-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16894-102">SYNOPSIS</span></span>
<span data-ttu-id="16894-103">Annullare un processo di migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="16894-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="16894-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16894-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16894-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16894-105">DESCRIPTION</span></span>
<span data-ttu-id="16894-106">Annullare un processo di migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="16894-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="16894-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16894-107">EXAMPLES</span></span>

### <span data-ttu-id="16894-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="16894-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="16894-109">Annullare la migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="16894-109">Cancel container migration.</span></span>

## <span data-ttu-id="16894-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16894-110">PARAMETERS</span></span>

### <span data-ttu-id="16894-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16894-111">-AsJob</span></span>
<span data-ttu-id="16894-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="16894-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="16894-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="16894-113">-FarmName</span></span>
<span data-ttu-id="16894-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="16894-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16894-115">-Force</span><span class="sxs-lookup"><span data-stu-id="16894-115">-Force</span></span>
<span data-ttu-id="16894-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="16894-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="16894-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="16894-117">-JobId</span></span>
<span data-ttu-id="16894-118">ID operazione.</span><span class="sxs-lookup"><span data-stu-id="16894-118">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16894-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16894-119">-ResourceGroupName</span></span>
<span data-ttu-id="16894-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="16894-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16894-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16894-121">-Confirm</span></span>
<span data-ttu-id="16894-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16894-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16894-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16894-123">-WhatIf</span></span>
<span data-ttu-id="16894-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16894-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16894-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16894-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16894-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16894-126">CommonParameters</span></span>
<span data-ttu-id="16894-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16894-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16894-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16894-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16894-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16894-129">INPUTS</span></span>

## <span data-ttu-id="16894-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16894-130">OUTPUTS</span></span>

## <span data-ttu-id="16894-131">Note</span><span class="sxs-lookup"><span data-stu-id="16894-131">NOTES</span></span>

## <span data-ttu-id="16894-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16894-132">RELATED LINKS</span></span>

