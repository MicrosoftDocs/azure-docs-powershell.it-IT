---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/set-azsstoragesettings
schema: 2.0.0
ms.openlocfilehash: 0b06ef857a7c035b7069b7a8b33db2d1763091e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863973"
---
# <span data-ttu-id="e2937-101">Set-AzsStorageSettings</span><span class="sxs-lookup"><span data-stu-id="e2937-101">Set-AzsStorageSettings</span></span>

## <span data-ttu-id="e2937-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2937-102">SYNOPSIS</span></span>


## <span data-ttu-id="e2937-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2937-103">SYNTAX</span></span>

```
Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays <Int32> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Force] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e2937-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2937-104">DESCRIPTION</span></span>


## <span data-ttu-id="e2937-105">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2937-105">EXAMPLES</span></span>

### <span data-ttu-id="e2937-106">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="e2937-106">Example 1:</span></span>
```powershell
PS C:\> Set-AzsStorageSettings -RetentionPeriodForDeletedStorageAccountsInDays 1
```

<span data-ttu-id="e2937-107">Aggiornare le impostazioni di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e2937-107">Update the storage settings.</span></span>

## <span data-ttu-id="e2937-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2937-108">PARAMETERS</span></span>

### <span data-ttu-id="e2937-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2937-109">-DefaultProfile</span></span>


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

### <span data-ttu-id="e2937-110">-Force</span><span class="sxs-lookup"><span data-stu-id="e2937-110">-Force</span></span>


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

### <span data-ttu-id="e2937-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e2937-111">-Location</span></span>


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

### <span data-ttu-id="e2937-112">-RetentionPeriodForDeletedStorageAccountsInDays</span><span class="sxs-lookup"><span data-stu-id="e2937-112">-RetentionPeriodForDeletedStorageAccountsInDays</span></span>


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e2937-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2937-113">-SubscriptionId</span></span>


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

### <span data-ttu-id="e2937-114">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e2937-114">-Confirm</span></span>
<span data-ttu-id="e2937-115">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2937-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2937-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2937-116">-WhatIf</span></span>
<span data-ttu-id="e2937-117">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2937-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2937-118">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e2937-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2937-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2937-119">CommonParameters</span></span>
<span data-ttu-id="e2937-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2937-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2937-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2937-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2937-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2937-122">INPUTS</span></span>

## <span data-ttu-id="e2937-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2937-123">OUTPUTS</span></span>

### <span data-ttu-id="e2937-124">Microsoft. Azure. PowerShell. Cmdlets. StorageAdmin. Models. Api201908Preview. ISettings</span><span class="sxs-lookup"><span data-stu-id="e2937-124">Microsoft.Azure.PowerShell.Cmdlets.StorageAdmin.Models.Api201908Preview.ISettings</span></span>



## <span data-ttu-id="e2937-125">Note</span><span class="sxs-lookup"><span data-stu-id="e2937-125">NOTES</span></span>

## <span data-ttu-id="e2937-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2937-126">RELATED LINKS</span></span>

