---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859493"
---
# <span data-ttu-id="194a1-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="194a1-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="194a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="194a1-102">SYNOPSIS</span></span>
<span data-ttu-id="194a1-103">Annullare un processo di migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="194a1-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="194a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="194a1-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="194a1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="194a1-105">DESCRIPTION</span></span>
<span data-ttu-id="194a1-106">Annullare un processo di migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="194a1-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="194a1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="194a1-107">EXAMPLES</span></span>

### <span data-ttu-id="194a1-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="194a1-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="194a1-109">Annullare la migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="194a1-109">Cancel container migration.</span></span>

## <span data-ttu-id="194a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="194a1-110">PARAMETERS</span></span>

### <span data-ttu-id="194a1-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="194a1-111">-JobId</span></span>
<span data-ttu-id="194a1-112">ID operazione.</span><span class="sxs-lookup"><span data-stu-id="194a1-112">Operation Id.</span></span>

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

### <span data-ttu-id="194a1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="194a1-113">-ResourceGroupName</span></span>
<span data-ttu-id="194a1-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="194a1-114">Resource group name.</span></span>

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

### <span data-ttu-id="194a1-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="194a1-115">-FarmName</span></span>
<span data-ttu-id="194a1-116">ID farm.</span><span class="sxs-lookup"><span data-stu-id="194a1-116">Farm Id.</span></span>

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

### <span data-ttu-id="194a1-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="194a1-117">-AsJob</span></span>
<span data-ttu-id="194a1-118">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="194a1-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="194a1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="194a1-119">-Force</span></span>
<span data-ttu-id="194a1-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="194a1-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="194a1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="194a1-121">-WhatIf</span></span>
<span data-ttu-id="194a1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="194a1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="194a1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="194a1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="194a1-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="194a1-124">-Confirm</span></span>
<span data-ttu-id="194a1-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="194a1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="194a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="194a1-126">CommonParameters</span></span>
<span data-ttu-id="194a1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="194a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="194a1-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="194a1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="194a1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="194a1-129">INPUTS</span></span>

## <span data-ttu-id="194a1-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="194a1-130">OUTPUTS</span></span>

## <span data-ttu-id="194a1-131">Note</span><span class="sxs-lookup"><span data-stu-id="194a1-131">NOTES</span></span>

## <span data-ttu-id="194a1-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="194a1-132">RELATED LINKS</span></span>
