---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentmarketplaceagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentMarketplaceAgreement.md
ms.openlocfilehash: f8c293870fa4eeb6f0df8a543473c8a9bda314c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012589"
---
# <span data-ttu-id="a578b-101">New-AzConfluentMarketplaceAgreement</span><span class="sxs-lookup"><span data-stu-id="a578b-101">New-AzConfluentMarketplaceAgreement</span></span>

## <span data-ttu-id="a578b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a578b-102">SYNOPSIS</span></span>
<span data-ttu-id="a578b-103">Accetta le condizioni del marketplace.</span><span class="sxs-lookup"><span data-stu-id="a578b-103">Accept marketplace terms.</span></span>

## <span data-ttu-id="a578b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a578b-104">SYNTAX</span></span>

```
New-AzConfluentMarketplaceAgreement [-SubscriptionId <String>] [-Accepted] [-LicenseTextLink <String>]
 [-Plan <String>] [-PrivacyPolicyLink <String>] [-Product <String>] [-Publisher <String>]
 [-RetrieveDatetime <DateTime>] [-Signature <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a578b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a578b-105">DESCRIPTION</span></span>
<span data-ttu-id="a578b-106">Accetta le condizioni del marketplace.</span><span class="sxs-lookup"><span data-stu-id="a578b-106">Accept marketplace terms.</span></span>

## <span data-ttu-id="a578b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a578b-107">EXAMPLES</span></span>

### <span data-ttu-id="a578b-108">Esempio 1: Creare un contratto di Marketplace confluente in un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a578b-108">Example 1: Create confluent marketplace agreement under a subscription</span></span>
```powershell
PS C:\> New-AzConfluentMarketplaceAgreement -Accepted

Name    Type
----    ----
default Microsoft.Confluent/agreement
```

<span data-ttu-id="a578b-109">Questo comando crea un contratto di Marketplace confluente in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a578b-109">This command create confluent marketplace agreement under a subscription.</span></span>

## <span data-ttu-id="a578b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a578b-110">PARAMETERS</span></span>

### <span data-ttu-id="a578b-111">-Accettato</span><span class="sxs-lookup"><span data-stu-id="a578b-111">-Accepted</span></span>
<span data-ttu-id="a578b-112">Se sono state accettate versioni delle condizioni, altrimenti false.</span><span class="sxs-lookup"><span data-stu-id="a578b-112">If any version of the terms have been accepted, otherwise false.</span></span>

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

### <span data-ttu-id="a578b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a578b-113">-DefaultProfile</span></span>
<span data-ttu-id="a578b-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a578b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a578b-115">-LicenseTextLink</span><span class="sxs-lookup"><span data-stu-id="a578b-115">-LicenseTextLink</span></span>
<span data-ttu-id="a578b-116">Creare un collegamento a html con i termini di Microsoft e Publisher.</span><span class="sxs-lookup"><span data-stu-id="a578b-116">Link to HTML with Microsoft and Publisher terms.</span></span>

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

### <span data-ttu-id="a578b-117">-Plan</span><span class="sxs-lookup"><span data-stu-id="a578b-117">-Plan</span></span>
<span data-ttu-id="a578b-118">Stringa identificatore del piano.</span><span class="sxs-lookup"><span data-stu-id="a578b-118">Plan identifier string.</span></span>

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

### <span data-ttu-id="a578b-119">-PrivacyPolicyLink</span><span class="sxs-lookup"><span data-stu-id="a578b-119">-PrivacyPolicyLink</span></span>
<span data-ttu-id="a578b-120">Collegamento all'informativa sulla privacy dell'autore.</span><span class="sxs-lookup"><span data-stu-id="a578b-120">Link to the privacy policy of the publisher.</span></span>

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

### <span data-ttu-id="a578b-121">-Prodotto</span><span class="sxs-lookup"><span data-stu-id="a578b-121">-Product</span></span>
<span data-ttu-id="a578b-122">Stringa dell'identificatore prodotto.</span><span class="sxs-lookup"><span data-stu-id="a578b-122">Product identifier string.</span></span>

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

### <span data-ttu-id="a578b-123">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a578b-123">-Publisher</span></span>
<span data-ttu-id="a578b-124">Stringa dell'identificatore dell'autore.</span><span class="sxs-lookup"><span data-stu-id="a578b-124">Publisher identifier string.</span></span>

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

### <span data-ttu-id="a578b-125">-RetrieveDatetime</span><span class="sxs-lookup"><span data-stu-id="a578b-125">-RetrieveDatetime</span></span>
<span data-ttu-id="a578b-126">Data e ora in FORMATO UTC in cui i termini sono stati accettati.</span><span class="sxs-lookup"><span data-stu-id="a578b-126">Date and time in UTC of when the terms were accepted.</span></span>
<span data-ttu-id="a578b-127">È vuoto se Accettato è falso.</span><span class="sxs-lookup"><span data-stu-id="a578b-127">This is empty if Accepted is false.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a578b-128">-Signature</span><span class="sxs-lookup"><span data-stu-id="a578b-128">-Signature</span></span>
<span data-ttu-id="a578b-129">Firma dei termini.</span><span class="sxs-lookup"><span data-stu-id="a578b-129">Terms signature.</span></span>

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

### <span data-ttu-id="a578b-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a578b-130">-SubscriptionId</span></span>
<span data-ttu-id="a578b-131">ID sottoscrizione Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="a578b-131">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="a578b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a578b-132">-Confirm</span></span>
<span data-ttu-id="a578b-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a578b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a578b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a578b-134">-WhatIf</span></span>
<span data-ttu-id="a578b-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a578b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a578b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a578b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a578b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a578b-137">CommonParameters</span></span>
<span data-ttu-id="a578b-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a578b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a578b-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a578b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a578b-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="a578b-140">INPUTS</span></span>

## <span data-ttu-id="a578b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a578b-141">OUTPUTS</span></span>

### <span data-ttu-id="a578b-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span><span class="sxs-lookup"><span data-stu-id="a578b-142">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IConfluentAgreementResource</span></span>

## <span data-ttu-id="a578b-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="a578b-143">NOTES</span></span>

<span data-ttu-id="a578b-144">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a578b-144">ALIASES</span></span>

## <span data-ttu-id="a578b-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a578b-145">RELATED LINKS</span></span>

