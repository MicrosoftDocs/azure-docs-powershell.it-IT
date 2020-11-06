---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 38b1c4e29ed82ac3bddcff9565a216bd6db23411
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519209"
---
# <span data-ttu-id="556e4-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="556e4-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="556e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="556e4-102">SYNOPSIS</span></span>
<span data-ttu-id="556e4-103">Ottenere fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="556e4-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="556e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="556e4-104">SYNTAX</span></span>

### <span data-ttu-id="556e4-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="556e4-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="556e4-106">Più recente</span><span class="sxs-lookup"><span data-stu-id="556e4-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="556e4-107">Singola</span><span class="sxs-lookup"><span data-stu-id="556e4-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="556e4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="556e4-108">DESCRIPTION</span></span>
<span data-ttu-id="556e4-109">Il cmdlet **Get-AzureRmBillingInvoice** ottiene le fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="556e4-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="556e4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="556e4-110">EXAMPLES</span></span>

### <span data-ttu-id="556e4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="556e4-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="556e4-112">Ottenere la fattura più recente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="556e4-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="556e4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="556e4-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="556e4-114">Ottenere la fattura dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="556e4-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="556e4-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="556e4-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="556e4-116">Ottenere tutte le fatture disponibili dell'abbonamento in ordine cronologico inverso a partire dalla fattura più recente senza download URL.</span><span class="sxs-lookup"><span data-stu-id="556e4-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="556e4-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="556e4-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="556e4-118">Ottenere le ultime 10 fatture dell'abbonamento e includere l'URL di download nel risultato.</span><span class="sxs-lookup"><span data-stu-id="556e4-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="556e4-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="556e4-119">PARAMETERS</span></span>

### <span data-ttu-id="556e4-120">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="556e4-120">-GenerateDownloadUrl</span></span>
<span data-ttu-id="556e4-121">Genera l'URL di download delle fatture.</span><span class="sxs-lookup"><span data-stu-id="556e4-121">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556e4-122">-Ultimi</span><span class="sxs-lookup"><span data-stu-id="556e4-122">-Latest</span></span>
<span data-ttu-id="556e4-123">Ottenere la fattura più recente.</span><span class="sxs-lookup"><span data-stu-id="556e4-123">Get the latest invoice.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="556e4-124">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="556e4-124">-MaxCount</span></span>
<span data-ttu-id="556e4-125">Determina il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="556e4-125">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="556e4-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="556e4-126">-Name</span></span>
<span data-ttu-id="556e4-127">Nome di una fattura specifica da ottenere o la più recente se non specificata.</span><span class="sxs-lookup"><span data-stu-id="556e4-127">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="556e4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556e4-128">-DefaultProfile</span></span>
<span data-ttu-id="556e4-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="556e4-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="556e4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556e4-130">CommonParameters</span></span>
<span data-ttu-id="556e4-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="556e4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556e4-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="556e4-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556e4-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="556e4-133">INPUTS</span></span>

### <span data-ttu-id="556e4-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="556e4-134">None</span></span>

## <span data-ttu-id="556e4-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="556e4-135">OUTPUTS</span></span>

### <span data-ttu-id="556e4-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Billing. Models. fattura, Microsoft. Azure. Commands. Billing, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="556e4-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="556e4-137">Microsoft. Azure. Management. Billing. Models. fattura</span><span class="sxs-lookup"><span data-stu-id="556e4-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="556e4-138">Note</span><span class="sxs-lookup"><span data-stu-id="556e4-138">NOTES</span></span>

## <span data-ttu-id="556e4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="556e4-139">RELATED LINKS</span></span>

