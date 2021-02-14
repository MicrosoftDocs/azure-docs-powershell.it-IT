---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: ccb686ab0aeb373a542e958aab7b90489fc36f63
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181990"
---
# <span data-ttu-id="a2af2-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="a2af2-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="a2af2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2af2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2af2-103">Ottieni le sezioni della fattura.</span><span class="sxs-lookup"><span data-stu-id="a2af2-103">Get invoice sections.</span></span>

## <span data-ttu-id="a2af2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2af2-104">SYNTAX</span></span>

### <span data-ttu-id="a2af2-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2af2-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a2af2-106">Single</span><span class="sxs-lookup"><span data-stu-id="a2af2-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2af2-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2af2-107">DESCRIPTION</span></span>
<span data-ttu-id="a2af2-108">Il cmdlet **Get-AzInvoiceSection** ottiene le sezioni di fattura nel profilo di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a2af2-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="a2af2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2af2-109">EXAMPLES</span></span>

### <span data-ttu-id="a2af2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2af2-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="a2af2-111">Ottieni tutte le sezioni delle fatture nel profilo di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a2af2-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="a2af2-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a2af2-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="a2af2-113">Recuperare la sezione della fattura con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="a2af2-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="a2af2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2af2-114">PARAMETERS</span></span>

### <span data-ttu-id="a2af2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2af2-115">-DefaultProfile</span></span>
<span data-ttu-id="a2af2-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a2af2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2af2-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="a2af2-117">-BillingAccountName</span></span>
<span data-ttu-id="a2af2-118">Nome dell'account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="a2af2-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="a2af2-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="a2af2-119">-BillingProfileName</span></span>
<span data-ttu-id="a2af2-120">Nome del profilo di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="a2af2-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="a2af2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a2af2-121">-Name</span></span>
<span data-ttu-id="a2af2-122">Nome di una sezione di fattura specifica.</span><span class="sxs-lookup"><span data-stu-id="a2af2-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="a2af2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2af2-123">CommonParameters</span></span>
<span data-ttu-id="a2af2-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2af2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2af2-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2af2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2af2-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2af2-126">INPUTS</span></span>

### <span data-ttu-id="a2af2-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a2af2-127">None</span></span>

## <span data-ttu-id="a2af2-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2af2-128">OUTPUTS</span></span>

### <span data-ttu-id="a2af2-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="a2af2-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="a2af2-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2af2-130">NOTES</span></span>

## <span data-ttu-id="a2af2-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2af2-131">RELATED LINKS</span></span>
