---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd62756b3a41af82a245a39d4f80478d47d90e1c
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2020
ms.locfileid: "93859838"
---
# <span data-ttu-id="f4663-101">Get-AzsReclaimStorageCapacityStatus</span><span class="sxs-lookup"><span data-stu-id="f4663-101">Get-AzsReclaimStorageCapacityStatus</span></span>

## <span data-ttu-id="f4663-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4663-102">SYNOPSIS</span></span>
<span data-ttu-id="f4663-103">Restituisce lo stato del processo di Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="f4663-103">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="f4663-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4663-104">SYNTAX</span></span>

```
Get-AzsReclaimStorageCapacityStatus [-FarmName] <String> [-JobId] <String> [[-ResourceGroupName] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4663-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4663-105">DESCRIPTION</span></span>
<span data-ttu-id="f4663-106">Restituisce lo stato del processo di Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="f4663-106">Returns the state of the garbage collection job.</span></span>

## <span data-ttu-id="f4663-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4663-107">EXAMPLES</span></span>

### <span data-ttu-id="f4663-108">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="f4663-108">EXAMPLE 1</span></span>
```
Get-AzsReclaimStorageCapacityStatus -FarmName "6ddbfe6e-8781-4a3d-b370-4a8b20a494d8" -JobId "92360f29-cd21-429d-a20b-9b11ab5902a0"
```

<span data-ttu-id="f4663-109">Restituiscono informazioni sullo stato di Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="f4663-109">Return information about the status of garbage collection.</span></span>

## <span data-ttu-id="f4663-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4663-110">PARAMETERS</span></span>

### <span data-ttu-id="f4663-111">-Farmname</span><span class="sxs-lookup"><span data-stu-id="f4663-111">-FarmName</span></span>
<span data-ttu-id="f4663-112">ID farm.</span><span class="sxs-lookup"><span data-stu-id="f4663-112">Farm Id.</span></span>

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

### <span data-ttu-id="f4663-113">-JobId</span><span class="sxs-lookup"><span data-stu-id="f4663-113">-JobId</span></span>
<span data-ttu-id="f4663-114">ID operazione.</span><span class="sxs-lookup"><span data-stu-id="f4663-114">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4663-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4663-115">-ResourceGroupName</span></span>
<span data-ttu-id="f4663-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f4663-116">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4663-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4663-117">CommonParameters</span></span>
<span data-ttu-id="f4663-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4663-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4663-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4663-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4663-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4663-120">INPUTS</span></span>

## <span data-ttu-id="f4663-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4663-121">OUTPUTS</span></span>

## <span data-ttu-id="f4663-122">Note</span><span class="sxs-lookup"><span data-stu-id="f4663-122">NOTES</span></span>

## <span data-ttu-id="f4663-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4663-123">RELATED LINKS</span></span>
