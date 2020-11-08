---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030065"
---
# <span data-ttu-id="868b9-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="868b9-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="868b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="868b9-102">SYNOPSIS</span></span>
<span data-ttu-id="868b9-103">Annullare un processo di migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="868b9-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="868b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="868b9-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="868b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="868b9-105">DESCRIPTION</span></span>
<span data-ttu-id="868b9-106">Annullare un processo di migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="868b9-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="868b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="868b9-107">EXAMPLES</span></span>

### <span data-ttu-id="868b9-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="868b9-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="868b9-109">Annullare la migrazione di contenitori.</span><span class="sxs-lookup"><span data-stu-id="868b9-109">Cancel container migration.</span></span>

## <span data-ttu-id="868b9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="868b9-110">PARAMETERS</span></span>

### <span data-ttu-id="868b9-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="868b9-111">-JobId</span></span>
<span data-ttu-id="868b9-112">ID operazione.</span><span class="sxs-lookup"><span data-stu-id="868b9-112">Operation Id.</span></span>

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

### <span data-ttu-id="868b9-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="868b9-113">-ResourceGroupName</span></span>
<span data-ttu-id="868b9-114">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="868b9-114">Resource group name.</span></span>

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

### <span data-ttu-id="868b9-115">-Farmname</span><span class="sxs-lookup"><span data-stu-id="868b9-115">-FarmName</span></span>
<span data-ttu-id="868b9-116">ID farm.</span><span class="sxs-lookup"><span data-stu-id="868b9-116">Farm Id.</span></span>

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

### <span data-ttu-id="868b9-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="868b9-117">-AsJob</span></span>
<span data-ttu-id="868b9-118">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="868b9-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="868b9-119">-Force</span><span class="sxs-lookup"><span data-stu-id="868b9-119">-Force</span></span>
<span data-ttu-id="868b9-120">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="868b9-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="868b9-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="868b9-121">-WhatIf</span></span>
<span data-ttu-id="868b9-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="868b9-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="868b9-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="868b9-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="868b9-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="868b9-124">-Confirm</span></span>
<span data-ttu-id="868b9-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="868b9-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="868b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868b9-126">CommonParameters</span></span>
<span data-ttu-id="868b9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="868b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868b9-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="868b9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868b9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="868b9-129">INPUTS</span></span>

## <span data-ttu-id="868b9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="868b9-130">OUTPUTS</span></span>

## <span data-ttu-id="868b9-131">Note</span><span class="sxs-lookup"><span data-stu-id="868b9-131">NOTES</span></span>

## <span data-ttu-id="868b9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="868b9-132">RELATED LINKS</span></span>
