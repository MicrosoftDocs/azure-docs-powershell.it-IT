---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182870"
---
# <span data-ttu-id="8dc1a-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="8dc1a-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="8dc1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc1a-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc1a-103">Crea un nuovo alias e un nuovo abbonamento</span><span class="sxs-lookup"><span data-stu-id="8dc1a-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="8dc1a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8dc1a-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc1a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8dc1a-105">DESCRIPTION</span></span>
<span data-ttu-id="8dc1a-106">Il cmdlet **New-AzSubscriptionAlias** crea un nuovo alias e un nuovo abbonamento</span><span class="sxs-lookup"><span data-stu-id="8dc1a-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="8dc1a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8dc1a-107">EXAMPLES</span></span>

### <span data-ttu-id="8dc1a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8dc1a-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="8dc1a-109">Crea un nuovo alias e un nuovo abbonamento</span><span class="sxs-lookup"><span data-stu-id="8dc1a-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="8dc1a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc1a-110">PARAMETERS</span></span>

### <span data-ttu-id="8dc1a-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="8dc1a-111">-AliasName</span></span>
<span data-ttu-id="8dc1a-112">Alias per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="8dc1a-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc1a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8dc1a-113">-AsJob</span></span>
<span data-ttu-id="8dc1a-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8dc1a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8dc1a-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="8dc1a-115">-BillingScope</span></span>
<span data-ttu-id="8dc1a-116">Ambito di fatturazione</span><span class="sxs-lookup"><span data-stu-id="8dc1a-116">Billing Scope</span></span>

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

### <span data-ttu-id="8dc1a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc1a-117">-DefaultProfile</span></span>
<span data-ttu-id="8dc1a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc1a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dc1a-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="8dc1a-119">-ResellerId</span></span>
<span data-ttu-id="8dc1a-120">ID rivenditore</span><span class="sxs-lookup"><span data-stu-id="8dc1a-120">Reseller Id</span></span>

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

### <span data-ttu-id="8dc1a-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8dc1a-121">-SubscriptionId</span></span>
<span data-ttu-id="8dc1a-122">ID sottoscrizione esistente</span><span class="sxs-lookup"><span data-stu-id="8dc1a-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="8dc1a-123">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8dc1a-123">-SubscriptionName</span></span>
<span data-ttu-id="8dc1a-124">Nome dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="8dc1a-124">Name of the subscription</span></span>

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

### <span data-ttu-id="8dc1a-125">-Workload</span><span class="sxs-lookup"><span data-stu-id="8dc1a-125">-Workload</span></span>
<span data-ttu-id="8dc1a-126">Tipo di carico di lavoro</span><span class="sxs-lookup"><span data-stu-id="8dc1a-126">Type of Workload</span></span>

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

### <span data-ttu-id="8dc1a-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc1a-127">-Confirm</span></span>
<span data-ttu-id="8dc1a-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc1a-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc1a-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc1a-129">-WhatIf</span></span>
<span data-ttu-id="8dc1a-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dc1a-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc1a-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8dc1a-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc1a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc1a-132">CommonParameters</span></span>
<span data-ttu-id="8dc1a-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc1a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc1a-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8dc1a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc1a-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="8dc1a-135">INPUTS</span></span>

### <span data-ttu-id="8dc1a-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8dc1a-136">None</span></span>

## <span data-ttu-id="8dc1a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8dc1a-137">OUTPUTS</span></span>

### <span data-ttu-id="8dc1a-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="8dc1a-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="8dc1a-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="8dc1a-139">NOTES</span></span>

## <span data-ttu-id="8dc1a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8dc1a-140">RELATED LINKS</span></span>
