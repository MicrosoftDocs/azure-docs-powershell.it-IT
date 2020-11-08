---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/start-azsreclaimstoragecapacity
schema: 2.0.0
ms.openlocfilehash: bb2eecb93a7a18559dc6fbe58cd5f07c737e16b5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023113"
---
# <span data-ttu-id="d0705-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="d0705-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="d0705-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0705-102">SYNOPSIS</span></span>


## <span data-ttu-id="d0705-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0705-103">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0705-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0705-104">DESCRIPTION</span></span>


## <span data-ttu-id="d0705-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0705-105">EXAMPLES</span></span>

### <span data-ttu-id="d0705-106">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="d0705-106">Example 1:</span></span>
```powershell
PS C:\> Start-AzsReclaimStorageCapacity
```

<span data-ttu-id="d0705-107">Avviare Garbage Collection.</span><span class="sxs-lookup"><span data-stu-id="d0705-107">Start garbage collection.</span></span>

## <span data-ttu-id="d0705-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0705-108">PARAMETERS</span></span>

### <span data-ttu-id="d0705-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0705-109">-AsJob</span></span>


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

### <span data-ttu-id="d0705-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0705-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="d0705-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d0705-111">-Force</span></span>


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

### <span data-ttu-id="d0705-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d0705-112">-Location</span></span>


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

### <span data-ttu-id="d0705-113">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d0705-113">-NoWait</span></span>


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

### <span data-ttu-id="d0705-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0705-114">-PassThru</span></span>


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

### <span data-ttu-id="d0705-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0705-115">-SubscriptionId</span></span>


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

### <span data-ttu-id="d0705-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d0705-116">-Confirm</span></span>
<span data-ttu-id="d0705-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0705-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0705-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0705-118">-WhatIf</span></span>
<span data-ttu-id="d0705-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0705-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0705-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d0705-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0705-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0705-121">CommonParameters</span></span>
<span data-ttu-id="d0705-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0705-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0705-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d0705-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0705-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0705-124">INPUTS</span></span>

## <span data-ttu-id="d0705-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0705-125">OUTPUTS</span></span>

### <span data-ttu-id="d0705-126">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d0705-126">System.Boolean</span></span>



## <span data-ttu-id="d0705-127">Note</span><span class="sxs-lookup"><span data-stu-id="d0705-127">NOTES</span></span>

## <span data-ttu-id="d0705-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0705-128">RELATED LINKS</span></span>

