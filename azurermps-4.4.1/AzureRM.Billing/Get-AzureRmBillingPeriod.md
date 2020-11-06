---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingPeriod.md
ms.openlocfilehash: f6b75a1c161515ee45571ba3db6d2f84b95af967
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511307"
---
# <span data-ttu-id="50b57-101">Get-AzureRmBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="50b57-101">Get-AzureRmBillingPeriod</span></span>

## <span data-ttu-id="50b57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50b57-102">SYNOPSIS</span></span>
<span data-ttu-id="50b57-103">Ottenere i periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="50b57-103">Get billing periods of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50b57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50b57-104">SYNTAX</span></span>

### <span data-ttu-id="50b57-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50b57-105">List (Default)</span></span>
```
Get-AzureRmBillingPeriod [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50b57-106">Singola</span><span class="sxs-lookup"><span data-stu-id="50b57-106">Single</span></span>
```
Get-AzureRmBillingPeriod -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50b57-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50b57-107">DESCRIPTION</span></span>
<span data-ttu-id="50b57-108">Il cmdlet **Get-AzureRmBillingPeriod** ottiene i periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="50b57-108">The **Get-AzureRmBillingPeriod** cmdlet gets billing periods of the subscription.</span></span>

## <span data-ttu-id="50b57-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50b57-109">EXAMPLES</span></span>

### <span data-ttu-id="50b57-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50b57-110">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingPeriod
```

<span data-ttu-id="50b57-111">Ottenere tutti i periodi di fatturazione disponibili per l'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="50b57-111">Get all available billing periods of the subscription.</span></span>

### <span data-ttu-id="50b57-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="50b57-112">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -Name 201704-1
```

<span data-ttu-id="50b57-113">Ottenere il periodo di fatturazione dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="50b57-113">Get the billing period of the subscription with the specified name.</span></span>

### <span data-ttu-id="50b57-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="50b57-114">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingPeriod -MaxCount 2
```

<span data-ttu-id="50b57-115">Ottenere al massimo 2 periodi di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="50b57-115">Get at most 2 billing periods of the subscription.</span></span>

## <span data-ttu-id="50b57-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50b57-116">PARAMETERS</span></span>

### <span data-ttu-id="50b57-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="50b57-117">-MaxCount</span></span>
<span data-ttu-id="50b57-118">Determinare il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="50b57-118">Determine the maximum number of records to return.</span></span>

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

### <span data-ttu-id="50b57-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="50b57-119">-Name</span></span>
<span data-ttu-id="50b57-120">Nome di un periodo di fatturazione specifico da ottenere.</span><span class="sxs-lookup"><span data-stu-id="50b57-120">Name of a specific billing period to get.</span></span>

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

### <span data-ttu-id="50b57-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50b57-121">-DefaultProfile</span></span>
<span data-ttu-id="50b57-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50b57-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50b57-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50b57-123">CommonParameters</span></span>
<span data-ttu-id="50b57-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50b57-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50b57-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50b57-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50b57-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50b57-126">INPUTS</span></span>

### <span data-ttu-id="50b57-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50b57-127">None</span></span>

## <span data-ttu-id="50b57-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50b57-128">OUTPUTS</span></span>

### <span data-ttu-id="50b57-129">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod, Microsoft. Azure. Commands. Billing, Version = 0.12.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="50b57-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod, Microsoft.Azure.Commands.Billing, Version=0.12.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="50b57-130">Microsoft. Azure. Commands. Billing. Models. PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="50b57-130">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="50b57-131">Note</span><span class="sxs-lookup"><span data-stu-id="50b57-131">NOTES</span></span>

## <span data-ttu-id="50b57-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50b57-132">RELATED LINKS</span></span>

