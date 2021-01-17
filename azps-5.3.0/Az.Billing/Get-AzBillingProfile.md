---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingProfile.md
ms.openlocfilehash: ec9ac0249715dc7c6d9966158b95261d0410c995
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478148"
---
# <span data-ttu-id="45d4b-101">Get-AzBillingProfile</span><span class="sxs-lookup"><span data-stu-id="45d4b-101">Get-AzBillingProfile</span></span>

## <span data-ttu-id="45d4b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="45d4b-103">Ottenere i profili di fatturazione.</span><span class="sxs-lookup"><span data-stu-id="45d4b-103">Get billing profiles.</span></span>

## <span data-ttu-id="45d4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45d4b-104">SYNTAX</span></span>

### <span data-ttu-id="45d4b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45d4b-105">List (Default)</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45d4b-106">Singola</span><span class="sxs-lookup"><span data-stu-id="45d4b-106">Single</span></span>
```
Get-AzBillingProfile -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]> [-ExpandInvoiceSection]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45d4b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45d4b-107">DESCRIPTION</span></span>
<span data-ttu-id="45d4b-108">Il cmdlet **Get-AzBillingProfile** ottiene i profili di fatturazione sotto l'account di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="45d4b-108">The **Get-AzBillingProfile** cmdlet gets billing profiles under the specified billing account.</span></span> 

## <span data-ttu-id="45d4b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45d4b-109">EXAMPLES</span></span>

### <span data-ttu-id="45d4b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45d4b-110">Example 1</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="45d4b-111">Ottenere tutti i profili di fatturazione nell'account di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="45d4b-111">Get all billing profiles under the specified billing account.</span></span>

### <span data-ttu-id="45d4b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="45d4b-112">Example 2</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -Name AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="45d4b-113">Ottenere il profilo di fatturazione con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="45d4b-113">Get the billing profile with the specified name.</span></span>

### <span data-ttu-id="45d4b-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="45d4b-114">Example 3</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection
```

<span data-ttu-id="45d4b-115">Ottenere tutti i profili di fatturazione in un account di fatturazione specificato e includere le sezioni della fattura nel risultato.</span><span class="sxs-lookup"><span data-stu-id="45d4b-115">Get all billing profiles under specified billing account, and include the invoice sections in the result.</span></span>

### <span data-ttu-id="45d4b-116">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="45d4b-116">Example 4</span></span>
```
PS C:\> Get-AzBillingProfile -BillingAccountName 00000000-0000-0000-0000-000000000000 -ExpandInvoiceSection -Name <System.Collections.Generic.List`1[System.String]>
```

<span data-ttu-id="45d4b-117">Ottenere il profilo di fatturazione con il nome specificato e includere le sezioni della fattura nel risultato.</span><span class="sxs-lookup"><span data-stu-id="45d4b-117">Get the billing profile with the specified name, and include the invoice sections in the result.</span></span>

## <span data-ttu-id="45d4b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45d4b-118">PARAMETERS</span></span>

### <span data-ttu-id="45d4b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d4b-119">-DefaultProfile</span></span>
<span data-ttu-id="45d4b-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="45d4b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45d4b-121">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="45d4b-121">-BillingAccountName</span></span>
<span data-ttu-id="45d4b-122">Nome dell'account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="45d4b-122">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="45d4b-123">-ExpandInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="45d4b-123">-ExpandInvoiceSection</span></span>
<span data-ttu-id="45d4b-124">Includere le sezioni fatture in profilo fatturazione.</span><span class="sxs-lookup"><span data-stu-id="45d4b-124">Include the invoices sections under billing profile.</span></span>

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

### <span data-ttu-id="45d4b-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="45d4b-125">-Name</span></span>
<span data-ttu-id="45d4b-126">Nome di un profilo di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="45d4b-126">Name of a specific billing profile.</span></span>

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

### <span data-ttu-id="45d4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d4b-127">CommonParameters</span></span>
<span data-ttu-id="45d4b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d4b-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d4b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d4b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45d4b-130">INPUTS</span></span>

### <span data-ttu-id="45d4b-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="45d4b-131">None</span></span>

## <span data-ttu-id="45d4b-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45d4b-132">OUTPUTS</span></span>

### <span data-ttu-id="45d4b-133">Microsoft. Azure. Commands. Billing. Models. PSBillingProfile</span><span class="sxs-lookup"><span data-stu-id="45d4b-133">Microsoft.Azure.Commands.Billing.Models.PSBillingProfile</span></span>

## <span data-ttu-id="45d4b-134">Note</span><span class="sxs-lookup"><span data-stu-id="45d4b-134">NOTES</span></span>

## <span data-ttu-id="45d4b-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45d4b-135">RELATED LINKS</span></span>
