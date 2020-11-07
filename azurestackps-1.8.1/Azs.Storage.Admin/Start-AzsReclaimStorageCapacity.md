---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7256c6ffa7dc3b8a227b516faad9482eb44242d5
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859957"
---
# <span data-ttu-id="597b1-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="597b1-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="597b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="597b1-102">SYNOPSIS</span></span>
<span data-ttu-id="597b1-103">Avviare la Garbage Collection in oggetti di archiviazione eliminati.</span><span class="sxs-lookup"><span data-stu-id="597b1-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="597b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="597b1-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="597b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="597b1-105">DESCRIPTION</span></span>
<span data-ttu-id="597b1-106">Avviare la Garbage Collection in oggetti di archiviazione eliminati.</span><span class="sxs-lookup"><span data-stu-id="597b1-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="597b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="597b1-107">EXAMPLES</span></span>

### <span data-ttu-id="597b1-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="597b1-108">EXAMPLE 1</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="597b1-109">Avviare Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="597b1-109">Start garbage collection.</span></span>

## <span data-ttu-id="597b1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="597b1-110">PARAMETERS</span></span>

### <span data-ttu-id="597b1-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="597b1-111">-ResourceGroupName</span></span>
<span data-ttu-id="597b1-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="597b1-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b1-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="597b1-113">-FarmName</span></span>
<span data-ttu-id="597b1-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="597b1-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="597b1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="597b1-115">-AsJob</span></span>
<span data-ttu-id="597b1-116">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="597b1-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="597b1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="597b1-117">-Force</span></span>
<span data-ttu-id="597b1-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="597b1-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="597b1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="597b1-119">-WhatIf</span></span>
<span data-ttu-id="597b1-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="597b1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="597b1-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="597b1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="597b1-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="597b1-122">-Confirm</span></span>
<span data-ttu-id="597b1-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="597b1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="597b1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597b1-124">CommonParameters</span></span>
<span data-ttu-id="597b1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="597b1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597b1-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597b1-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597b1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="597b1-127">INPUTS</span></span>

## <span data-ttu-id="597b1-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="597b1-128">OUTPUTS</span></span>

## <span data-ttu-id="597b1-129">Note</span><span class="sxs-lookup"><span data-stu-id="597b1-129">NOTES</span></span>

## <span data-ttu-id="597b1-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="597b1-130">RELATED LINKS</span></span>
