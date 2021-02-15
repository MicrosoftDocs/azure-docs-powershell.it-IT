---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182015"
---
# <span data-ttu-id="8a2bd-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="8a2bd-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="8a2bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a2bd-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2bd-103">Ottenere account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-103">Get billing accounts.</span></span>

## <span data-ttu-id="8a2bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a2bd-104">SYNTAX</span></span>

### <span data-ttu-id="8a2bd-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a2bd-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2bd-106">Single</span><span class="sxs-lookup"><span data-stu-id="8a2bd-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a2bd-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8a2bd-107">DESCRIPTION</span></span>
<span data-ttu-id="8a2bd-108">Il **cmdlet Get-AzBillingAccount** ottiene gli account di fatturazione a cui l'utente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="8a2bd-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a2bd-109">EXAMPLES</span></span>

### <span data-ttu-id="8a2bd-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a2bd-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="8a2bd-111">Ottieni tutti gli account di fatturazione a cui l'utente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="8a2bd-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8a2bd-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="8a2bd-113">Ottenere l'account di fatturazione con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="8a2bd-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8a2bd-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="8a2bd-115">Ottieni tutti gli account di fatturazione a cui l'utente ha accesso e includi l'indirizzo nel risultato.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="8a2bd-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="8a2bd-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="8a2bd-117">Ottieni tutti gli account di fatturazione a cui l'utente ha accesso e includi i profili di fatturazione nel risultato.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="8a2bd-118">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="8a2bd-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="8a2bd-119">Ottenere tutti gli account di fatturazione a cui l'utente ha accesso e includere i profili di fatturazione e le sezioni delle fatture al di sotto di essi nei risultati.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="8a2bd-120">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="8a2bd-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="8a2bd-121">Ottenere l'account di fatturazione con il nome specificato e includere l'indirizzo, i profili di fatturazione e le sezioni delle fatture al di sotto di essi nel risultato.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="8a2bd-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a2bd-122">PARAMETERS</span></span>

### <span data-ttu-id="8a2bd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2bd-123">-DefaultProfile</span></span>
<span data-ttu-id="8a2bd-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8a2bd-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a2bd-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="8a2bd-125">-IncludeAddress</span></span>
<span data-ttu-id="8a2bd-126">Includere l'indirizzo dell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="8a2bd-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="8a2bd-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="8a2bd-128">Includere i profili di fatturazione nell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="8a2bd-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="8a2bd-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="8a2bd-130">Includere i profili di fatturazione nelle sezioni account di fatturazione e fatture.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="8a2bd-131">-Name</span><span class="sxs-lookup"><span data-stu-id="8a2bd-131">-Name</span></span>
<span data-ttu-id="8a2bd-132">Nome di un account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="8a2bd-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="8a2bd-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="8a2bd-134">Elencare le entità di fatturazione nell'account di fatturazione che possono essere usate come input per creare una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="8a2bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2bd-135">CommonParameters</span></span>
<span data-ttu-id="8a2bd-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2bd-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a2bd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2bd-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="8a2bd-138">INPUTS</span></span>

### <span data-ttu-id="8a2bd-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a2bd-139">None</span></span>

## <span data-ttu-id="8a2bd-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a2bd-140">OUTPUTS</span></span>

### <span data-ttu-id="8a2bd-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="8a2bd-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="8a2bd-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="8a2bd-142">NOTES</span></span>

## <span data-ttu-id="8a2bd-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a2bd-143">RELATED LINKS</span></span>
