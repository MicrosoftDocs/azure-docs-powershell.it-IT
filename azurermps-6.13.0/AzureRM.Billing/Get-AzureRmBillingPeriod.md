---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillingperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: 66c9a0bb9ba4aa2f17c48ffb737f1c8d72034f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519760"
---
# <span data-ttu-id="d71d5-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="d71d5-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="d71d5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d71d5-102">SYNOPSIS</span></span>
<span data-ttu-id="d71d5-103">Ottenere i periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d71d5-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d71d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d71d5-104">SYNTAX</span></span>

### <span data-ttu-id="d71d5-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d71d5-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d71d5-106">Singola</span><span class="sxs-lookup"><span data-stu-id="d71d5-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d71d5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d71d5-107">DESCRIPTION</span></span>
<span data-ttu-id="d71d5-108">Il cmdlet **Get-AzureRmBillingPeriod** ottiene i periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d71d5-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="d71d5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d71d5-109">EXAMPLES</span></span>

### <span data-ttu-id="d71d5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d71d5-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="d71d5-111">Ottenere tutti i periodi di fatturazione disponibili per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d71d5-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="d71d5-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d71d5-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="d71d5-113">Ottenere il periodo di fatturazione dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="d71d5-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="d71d5-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d71d5-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="d71d5-115">Ottenere al massimo 2 periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d71d5-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="d71d5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d71d5-116">PARAMETERS</span></span>

### <span data-ttu-id="d71d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d71d5-117">-DefaultProfile</span></span>
<span data-ttu-id="d71d5-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d71d5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d71d5-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="d71d5-119">-MaxCount</span></span>
<span data-ttu-id="d71d5-120">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="d71d5-120">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="d71d5-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d71d5-121">-Name</span></span>
<span data-ttu-id="d71d5-122">Nome di un periodo di fatturazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="d71d5-122">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="d71d5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d71d5-123">CommonParameters</span></span>
<span data-ttu-id="d71d5-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d71d5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d71d5-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d71d5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d71d5-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d71d5-126">INPUTS</span></span>

### <span data-ttu-id="d71d5-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d71d5-127">None</span></span>

## <span data-ttu-id="d71d5-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d71d5-128">OUTPUTS</span></span>

### <span data-ttu-id="d71d5-129">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="d71d5-129">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="d71d5-130">Note</span><span class="sxs-lookup"><span data-stu-id="d71d5-130">NOTES</span></span>

## <span data-ttu-id="d71d5-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d71d5-131">RELATED LINKS</span></span>
