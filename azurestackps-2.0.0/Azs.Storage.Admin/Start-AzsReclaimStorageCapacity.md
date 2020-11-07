---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861649"
---
# <span data-ttu-id="3114f-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="3114f-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="3114f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3114f-102">SYNOPSIS</span></span>


## <span data-ttu-id="3114f-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3114f-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3114f-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3114f-104">DESCRIPTION</span></span>


## <span data-ttu-id="3114f-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3114f-105">EXAMPLES</span></span>

### <span data-ttu-id="3114f-106">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="3114f-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="3114f-107">Avviare Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="3114f-107">Start garbage collection.</span></span>

## <span data-ttu-id="3114f-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3114f-108">PARAMETERS</span></span>

### <span data-ttu-id="3114f-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3114f-109">-AsJob</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3114f-110">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="3114f-111">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="3114f-112">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-113">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="3114f-113">-NoWait</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3114f-114">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3114f-115">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3114f-116">-Confirm</span></span>
<span data-ttu-id="3114f-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3114f-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3114f-118">-WhatIf</span></span>
<span data-ttu-id="3114f-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3114f-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3114f-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3114f-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3114f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3114f-121">CommonParameters</span></span>
<span data-ttu-id="3114f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3114f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3114f-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3114f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3114f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3114f-124">INPUTS</span></span>

## <span data-ttu-id="3114f-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3114f-125">OUTPUTS</span></span>

### <span data-ttu-id="3114f-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3114f-126">System.Boolean</span></span>



## <span data-ttu-id="3114f-127">Note</span><span class="sxs-lookup"><span data-stu-id="3114f-127">NOTES</span></span>

## <span data-ttu-id="3114f-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3114f-128">RELATED LINKS</span></span>

