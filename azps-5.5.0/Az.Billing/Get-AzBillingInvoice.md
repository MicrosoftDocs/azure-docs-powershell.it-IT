---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: ca1e2032b312a7d0805811fb638c95777ba8ae75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199511"
---
# <span data-ttu-id="4a835-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="4a835-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="4a835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a835-102">SYNOPSIS</span></span>
<span data-ttu-id="4a835-103">Ottenere le fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4a835-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="4a835-104">Ottenere le fatture di un account di fatturazione e di un profilo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="4a835-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="4a835-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a835-105">SYNTAX</span></span>

### <span data-ttu-id="4a835-106">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a835-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="4a835-107">Più recenti</span><span class="sxs-lookup"><span data-stu-id="4a835-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="4a835-108">Single</span><span class="sxs-lookup"><span data-stu-id="4a835-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a835-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4a835-109">DESCRIPTION</span></span>
<span data-ttu-id="4a835-110">Il **cmdlet Get-AzBillingInvoice** riceve le fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4a835-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="4a835-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a835-111">EXAMPLES</span></span>

### <span data-ttu-id="4a835-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a835-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="4a835-113">Ottenere la fattura più recente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4a835-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="4a835-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4a835-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="4a835-115">Ottenere la fattura dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="4a835-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="4a835-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4a835-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="4a835-117">Ottenere tutte le fatture disponibili dell'abbonamento in ordine cronologico inverso a partire dalla fattura più recente senza scaricare l'URL.</span><span class="sxs-lookup"><span data-stu-id="4a835-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="4a835-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="4a835-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="4a835-119">Ottieni le 10 fatture più recenti dell'abbonamento e includi l'URL di download nei risultati.</span><span class="sxs-lookup"><span data-stu-id="4a835-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="4a835-120">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="4a835-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="4a835-121">Ottenere la fattura specifica per nome e includere l'URL di download nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4a835-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="4a835-122">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="4a835-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="4a835-123">Ottenere le fatture in base al nome dell'account di fatturazione e includere l'URL di download per ogni fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="4a835-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="4a835-124">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="4a835-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="4a835-125">Ottenere una fattura specifica in base al nome della fattura e al nome dell'account di fatturazione e includere l'URL di download per ogni fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="4a835-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="4a835-126">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="4a835-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="4a835-127">Ottieni l'ultima fattura in base al nome dell'account di fatturazione e includi l'URL di download per la fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="4a835-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="4a835-128">Esempio 9</span><span class="sxs-lookup"><span data-stu-id="4a835-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="4a835-129">Ottieni le 10 fatture più recenti dell'account di fatturazione specifico e del profilo di fatturazione specifico e includi l'URL di download nel risultato.</span><span class="sxs-lookup"><span data-stu-id="4a835-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="4a835-130">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="4a835-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="4a835-131">Ottieni l'ultima fattura in base al nome dell'account di fatturazione e al nome del profilo di fatturazione e includi l'URL di download per la fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="4a835-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="4a835-132">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="4a835-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="4a835-133">Ottenere le fatture in base al nome dell'account di fatturazione e al nome del profilo di fatturazione per un periodo di fatturazione specificato in base alla data di inizio e alla data di fine del periodo.</span><span class="sxs-lookup"><span data-stu-id="4a835-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="4a835-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a835-134">PARAMETERS</span></span>

### <span data-ttu-id="4a835-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a835-135">-DefaultProfile</span></span>
<span data-ttu-id="4a835-136">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="4a835-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a835-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="4a835-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="4a835-138">Generare l'URL di download delle fatture.</span><span class="sxs-lookup"><span data-stu-id="4a835-138">Generate the download url of the invoices.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a835-139">-Più recenti</span><span class="sxs-lookup"><span data-stu-id="4a835-139">-Latest</span></span>
<span data-ttu-id="4a835-140">Ottieni la fattura più recente.</span><span class="sxs-lookup"><span data-stu-id="4a835-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="4a835-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="4a835-141">-MaxCount</span></span>
<span data-ttu-id="4a835-142">Determina il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="4a835-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="4a835-143">-Name</span><span class="sxs-lookup"><span data-stu-id="4a835-143">-Name</span></span>
<span data-ttu-id="4a835-144">Nome di una fattura specifica da ottenere o la più recente, se non specificata.</span><span class="sxs-lookup"><span data-stu-id="4a835-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="4a835-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="4a835-145">-BillingAccountName</span></span>
<span data-ttu-id="4a835-146">Nome di un account di fatturazione specifico per cui ottenere le fatture.</span><span class="sxs-lookup"><span data-stu-id="4a835-146">Name of a specific billing account to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a835-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="4a835-147">-BillingProfileName</span></span>
<span data-ttu-id="4a835-148">Nome di un profilo di fatturazione specifico per cui ottenere le fatture.</span><span class="sxs-lookup"><span data-stu-id="4a835-148">Name of a specific billing profile to get invoices for.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a835-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="4a835-149">-PeriodStartDate</span></span>
<span data-ttu-id="4a835-150">Data di inizio per la fattura.</span><span class="sxs-lookup"><span data-stu-id="4a835-150">Start date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4a835-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="4a835-151">-PeriodEndDate</span></span>
<span data-ttu-id="4a835-152">Data di fine per la fattura.</span><span class="sxs-lookup"><span data-stu-id="4a835-152">End date for invoice.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```



### <span data-ttu-id="4a835-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a835-153">CommonParameters</span></span>
<span data-ttu-id="4a835-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a835-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a835-155">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a835-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a835-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="4a835-156">INPUTS</span></span>

### <span data-ttu-id="4a835-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4a835-157">None</span></span>

## <span data-ttu-id="4a835-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a835-158">OUTPUTS</span></span>

### <span data-ttu-id="4a835-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="4a835-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="4a835-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="4a835-160">NOTES</span></span>

## <span data-ttu-id="4a835-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a835-161">RELATED LINKS</span></span>
