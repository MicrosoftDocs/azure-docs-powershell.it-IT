---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685182"
---
# <span data-ttu-id="7a82c-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="7a82c-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="7a82c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7a82c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a82c-103">Avviare la Garbage Collection in oggetti di archiviazione eliminati.</span><span class="sxs-lookup"><span data-stu-id="7a82c-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="7a82c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7a82c-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a82c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7a82c-105">DESCRIPTION</span></span>
<span data-ttu-id="7a82c-106">Avviare la Garbage Collection in oggetti di archiviazione eliminati.</span><span class="sxs-lookup"><span data-stu-id="7a82c-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="7a82c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7a82c-107">EXAMPLES</span></span>

### <span data-ttu-id="7a82c-108">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7a82c-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="7a82c-109">Avviare Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="7a82c-109">Start garbage collection.</span></span>

## <span data-ttu-id="7a82c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7a82c-110">PARAMETERS</span></span>

### <span data-ttu-id="7a82c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a82c-111">-AsJob</span></span>
<span data-ttu-id="7a82c-112">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="7a82c-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7a82c-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="7a82c-113">-FarmName</span></span>
<span data-ttu-id="7a82c-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="7a82c-114">Farm Id.</span></span>

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

### <span data-ttu-id="7a82c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a82c-115">-Force</span></span>
<span data-ttu-id="7a82c-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="7a82c-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7a82c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a82c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a82c-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7a82c-118">Resource group name.</span></span>

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

### <span data-ttu-id="7a82c-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7a82c-119">-Confirm</span></span>
<span data-ttu-id="7a82c-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a82c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a82c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a82c-121">-WhatIf</span></span>
<span data-ttu-id="7a82c-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a82c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a82c-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7a82c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a82c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a82c-124">CommonParameters</span></span>
<span data-ttu-id="7a82c-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a82c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a82c-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a82c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a82c-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7a82c-127">INPUTS</span></span>

## <span data-ttu-id="7a82c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7a82c-128">OUTPUTS</span></span>

## <span data-ttu-id="7a82c-129">Note</span><span class="sxs-lookup"><span data-stu-id="7a82c-129">NOTES</span></span>

## <span data-ttu-id="7a82c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7a82c-130">RELATED LINKS</span></span>
