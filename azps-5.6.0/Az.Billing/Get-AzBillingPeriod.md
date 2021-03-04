---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: d2a859740d2e5627eca3ca0748aab8e72c1ee9af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990455"
---
# <span data-ttu-id="4ed0e-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="4ed0e-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="4ed0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed0e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed0e-103">Ottenere periodi di fatturazione per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="4ed0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ed0e-104">SYNTAX</span></span>

### <span data-ttu-id="4ed0e-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ed0e-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ed0e-106">Single</span><span class="sxs-lookup"><span data-stu-id="4ed0e-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed0e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ed0e-107">DESCRIPTION</span></span>
<span data-ttu-id="4ed0e-108">Il **cmdlet Get-AzBillingPeriod** ottiene i periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="4ed0e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ed0e-109">EXAMPLES</span></span>

### <span data-ttu-id="4ed0e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ed0e-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="4ed0e-111">Ottieni tutti i periodi di fatturazione disponibili per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="4ed0e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4ed0e-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="4ed0e-113">Ottenere il periodo di fatturazione dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="4ed0e-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4ed0e-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="4ed0e-115">Ottieni al massimo 2 periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="4ed0e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ed0e-116">PARAMETERS</span></span>

### <span data-ttu-id="4ed0e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed0e-117">-DefaultProfile</span></span>
<span data-ttu-id="4ed0e-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4ed0e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ed0e-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4ed0e-119">-MaxCount</span></span>
<span data-ttu-id="4ed0e-120">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-120">Determine the maximum number of records to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ed0e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4ed0e-121">-Name</span></span>
<span data-ttu-id="4ed0e-122">Nome di un periodo di fatturazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="4ed0e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed0e-123">CommonParameters</span></span>
<span data-ttu-id="4ed0e-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed0e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed0e-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ed0e-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed0e-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ed0e-126">INPUTS</span></span>

### <span data-ttu-id="4ed0e-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4ed0e-127">None</span></span>

## <span data-ttu-id="4ed0e-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ed0e-128">OUTPUTS</span></span>

### <span data-ttu-id="4ed0e-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="4ed0e-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="4ed0e-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ed0e-130">NOTES</span></span>

## <span data-ttu-id="4ed0e-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ed0e-131">RELATED LINKS</span></span>
