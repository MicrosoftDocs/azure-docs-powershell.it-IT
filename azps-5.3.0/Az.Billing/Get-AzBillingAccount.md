---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingAccount.md
ms.openlocfilehash: 21914793295f8ff000d02355fead1df718fcf052
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488775"
---
# <span data-ttu-id="db26b-101">Get-AzBillingAccount</span><span class="sxs-lookup"><span data-stu-id="db26b-101">Get-AzBillingAccount</span></span>

## <span data-ttu-id="db26b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db26b-102">SYNOPSIS</span></span>
<span data-ttu-id="db26b-103">Ottenere gli account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="db26b-103">Get billing accounts.</span></span>

## <span data-ttu-id="db26b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db26b-104">SYNTAX</span></span>

### <span data-ttu-id="db26b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db26b-105">List (Default)</span></span>
```
Get-AzBillingAccount [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="db26b-106">Singola</span><span class="sxs-lookup"><span data-stu-id="db26b-106">Single</span></span>
```
Get-AzBillingAccount -Name <System.Collections.Generic.List`1[System.String]> [-IncludeAddress] [-ExpandBillingProfile] [-ExpandInvoiceSection] [-ListEntitiesToCreateSubscription]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db26b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db26b-107">DESCRIPTION</span></span>
<span data-ttu-id="db26b-108">Il cmdlet **Get-AzBillingAccount** ottiene gli account di fatturazione, a cui l'utente ha accesso.</span><span class="sxs-lookup"><span data-stu-id="db26b-108">The **Get-AzBillingAccount** cmdlet gets billing accounts, user has access to.</span></span> 

## <span data-ttu-id="db26b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db26b-109">EXAMPLES</span></span>

### <span data-ttu-id="db26b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db26b-110">Example 1</span></span>
```
PS C:\> Get-AzBillingAccount
```

<span data-ttu-id="db26b-111">Ottenere l'accesso a tutti gli account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="db26b-111">Get all billing accounts user has access to.</span></span>

### <span data-ttu-id="db26b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="db26b-112">Example 2</span></span>
```
PS C:\> Get-AzBillingAccount -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="db26b-113">Ottenere l'account di fatturazione con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="db26b-113">Get the billing account with the specified name.</span></span>

### <span data-ttu-id="db26b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="db26b-114">Example 3</span></span>
```
PS C:\> Get-AzBillingAccount -IncludeAddress
```

<span data-ttu-id="db26b-115">Ottenere tutti gli account di fatturazione che l'utente ha accesso e includere l'indirizzo nel risultato.</span><span class="sxs-lookup"><span data-stu-id="db26b-115">Get all billing accounts user has access to, and include the address in the result.</span></span>

### <span data-ttu-id="db26b-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="db26b-116">Example 4</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandBillingProfile
```

<span data-ttu-id="db26b-117">Ottenere tutti gli account di fatturazione che l'utente ha accesso e includere i profili di fatturazione nel risultato.</span><span class="sxs-lookup"><span data-stu-id="db26b-117">Get all billing accounts user has access to, and include the billing profiles in the result.</span></span>

### <span data-ttu-id="db26b-118">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="db26b-118">Example 5</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection
```

<span data-ttu-id="db26b-119">Ottenere tutti gli account di fatturazione che l'utente ha accesso e includere nel risultato i profili di fatturazione e le sezioni della fattura.</span><span class="sxs-lookup"><span data-stu-id="db26b-119">Get all billing accounts user has access to, and include the billing profiles and invoice sections under them in the result.</span></span>

### <span data-ttu-id="db26b-120">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="db26b-120">Example 6</span></span>
```
PS C:\> Get-AzBillingAccount -ExpandInvoiceSection -ExpandAddress -Name 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="db26b-121">Ottenere l'account di fatturazione con il nome specificato e includere nel risultato l'indirizzo, i profili di fatturazione e le sezioni fattura.</span><span class="sxs-lookup"><span data-stu-id="db26b-121">Get the billing account with the specified name, and include the address, billing profiles and invoice sections under them in the result.</span></span>

## <span data-ttu-id="db26b-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db26b-122">PARAMETERS</span></span>

### <span data-ttu-id="db26b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db26b-123">-DefaultProfile</span></span>
<span data-ttu-id="db26b-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="db26b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db26b-125">-IncludeAddress</span><span class="sxs-lookup"><span data-stu-id="db26b-125">-IncludeAddress</span></span>
<span data-ttu-id="db26b-126">Includere l'indirizzo dell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="db26b-126">Include the address of the billing account.</span></span>

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

### <span data-ttu-id="db26b-127">-ExpandBillingProfile</span><span class="sxs-lookup"><span data-stu-id="db26b-127">-ExpandBillingProfile</span></span>
<span data-ttu-id="db26b-128">Includere i profili di fatturazione nell'account di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="db26b-128">Include the billing profiles under the billing account.</span></span>

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

### <span data-ttu-id="db26b-129">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="db26b-129">-ExpandInvoiceSection</span></span>
<span data-ttu-id="db26b-130">Includere i profili di fatturazione in sezioni account di fatturazione e fatture.</span><span class="sxs-lookup"><span data-stu-id="db26b-130">Include the billing profiles under billing account and invoices sections under them.</span></span>

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

### <span data-ttu-id="db26b-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="db26b-131">-Name</span></span>
<span data-ttu-id="db26b-132">Nome di un account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="db26b-132">Name of a specific billing account.</span></span>

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

### <span data-ttu-id="db26b-133">-ListEntitiesToCreateSubscription</span><span class="sxs-lookup"><span data-stu-id="db26b-133">-ListEntitiesToCreateSubscription</span></span>
<span data-ttu-id="db26b-134">Elencare le entità di fatturazione in account di fatturazione che possono essere usate come input per creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="db26b-134">List the billing entities under billing account which can be used as input to create subscription.</span></span>

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

### <span data-ttu-id="db26b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db26b-135">CommonParameters</span></span>
<span data-ttu-id="db26b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db26b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db26b-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db26b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db26b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db26b-138">INPUTS</span></span>

### <span data-ttu-id="db26b-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="db26b-139">None</span></span>

## <span data-ttu-id="db26b-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db26b-140">OUTPUTS</span></span>

### <span data-ttu-id="db26b-141">Microsoft. Azure. Commands. Billing. Models. PSBillingAccount</span><span class="sxs-lookup"><span data-stu-id="db26b-141">Microsoft.Azure.Commands.Billing.Models.PSBillingAccount</span></span>

## <span data-ttu-id="db26b-142">Note</span><span class="sxs-lookup"><span data-stu-id="db26b-142">NOTES</span></span>

## <span data-ttu-id="db26b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db26b-143">RELATED LINKS</span></span>
