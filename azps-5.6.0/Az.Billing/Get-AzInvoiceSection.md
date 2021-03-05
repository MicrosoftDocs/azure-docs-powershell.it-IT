---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azinvoicesection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzInvoiceSection.md
ms.openlocfilehash: 6bf0b5a25772d430695737d70ff68cae5c5aa0d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013997"
---
# <span data-ttu-id="2ac62-101">Get-AzInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="2ac62-101">Get-AzInvoiceSection</span></span>

## <span data-ttu-id="2ac62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac62-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac62-103">Ottieni le sezioni della fattura.</span><span class="sxs-lookup"><span data-stu-id="2ac62-103">Get invoice sections.</span></span>

## <span data-ttu-id="2ac62-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ac62-104">SYNTAX</span></span>

### <span data-ttu-id="2ac62-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ac62-105">List (Default)</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ac62-106">Single</span><span class="sxs-lookup"><span data-stu-id="2ac62-106">Single</span></span>
```
Get-AzInvoiceSection -BillingAccountName <String> -BillingProfileName <String> -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac62-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2ac62-107">DESCRIPTION</span></span>
<span data-ttu-id="2ac62-108">Il cmdlet **Get-AzInvoiceSection** ottiene le sezioni di fattura nel profilo di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="2ac62-108">The **Get-AzInvoiceSection** cmdlet gets invoice sections under the specified billing profile.</span></span> 

## <span data-ttu-id="2ac62-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ac62-109">EXAMPLES</span></span>

### <span data-ttu-id="2ac62-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ac62-110">Example 1</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ
```

<span data-ttu-id="2ac62-111">Ottieni tutte le sezioni delle fatture nel profilo di fatturazione specificato.</span><span class="sxs-lookup"><span data-stu-id="2ac62-111">Get all invoice sections under the specified billing profile.</span></span>

### <span data-ttu-id="2ac62-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2ac62-112">Example 2</span></span>
```
PS C:\> Get-AzInvoiceSection -BillingAccountName 00000000-0000-0000-0000-000000000000 -BillingProfileName AAAA-0A00-AAA-ZZZ -Name BBBB-0A00-BBB-ZZZ
```

<span data-ttu-id="2ac62-113">Recuperare la sezione della fattura con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="2ac62-113">Get the invoice section with the specified name.</span></span>

## <span data-ttu-id="2ac62-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ac62-114">PARAMETERS</span></span>

### <span data-ttu-id="2ac62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac62-115">-DefaultProfile</span></span>
<span data-ttu-id="2ac62-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2ac62-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ac62-117">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="2ac62-117">-BillingAccountName</span></span>
<span data-ttu-id="2ac62-118">Nome dell'account di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="2ac62-118">Name of the specific billing account.</span></span>

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

### <span data-ttu-id="2ac62-119">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="2ac62-119">-BillingProfileName</span></span>
<span data-ttu-id="2ac62-120">Nome del profilo di fatturazione specifico.</span><span class="sxs-lookup"><span data-stu-id="2ac62-120">Name of the specific billing profile.</span></span>

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

### <span data-ttu-id="2ac62-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2ac62-121">-Name</span></span>
<span data-ttu-id="2ac62-122">Nome di una sezione specifica della fattura.</span><span class="sxs-lookup"><span data-stu-id="2ac62-122">Name of a specific invoice section.</span></span>

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

### <span data-ttu-id="2ac62-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac62-123">CommonParameters</span></span>
<span data-ttu-id="2ac62-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac62-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac62-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac62-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac62-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="2ac62-126">INPUTS</span></span>

### <span data-ttu-id="2ac62-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="2ac62-127">None</span></span>

## <span data-ttu-id="2ac62-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ac62-128">OUTPUTS</span></span>

### <span data-ttu-id="2ac62-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span><span class="sxs-lookup"><span data-stu-id="2ac62-129">Microsoft.Azure.Commands.Billing.Models.PSInvoiceSection</span></span>

## <span data-ttu-id="2ac62-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="2ac62-130">NOTES</span></span>

## <span data-ttu-id="2ac62-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ac62-131">RELATED LINKS</span></span>
