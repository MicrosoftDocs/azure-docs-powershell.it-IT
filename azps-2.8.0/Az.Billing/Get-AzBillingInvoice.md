---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 8c5e107de50d5e1df1f0c9da7305dbe801857410
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675634"
---
# <span data-ttu-id="8853f-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="8853f-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="8853f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8853f-102">SYNOPSIS</span></span>
<span data-ttu-id="8853f-103">Ottenere fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8853f-103">Get billing invoices of the subscription.</span></span>

## <span data-ttu-id="8853f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8853f-104">SYNTAX</span></span>

### <span data-ttu-id="8853f-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8853f-105">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8853f-106">Più recente</span><span class="sxs-lookup"><span data-stu-id="8853f-106">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8853f-107">Singola</span><span class="sxs-lookup"><span data-stu-id="8853f-107">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8853f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8853f-108">DESCRIPTION</span></span>
<span data-ttu-id="8853f-109">Il cmdlet **Get-AzBillingInvoice** ottiene le fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8853f-109">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="8853f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8853f-110">EXAMPLES</span></span>

### <span data-ttu-id="8853f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8853f-111">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="8853f-112">Ottenere la fattura più recente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8853f-112">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="8853f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8853f-113">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="8853f-114">Ottenere la fattura dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="8853f-114">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="8853f-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8853f-115">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="8853f-116">Ottenere tutte le fatture disponibili dell'abbonamento in ordine cronologico inverso a partire dalla fattura più recente senza download URL.</span><span class="sxs-lookup"><span data-stu-id="8853f-116">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="8853f-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="8853f-117">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="8853f-118">Ottenere le ultime 10 fatture dell'abbonamento e includere l'URL di download nel risultato.</span><span class="sxs-lookup"><span data-stu-id="8853f-118">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

## <span data-ttu-id="8853f-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8853f-119">PARAMETERS</span></span>

### <span data-ttu-id="8853f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8853f-120">-DefaultProfile</span></span>
<span data-ttu-id="8853f-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8853f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8853f-122">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="8853f-122">-GenerateDownloadUrl</span></span>
<span data-ttu-id="8853f-123">Genera l'URL di download delle fatture.</span><span class="sxs-lookup"><span data-stu-id="8853f-123">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="8853f-124">-Ultimi</span><span class="sxs-lookup"><span data-stu-id="8853f-124">-Latest</span></span>
<span data-ttu-id="8853f-125">Ottenere la fattura più recente.</span><span class="sxs-lookup"><span data-stu-id="8853f-125">Get the latest invoice.</span></span>

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

### <span data-ttu-id="8853f-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="8853f-126">-MaxCount</span></span>
<span data-ttu-id="8853f-127">Determina il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="8853f-127">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="8853f-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="8853f-128">-Name</span></span>
<span data-ttu-id="8853f-129">Nome di una fattura specifica da ottenere o la più recente se non specificata.</span><span class="sxs-lookup"><span data-stu-id="8853f-129">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="8853f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8853f-130">CommonParameters</span></span>
<span data-ttu-id="8853f-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8853f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8853f-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8853f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8853f-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8853f-133">INPUTS</span></span>

### <span data-ttu-id="8853f-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8853f-134">None</span></span>

## <span data-ttu-id="8853f-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8853f-135">OUTPUTS</span></span>

### <span data-ttu-id="8853f-136">Microsoft. Azure. Commands. Billing. Models. PSInvoice</span><span class="sxs-lookup"><span data-stu-id="8853f-136">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="8853f-137">Note</span><span class="sxs-lookup"><span data-stu-id="8853f-137">NOTES</span></span>

## <span data-ttu-id="8853f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8853f-138">RELATED LINKS</span></span>
