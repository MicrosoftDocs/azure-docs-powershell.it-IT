---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmBillingInvoice.md
ms.openlocfilehash: 5a6ccf36f8e7aecdca4d6560614e9185a5ca26b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510092"
---
# <span data-ttu-id="63fc1-101">Get-AzureRmBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="63fc1-101">Get-AzureRmBillingInvoice</span></span>

## <span data-ttu-id="63fc1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="63fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="63fc1-103">Ottenere fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="63fc1-103">Get billing invoices of the subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63fc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="63fc1-104">SYNTAX</span></span>

### <span data-ttu-id="63fc1-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="63fc1-105">List (Default)</span></span>
```
Get-AzureRmBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63fc1-106">Più recente</span><span class="sxs-lookup"><span data-stu-id="63fc1-106">Latest</span></span>
```
Get-AzureRmBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63fc1-107">Singola</span><span class="sxs-lookup"><span data-stu-id="63fc1-107">Single</span></span>
```
Get-AzureRmBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63fc1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="63fc1-108">DESCRIPTION</span></span>
<span data-ttu-id="63fc1-109">Il cmdlet **Get-AzureRmBillingInvoice** ottiene le fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="63fc1-109">The **Get-AzureRmBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="63fc1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="63fc1-110">EXAMPLES</span></span>

### <span data-ttu-id="63fc1-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="63fc1-111">Example 1</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Latest
```

<span data-ttu-id="63fc1-112">Ottenere la fattura più recente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="63fc1-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="63fc1-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="63fc1-113">Example 2</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="63fc1-114">Ottenere la fattura dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="63fc1-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="63fc1-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="63fc1-115">Example 3</span></span>
```
PS C:\> Get-AzureRmBillingInvoice
```

<span data-ttu-id="63fc1-116">Ottenere tutte le fatture disponibili dell'abbonamento in ordine cronologico inverso a partire dalla fattura più recente senza download URL.</span><span class="sxs-lookup"><span data-stu-id="63fc1-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="63fc1-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="63fc1-117">Example 4</span></span>
```
PS C:\> Get-AzureRmBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="63fc1-118">Ottenere le ultime 10 fatture dell'abbonamento e includere l'URL di download nel risultato.</span><span class="sxs-lookup"><span data-stu-id="63fc1-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="63fc1-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="63fc1-119">PARAMETERS</span></span>

### <span data-ttu-id="63fc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63fc1-120">-DefaultProfile</span></span>
<span data-ttu-id="63fc1-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="63fc1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fc1-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="63fc1-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="63fc1-123">Genera l'URL di download delle fatture.</span><span class="sxs-lookup"><span data-stu-id="63fc1-123">Generate the download url of the invoices.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fc1-124">-Ultimi</span><span class="sxs-lookup"><span data-stu-id="63fc1-124">-Latest</span></span>
<span data-ttu-id="63fc1-125">Ottenere la fattura più recente.</span><span class="sxs-lookup"><span data-stu-id="63fc1-125">Get the latest invoice.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Latest
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fc1-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="63fc1-126">-MaxCount</span></span>
<span data-ttu-id="63fc1-127">Determina il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="63fc1-127">Determines the maximum number of records to return.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fc1-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="63fc1-128">-Name</span></span>
<span data-ttu-id="63fc1-129">Nome di una fattura specifica da ottenere o la più recente se non specificata.</span><span class="sxs-lookup"><span data-stu-id="63fc1-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="63fc1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fc1-130">CommonParameters</span></span>
<span data-ttu-id="63fc1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63fc1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fc1-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fc1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fc1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="63fc1-133">INPUTS</span></span>

### <span data-ttu-id="63fc1-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="63fc1-134">None</span></span>

## <span data-ttu-id="63fc1-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="63fc1-135">OUTPUTS</span></span>

### <span data-ttu-id="63fc1-136">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. Billing. Models. fattura, Microsoft. Azure. Commands. Billing, Version = 0.14.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="63fc1-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Billing.Models.Invoice, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="63fc1-137">Microsoft. Azure. Management. Billing. Models. fattura</span><span class="sxs-lookup"><span data-stu-id="63fc1-137">Microsoft.Azure.Management.Billing.Models.Invoice</span></span>

## <span data-ttu-id="63fc1-138">Note</span><span class="sxs-lookup"><span data-stu-id="63fc1-138">NOTES</span></span>

## <span data-ttu-id="63fc1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="63fc1-139">RELATED LINKS</span></span>

