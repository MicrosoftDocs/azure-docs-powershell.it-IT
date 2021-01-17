---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478140"
---
# <span data-ttu-id="f03ed-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="f03ed-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="f03ed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f03ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f03ed-103">Ottenere le sezioni fattura.</span><span class="sxs-lookup"><span data-stu-id="f03ed-103">Get invoice sections.</span></span>

## <span data-ttu-id="f03ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f03ed-104">SYNTAX</span></span>

### <span data-ttu-id="f03ed-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f03ed-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f03ed-106">Singola</span><span class="sxs-lookup"><span data-stu-id="f03ed-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f03ed-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f03ed-107">DESCRIPTION</span></span>
<span data-ttu-id="f03ed-108">Il cmdlet **Get-AzInvoiceSection** ottiene le sezioni fattura sotto il profilo di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f03ed-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="f03ed-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f03ed-109">EXAMPLES</span></span>

### <span data-ttu-id="f03ed-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f03ed-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="f03ed-111">Ottenere tutte le sezioni della fattura sotto il profilo di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f03ed-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="f03ed-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f03ed-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="f03ed-113">Ottenere la sezione fattura con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="f03ed-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="f03ed-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f03ed-114">PARAMETERS</span></span>

### <span data-ttu-id="f03ed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f03ed-115">-DefaultProfile</span></span>
<span data-ttu-id="f03ed-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f03ed-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f03ed-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="f03ed-117">-BillingAccountName</span></span>
<span data-ttu-id="f03ed-118">Nome dell'account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="f03ed-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="f03ed-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="f03ed-119">-BillingProfileName</span></span>
<span data-ttu-id="f03ed-120">Nome del profilo di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="f03ed-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="f03ed-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="f03ed-121">-Name</span></span>
<span data-ttu-id="f03ed-122">Nome di una specifica sezione fattura.</span><span class="sxs-lookup"><span data-stu-id="f03ed-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="f03ed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f03ed-123">CommonParameters</span></span>
<span data-ttu-id="f03ed-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f03ed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f03ed-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f03ed-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f03ed-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f03ed-126">INPUTS</span></span>

### <span data-ttu-id="f03ed-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f03ed-127">None</span></span>

## <span data-ttu-id="f03ed-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f03ed-128">OUTPUTS</span></span>

### <span data-ttu-id="f03ed-129">Microsoft. Azure. Commands. Billing. Models. PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="f03ed-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="f03ed-130">Note</span><span class="sxs-lookup"><span data-stu-id="f03ed-130">NOTES</span></span>

## <span data-ttu-id="f03ed-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f03ed-131">RELATED LINKS</span></span>
