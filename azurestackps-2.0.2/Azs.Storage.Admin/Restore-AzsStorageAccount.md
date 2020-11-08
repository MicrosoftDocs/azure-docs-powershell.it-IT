---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/restore-azsstorageaccount
schema: 2.0.0
ms.openlocfilehash: 81b6a6dc960e9364d6d3e54f6e6394e17559b7f8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030471"
---
# <span data-ttu-id="ae45d-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ae45d-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="ae45d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae45d-102">SYNOPSIS</span></span>


## <span data-ttu-id="ae45d-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae45d-103">SYNTAX</span></span>

```
Restore-AzsStorageAccount -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-NewAccountName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae45d-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae45d-104">DESCRIPTION</span></span>


## <span data-ttu-id="ae45d-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae45d-105">EXAMPLES</span></span>

### <span data-ttu-id="ae45d-106">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="ae45d-106">Example 1:</span></span>
```powershell
PS C:\> Restore-AzsStorageAccount -Name 32cbc1173bde4e5fad04e11cc4cb2e00 
```

<span data-ttu-id="ae45d-107">Annullare l'eliminazione di un account di archiviazione eliminato.</span><span class="sxs-lookup"><span data-stu-id="ae45d-107">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="ae45d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae45d-108">PARAMETERS</span></span>

### <span data-ttu-id="ae45d-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae45d-109">-AsJob</span></span>


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

### <span data-ttu-id="ae45d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae45d-110">-DefaultProfile</span></span>


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

### <span data-ttu-id="ae45d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ae45d-111">-Force</span></span>


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

### <span data-ttu-id="ae45d-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ae45d-112">-Location</span></span>


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

### <span data-ttu-id="ae45d-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae45d-113">-Name</span></span>


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

### <span data-ttu-id="ae45d-114">-NewAccountName</span><span class="sxs-lookup"><span data-stu-id="ae45d-114">-NewAccountName</span></span>


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

### <span data-ttu-id="ae45d-115">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ae45d-115">-NoWait</span></span>


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

### <span data-ttu-id="ae45d-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae45d-116">-PassThru</span></span>


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

### <span data-ttu-id="ae45d-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae45d-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="ae45d-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae45d-118">-Confirm</span></span>
<span data-ttu-id="ae45d-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae45d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae45d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae45d-120">-WhatIf</span></span>
<span data-ttu-id="ae45d-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae45d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae45d-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae45d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae45d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae45d-123">CommonParameters</span></span>
<span data-ttu-id="ae45d-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae45d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae45d-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae45d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae45d-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae45d-126">INPUTS</span></span>

## <span data-ttu-id="ae45d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae45d-127">OUTPUTS</span></span>

### <span data-ttu-id="ae45d-128">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae45d-128">System.Boolean</span></span>



## <span data-ttu-id="ae45d-129">Note</span><span class="sxs-lookup"><span data-stu-id="ae45d-129">NOTES</span></span>

## <span data-ttu-id="ae45d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae45d-130">RELATED LINKS</span></span>

