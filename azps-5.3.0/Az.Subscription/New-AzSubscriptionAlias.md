---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384215"
---
# <span data-ttu-id="98ffd-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="98ffd-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="98ffd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="98ffd-103">Crea un nuovo alias e un abbonamento</span><span class="sxs-lookup"><span data-stu-id="98ffd-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="98ffd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98ffd-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98ffd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="98ffd-106">Il cmdlet **New-AzSubscriptionAlias** crea un nuovo alias e un abbonamento</span><span class="sxs-lookup"><span data-stu-id="98ffd-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="98ffd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="98ffd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98ffd-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="98ffd-109">Crea un nuovo alias e un abbonamento</span><span class="sxs-lookup"><span data-stu-id="98ffd-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="98ffd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98ffd-110">PARAMETERS</span></span>

### <span data-ttu-id="98ffd-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="98ffd-111">-AliasName</span></span>
<span data-ttu-id="98ffd-112">Alias per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="98ffd-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="98ffd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98ffd-113">-AsJob</span></span>
<span data-ttu-id="98ffd-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="98ffd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98ffd-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="98ffd-115">-BillingScope</span></span>
<span data-ttu-id="98ffd-116">Ambito di fatturazione</span><span class="sxs-lookup"><span data-stu-id="98ffd-116">Billing Scope</span></span>

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

### <span data-ttu-id="98ffd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98ffd-117">-DefaultProfile</span></span>
<span data-ttu-id="98ffd-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98ffd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98ffd-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="98ffd-119">-ResellerId</span></span>
<span data-ttu-id="98ffd-120">ID rivenditore</span><span class="sxs-lookup"><span data-stu-id="98ffd-120">Reseller Id</span></span>

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

### <span data-ttu-id="98ffd-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="98ffd-121">-SubscriptionId</span></span>
<span data-ttu-id="98ffd-122">ID abbonamento esistente</span><span class="sxs-lookup"><span data-stu-id="98ffd-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="98ffd-123">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="98ffd-123">-SubscriptionName</span></span>
<span data-ttu-id="98ffd-124">Nome dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="98ffd-124">Name of the subscription</span></span>

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

### <span data-ttu-id="98ffd-125">-Carico di lavoro</span><span class="sxs-lookup"><span data-stu-id="98ffd-125">-Workload</span></span>
<span data-ttu-id="98ffd-126">Tipo di carico di lavoro</span><span class="sxs-lookup"><span data-stu-id="98ffd-126">Type of Workload</span></span>

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

### <span data-ttu-id="98ffd-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="98ffd-127">-Confirm</span></span>
<span data-ttu-id="98ffd-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98ffd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98ffd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98ffd-129">-WhatIf</span></span>
<span data-ttu-id="98ffd-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98ffd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98ffd-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="98ffd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98ffd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98ffd-132">CommonParameters</span></span>
<span data-ttu-id="98ffd-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98ffd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98ffd-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98ffd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98ffd-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98ffd-135">INPUTS</span></span>

### <span data-ttu-id="98ffd-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="98ffd-136">None</span></span>

## <span data-ttu-id="98ffd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98ffd-137">OUTPUTS</span></span>

### <span data-ttu-id="98ffd-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="98ffd-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="98ffd-139">Note</span><span class="sxs-lookup"><span data-stu-id="98ffd-139">NOTES</span></span>

## <span data-ttu-id="98ffd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98ffd-140">RELATED LINKS</span></span>
