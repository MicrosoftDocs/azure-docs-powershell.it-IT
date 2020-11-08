---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 5523170e571fbd1dc93bd0fa4223aba3b324d3b0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2020
ms.locfileid: "94023345"
---
# <span data-ttu-id="d76cb-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d76cb-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="d76cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d76cb-102">SYNOPSIS</span></span>


## <span data-ttu-id="d76cb-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d76cb-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d76cb-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d76cb-104">DESCRIPTION</span></span>


## <span data-ttu-id="d76cb-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d76cb-105">EXAMPLES</span></span>

### <span data-ttu-id="d76cb-106">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="d76cb-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="d76cb-107">Annullare l'eliminazione di un account di archiviazione eliminato.</span><span class="sxs-lookup"><span data-stu-id="d76cb-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="d76cb-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d76cb-108">PARAMETERS</span></span>

### <span data-ttu-id="d76cb-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d76cb-109">-AsJob</span></span>


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

### <span data-ttu-id="d76cb-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76cb-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="d76cb-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d76cb-111">-Force</span></span>


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

### <span data-ttu-id="d76cb-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d76cb-112">-Location</span></span>


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

### <span data-ttu-id="d76cb-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d76cb-113">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d76cb-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="d76cb-114">-NewAccountName</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d76cb-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d76cb-115">-NoWait</span></span>


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

### <span data-ttu-id="d76cb-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d76cb-116">-PassThru</span></span>


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

### <span data-ttu-id="d76cb-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d76cb-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="d76cb-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d76cb-118">-Confirm</span></span>
<span data-ttu-id="d76cb-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d76cb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d76cb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d76cb-120">-WhatIf</span></span>
<span data-ttu-id="d76cb-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d76cb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d76cb-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d76cb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d76cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76cb-123">CommonParameters</span></span>
<span data-ttu-id="d76cb-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d76cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76cb-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d76cb-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76cb-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d76cb-126">INPUTS</span></span>

## <span data-ttu-id="d76cb-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d76cb-127">OUTPUTS</span></span>

### <span data-ttu-id="d76cb-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d76cb-128">System.Boolean</span></span>



## <span data-ttu-id="d76cb-129">Note</span><span class="sxs-lookup"><span data-stu-id="d76cb-129">NOTES</span></span>

## <span data-ttu-id="d76cb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d76cb-130">RELATED LINKS</span></span>

