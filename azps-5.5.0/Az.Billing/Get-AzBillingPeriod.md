---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingPeriod.md
ms.openlocfilehash: 6a7f7d47976608b521e69e7aaf926a9600b35382
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199502"
---
# <span data-ttu-id="97175-101">Get-AzBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="97175-101">Get-AzBillingPeriod</span></span>

## <span data-ttu-id="97175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97175-102">SYNOPSIS</span></span>
<span data-ttu-id="97175-103">Ottenere periodi di fatturazione per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97175-103">Get billing periods of the subscription.</span></span>

## <span data-ttu-id="97175-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97175-104">SYNTAX</span></span>

### <span data-ttu-id="97175-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97175-105">List (Default)</span></span>
```
Get-AzBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97175-106">Single</span><span class="sxs-lookup"><span data-stu-id="97175-106">Single</span></span>
```
Get-AzBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97175-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97175-107">DESCRIPTION</span></span>
<span data-ttu-id="97175-108">Il **cmdlet Get-AzBillingPeriod** ottiene i periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97175-108">The **Get-AzBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="97175-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97175-109">EXAMPLES</span></span>

### <span data-ttu-id="97175-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97175-110">Example 1</span></span>
```
PS C:\> Get-AzBillingPeriod
```

<span data-ttu-id="97175-111">Ottieni tutti i periodi di fatturazione disponibili per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97175-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="97175-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="97175-112">Example 2</span></span>
```
PS C:\> Get-AzBillingPeriod -Name 201704-1
```

<span data-ttu-id="97175-113">Ottenere il periodo di fatturazione dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="97175-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="97175-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="97175-114">Example 3</span></span>
```
PS C:\> Get-AzBillingPeriod -MaxCount 2
```

<span data-ttu-id="97175-115">Ottieni al massimo 2 periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="97175-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="97175-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97175-116">PARAMETERS</span></span>

### <span data-ttu-id="97175-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97175-117">-DefaultProfile</span></span>
<span data-ttu-id="97175-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="97175-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97175-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="97175-119">-MaxCount</span></span>
<span data-ttu-id="97175-120">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="97175-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="97175-121">-Name</span><span class="sxs-lookup"><span data-stu-id="97175-121">-Name</span></span>
<span data-ttu-id="97175-122">Nome di un periodo di fatturazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="97175-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="97175-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97175-123">CommonParameters</span></span>
<span data-ttu-id="97175-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97175-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97175-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97175-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97175-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="97175-126">INPUTS</span></span>

### <span data-ttu-id="97175-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="97175-127">None</span></span>

## <span data-ttu-id="97175-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97175-128">OUTPUTS</span></span>

### <span data-ttu-id="97175-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="97175-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="97175-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="97175-130">NOTES</span></span>

## <span data-ttu-id="97175-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97175-131">RELATED LINKS</span></span>
