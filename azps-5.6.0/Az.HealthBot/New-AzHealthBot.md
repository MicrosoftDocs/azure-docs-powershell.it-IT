---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: b9c4e4cd55f81449497b0d397574c3eeec64d2d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013229"
---
# <span data-ttu-id="33eba-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="33eba-101">New-AzHealthBot</span></span>

## <span data-ttu-id="33eba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33eba-102">SYNOPSIS</span></span>
<span data-ttu-id="33eba-103">Crea un nuovo HealthBot.</span><span class="sxs-lookup"><span data-stu-id="33eba-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="33eba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33eba-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="33eba-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33eba-105">DESCRIPTION</span></span>
<span data-ttu-id="33eba-106">Crea un nuovo HealthBot.</span><span class="sxs-lookup"><span data-stu-id="33eba-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="33eba-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33eba-107">EXAMPLES</span></span>

### <span data-ttu-id="33eba-108">Esempio 1: Creare un nuovo HealthBot</span><span class="sxs-lookup"><span data-stu-id="33eba-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="33eba-109">Creare un nuovo modello HealthBot per impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="33eba-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="33eba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33eba-110">PARAMETERS</span></span>

### <span data-ttu-id="33eba-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33eba-111">-AsJob</span></span>
<span data-ttu-id="33eba-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="33eba-112">Run the command as a job</span></span>

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

### <span data-ttu-id="33eba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33eba-113">-DefaultProfile</span></span>
<span data-ttu-id="33eba-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33eba-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33eba-115">-Location</span><span class="sxs-lookup"><span data-stu-id="33eba-115">-Location</span></span>
<span data-ttu-id="33eba-116">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="33eba-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="33eba-117">-Name</span><span class="sxs-lookup"><span data-stu-id="33eba-117">-Name</span></span>
<span data-ttu-id="33eba-118">Nome della risorsa Bot.</span><span class="sxs-lookup"><span data-stu-id="33eba-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33eba-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="33eba-119">-NoWait</span></span>
<span data-ttu-id="33eba-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="33eba-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="33eba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33eba-121">-ResourceGroupName</span></span>
<span data-ttu-id="33eba-122">Nome del gruppo di risorse Bot nella sottoscrizione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="33eba-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="33eba-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="33eba-123">-Sku</span></span>
<span data-ttu-id="33eba-124">Nome dello SKU HealthBot</span><span class="sxs-lookup"><span data-stu-id="33eba-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33eba-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="33eba-125">-SubscriptionId</span></span>
<span data-ttu-id="33eba-126">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="33eba-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="33eba-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="33eba-127">-Tag</span></span>
<span data-ttu-id="33eba-128">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="33eba-128">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33eba-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33eba-129">-Confirm</span></span>
<span data-ttu-id="33eba-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33eba-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33eba-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33eba-131">-WhatIf</span></span>
<span data-ttu-id="33eba-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33eba-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33eba-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33eba-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33eba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33eba-134">CommonParameters</span></span>
<span data-ttu-id="33eba-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33eba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33eba-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33eba-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33eba-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="33eba-137">INPUTS</span></span>

## <span data-ttu-id="33eba-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33eba-138">OUTPUTS</span></span>

### <span data-ttu-id="33eba-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="33eba-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="33eba-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="33eba-140">NOTES</span></span>

<span data-ttu-id="33eba-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="33eba-141">ALIASES</span></span>

## <span data-ttu-id="33eba-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33eba-142">RELATED LINKS</span></span>

