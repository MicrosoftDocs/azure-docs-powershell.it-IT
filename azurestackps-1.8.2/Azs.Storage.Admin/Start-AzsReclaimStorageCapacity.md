---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7256c6ffa7dc3b8a227b516faad9482eb44242d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030414"
---
# <span data-ttu-id="60b50-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="60b50-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="60b50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="60b50-102">SYNOPSIS</span></span>
<span data-ttu-id="60b50-103">Avviare la Garbage Collection in oggetti di archiviazione eliminati.</span><span class="sxs-lookup"><span data-stu-id="60b50-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="60b50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60b50-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b50-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60b50-105">DESCRIPTION</span></span>
<span data-ttu-id="60b50-106">Avviare la Garbage Collection in oggetti di archiviazione eliminati.</span><span class="sxs-lookup"><span data-stu-id="60b50-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="60b50-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60b50-107">EXAMPLES</span></span>

### <span data-ttu-id="60b50-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="60b50-108">EXAMPLE 1</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="60b50-109">Avviare Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="60b50-109">Start garbage collection.</span></span>

## <span data-ttu-id="60b50-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="60b50-110">PARAMETERS</span></span>

### <span data-ttu-id="60b50-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b50-111">-ResourceGroupName</span></span>
<span data-ttu-id="60b50-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="60b50-112">Resource group name.</span></span>

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

### <span data-ttu-id="60b50-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="60b50-113">-FarmName</span></span>
<span data-ttu-id="60b50-114">ID farm.</span><span class="sxs-lookup"><span data-stu-id="60b50-114">Farm Id.</span></span>

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

### <span data-ttu-id="60b50-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60b50-115">-AsJob</span></span>
<span data-ttu-id="60b50-116">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="60b50-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="60b50-117">-Force</span><span class="sxs-lookup"><span data-stu-id="60b50-117">-Force</span></span>
<span data-ttu-id="60b50-118">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="60b50-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="60b50-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b50-119">-WhatIf</span></span>
<span data-ttu-id="60b50-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60b50-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60b50-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60b50-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b50-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="60b50-122">-Confirm</span></span>
<span data-ttu-id="60b50-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60b50-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b50-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b50-124">CommonParameters</span></span>
<span data-ttu-id="60b50-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b50-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b50-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60b50-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b50-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="60b50-127">INPUTS</span></span>

## <span data-ttu-id="60b50-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60b50-128">OUTPUTS</span></span>

## <span data-ttu-id="60b50-129">Note</span><span class="sxs-lookup"><span data-stu-id="60b50-129">NOTES</span></span>

## <span data-ttu-id="60b50-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60b50-130">RELATED LINKS</span></span>
