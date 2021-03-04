---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 8c934adfd0bea950f97fbe8e8226568f9eaf57dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959789"
---
# <span data-ttu-id="bd7e7-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="bd7e7-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="bd7e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7e7-103">Ottenere account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-103">Get billing accounts.</span></span>

## <span data-ttu-id="bd7e7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bd7e7-104">SYNTAX</span></span>

### <span data-ttu-id="bd7e7-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bd7e7-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd7e7-106">Single</span><span class="sxs-lookup"><span data-stu-id="bd7e7-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd7e7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bd7e7-107">DESCRIPTION</span></span>
<span data-ttu-id="bd7e7-108">Il cmdlet **Get-AzBillingAccount** ottiene gli account di fatturazione a cui l'utente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="bd7e7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bd7e7-109">EXAMPLES</span></span>

### <span data-ttu-id="bd7e7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bd7e7-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="bd7e7-111">Ottieni tutti gli account di fatturazione a cui l'utente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="bd7e7-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="bd7e7-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="bd7e7-113">Ottenere l'account di fatturazione con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="bd7e7-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="bd7e7-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="bd7e7-115">Ottieni tutti gli account di fatturazione a cui l'utente ha accesso e includi l'indirizzo nel risultato.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="bd7e7-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="bd7e7-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="bd7e7-117">Ottieni tutti gli account di fatturazione a cui l'utente ha accesso e includi i profili di fatturazione nel risultato.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="bd7e7-118">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="bd7e7-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="bd7e7-119">Ottenere tutti gli account di fatturazione a cui l'utente ha accesso e includere i profili di fatturazione e le sezioni delle fatture al di sotto di essi nei risultati.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="bd7e7-120">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="bd7e7-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="bd7e7-121">Ottenere l'account di fatturazione con il nome specificato e includere l'indirizzo, i profili di fatturazione e le sezioni delle fatture al di sotto di essi nel risultato.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="bd7e7-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd7e7-122">PARAMETERS</span></span>

### <span data-ttu-id="bd7e7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7e7-123">-DefaultProfile</span></span>
<span data-ttu-id="bd7e7-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bd7e7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd7e7-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="bd7e7-125">-IncludeAddress</span></span>
<span data-ttu-id="bd7e7-126">Includere l'indirizzo dell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="bd7e7-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="bd7e7-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="bd7e7-128">Includere i profili di fatturazione nell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="bd7e7-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="bd7e7-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="bd7e7-130">Includere i profili di fatturazione nelle sezioni account di fatturazione e fatture.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="bd7e7-131">-Name</span><span class="sxs-lookup"><span data-stu-id="bd7e7-131">-Name</span></span>
<span data-ttu-id="bd7e7-132">Nome di un account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-132">Name of a specific billing account.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Single
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e7-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="bd7e7-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="bd7e7-134">Elenca le entità di fatturazione sotto l'account di fatturazione che possono essere usate come input per creare una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Single
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd7e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7e7-135">CommonParameters</span></span>
<span data-ttu-id="bd7e7-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7e7-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd7e7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7e7-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="bd7e7-138">INPUTS</span></span>

### <span data-ttu-id="bd7e7-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bd7e7-139">None</span></span>

## <span data-ttu-id="bd7e7-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bd7e7-140">OUTPUTS</span></span>

### <span data-ttu-id="bd7e7-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="bd7e7-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="bd7e7-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="bd7e7-142">NOTES</span></span>

## <span data-ttu-id="bd7e7-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bd7e7-143">RELATED LINKS</span></span>
