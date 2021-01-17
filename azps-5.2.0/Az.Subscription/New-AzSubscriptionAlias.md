---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscriptionAlias.md
ms.openlocfilehash: 2e957f3a149c4aac30ac83c03997611125aa7870
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367947"
---
# <span data-ttu-id="19c06-101">New-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="19c06-101">New-AzSubscriptionAlias</span></span>

## <span data-ttu-id="19c06-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19c06-102">SYNOPSIS</span></span>
<span data-ttu-id="19c06-103">Crea un nuovo alias e un abbonamento</span><span class="sxs-lookup"><span data-stu-id="19c06-103">Creates new alias and subscription</span></span>

## <span data-ttu-id="19c06-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19c06-104">SYNTAX</span></span>

```
New-AzSubscriptionAlias -AliasName <String> [-BillingScope <String>] [-Workload <String>]
 [-SubscriptionName <String>] [-ResellerId <String>] [-SubscriptionId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c06-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19c06-105">DESCRIPTION</span></span>
<span data-ttu-id="19c06-106">Il cmdlet **New-AzSubscriptionAlias** crea un nuovo alias e un abbonamento</span><span class="sxs-lookup"><span data-stu-id="19c06-106">The **New-AzSubscriptionAlias** cmdlet creates new alias and subscription</span></span>

## <span data-ttu-id="19c06-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19c06-107">EXAMPLES</span></span>

### <span data-ttu-id="19c06-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19c06-108">Example 1</span></span>
```powershell
PS C:\> New-AzSubscriptionAlias -AliasName "NewAliasName" -SubscriptionName "SubscriptionName" -BillingScope "BillingScope" -Workload "WorkloadType"
```

<span data-ttu-id="19c06-109">Crea un nuovo alias e un abbonamento</span><span class="sxs-lookup"><span data-stu-id="19c06-109">Creates new alias and subscription</span></span>

## <span data-ttu-id="19c06-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19c06-110">PARAMETERS</span></span>

### <span data-ttu-id="19c06-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="19c06-111">-AliasName</span></span>
<span data-ttu-id="19c06-112">Alias per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="19c06-112">Alias for the subscription</span></span>

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

### <span data-ttu-id="19c06-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19c06-113">-AsJob</span></span>
<span data-ttu-id="19c06-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="19c06-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19c06-115">-BillingScope</span><span class="sxs-lookup"><span data-stu-id="19c06-115">-BillingScope</span></span>
<span data-ttu-id="19c06-116">Ambito di fatturazione</span><span class="sxs-lookup"><span data-stu-id="19c06-116">Billing Scope</span></span>

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

### <span data-ttu-id="19c06-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c06-117">-DefaultProfile</span></span>
<span data-ttu-id="19c06-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19c06-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c06-119">-ResellerId</span><span class="sxs-lookup"><span data-stu-id="19c06-119">-ResellerId</span></span>
<span data-ttu-id="19c06-120">ID rivenditore</span><span class="sxs-lookup"><span data-stu-id="19c06-120">Reseller Id</span></span>

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

### <span data-ttu-id="19c06-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19c06-121">-SubscriptionId</span></span>
<span data-ttu-id="19c06-122">ID abbonamento esistente</span><span class="sxs-lookup"><span data-stu-id="19c06-122">Existing Subscription Id</span></span>

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

### <span data-ttu-id="19c06-123">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="19c06-123">-SubscriptionName</span></span>
<span data-ttu-id="19c06-124">Nome dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="19c06-124">Name of the subscription</span></span>

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

### <span data-ttu-id="19c06-125">-Carico di lavoro</span><span class="sxs-lookup"><span data-stu-id="19c06-125">-Workload</span></span>
<span data-ttu-id="19c06-126">Tipo di carico di lavoro</span><span class="sxs-lookup"><span data-stu-id="19c06-126">Type of Workload</span></span>

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

### <span data-ttu-id="19c06-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="19c06-127">-Confirm</span></span>
<span data-ttu-id="19c06-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c06-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c06-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c06-129">-WhatIf</span></span>
<span data-ttu-id="19c06-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19c06-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c06-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="19c06-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c06-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c06-132">CommonParameters</span></span>
<span data-ttu-id="19c06-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c06-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c06-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19c06-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c06-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19c06-135">INPUTS</span></span>

### <span data-ttu-id="19c06-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="19c06-136">None</span></span>

## <span data-ttu-id="19c06-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19c06-137">OUTPUTS</span></span>

### <span data-ttu-id="19c06-138">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="19c06-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="19c06-139">Note</span><span class="sxs-lookup"><span data-stu-id="19c06-139">NOTES</span></span>

## <span data-ttu-id="19c06-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19c06-140">RELATED LINKS</span></span>
