---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351235"
---
# <span data-ttu-id="4c657-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="4c657-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="4c657-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c657-102">SYNOPSIS</span></span>
<span data-ttu-id="4c657-103">Ottenere gli account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="4c657-103">Get billing accounts.</span></span>

## <span data-ttu-id="4c657-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c657-104">SYNTAX</span></span>

### <span data-ttu-id="4c657-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c657-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4c657-106">Singola</span><span class="sxs-lookup"><span data-stu-id="4c657-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c657-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c657-107">DESCRIPTION</span></span>
<span data-ttu-id="4c657-108">Il cmdlet **Get-AzBillingAccount** ottiene gli account di fatturazione, a cui l'utente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="4c657-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="4c657-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c657-109">EXAMPLES</span></span>

### <span data-ttu-id="4c657-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c657-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="4c657-111">Ottenere l'accesso a tutti gli account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="4c657-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="4c657-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4c657-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="4c657-113">Ottenere l'account di fatturazione con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="4c657-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="4c657-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4c657-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="4c657-115">Ottenere tutti gli account di fatturazione che l'utente ha accesso e includere l'indirizzo nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4c657-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="4c657-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="4c657-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="4c657-117">Ottenere tutti gli account di fatturazione che l'utente ha accesso e includere i profili di fatturazione nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4c657-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="4c657-118">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="4c657-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="4c657-119">Ottenere tutti gli account di fatturazione che l'utente ha accesso e includere nel risultato i profili di fatturazione e le sezioni della fattura.</span><span class="sxs-lookup"><span data-stu-id="4c657-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="4c657-120">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="4c657-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="4c657-121">Ottenere l'account di fatturazione con il nome specificato e includere nel risultato l'indirizzo, i profili di fatturazione e le sezioni fattura.</span><span class="sxs-lookup"><span data-stu-id="4c657-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="4c657-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c657-122">PARAMETERS</span></span>

### <span data-ttu-id="4c657-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c657-123">-DefaultProfile</span></span>
<span data-ttu-id="4c657-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4c657-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c657-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="4c657-125">-IncludeAddress</span></span>
<span data-ttu-id="4c657-126">Includere l'indirizzo dell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="4c657-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="4c657-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="4c657-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="4c657-128">Includere i profili di fatturazione nell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="4c657-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="4c657-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="4c657-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="4c657-130">Includere i profili di fatturazione in sezioni account di fatturazione e fatture.</span><span class="sxs-lookup"><span data-stu-id="4c657-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="4c657-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c657-131">-Name</span></span>
<span data-ttu-id="4c657-132">Nome di un account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="4c657-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="4c657-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="4c657-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="4c657-134">Elencare le entità di fatturazione in account di fatturazione che possono essere usate come input per creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4c657-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="4c657-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c657-135">CommonParameters</span></span>
<span data-ttu-id="4c657-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c657-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c657-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c657-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c657-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c657-138">INPUTS</span></span>

### <span data-ttu-id="4c657-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4c657-139">None</span></span>

## <span data-ttu-id="4c657-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c657-140">OUTPUTS</span></span>

### <span data-ttu-id="4c657-141">Microsoft. Azure. Commands. Billing. Models. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="4c657-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="4c657-142">Note</span><span class="sxs-lookup"><span data-stu-id="4c657-142">NOTES</span></span>

## <span data-ttu-id="4c657-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c657-143">RELATED LINKS</span></span>
