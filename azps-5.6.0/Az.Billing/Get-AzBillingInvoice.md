---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azbillinginvoice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzBillingInvoice.md
ms.openlocfilehash: 604109a80171ff4bb294dc1643081cd8e933d728
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959757"
---
# <span data-ttu-id="eefd7-101">Get-AzBillingInvoice</span><span class="sxs-lookup"><span data-stu-id="eefd7-101">Get-AzBillingInvoice</span></span>

## <span data-ttu-id="eefd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eefd7-102">SYNOPSIS</span></span>
<span data-ttu-id="eefd7-103">Ottenere le fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eefd7-103">Get billing invoices of the subscription.</span></span>
<span data-ttu-id="eefd7-104">Ottenere le fatture di un account di fatturazione e di un profilo di fatturazione</span><span class="sxs-lookup"><span data-stu-id="eefd7-104">Get billing invoices of a billing account and billing profile</span></span>

## <span data-ttu-id="eefd7-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eefd7-105">SYNTAX</span></span>

### <span data-ttu-id="eefd7-106">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eefd7-106">List (Default)</span></span>
```
Get-AzBillingInvoice [-MaxCount <Int32>] [-GenerateDownloadUrl] [-DefaultProfile <IAzureContextContainer>] [-BillingAccountName] [-BillingProfileName]
 [<CommonParameters>]
```

### <span data-ttu-id="eefd7-107">Più recenti</span><span class="sxs-lookup"><span data-stu-id="eefd7-107">Latest</span></span>
```
Get-AzBillingInvoice [-Latest] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>] [-BillingAccountName] [-BillingProfileName]
```

### <span data-ttu-id="eefd7-108">Single</span><span class="sxs-lookup"><span data-stu-id="eefd7-108">Single</span></span>
```
Get-AzBillingInvoice -Name <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eefd7-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eefd7-109">DESCRIPTION</span></span>
<span data-ttu-id="eefd7-110">Il **cmdlet Get-AzBillingInvoice** riceve le fatture di fatturazione dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eefd7-110">The **Get-AzBillingInvoice** cmdlet gets billing invoices of the subscription.</span></span> 

## <span data-ttu-id="eefd7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eefd7-111">EXAMPLES</span></span>

### <span data-ttu-id="eefd7-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eefd7-112">Example 1</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest
```

<span data-ttu-id="eefd7-113">Ottenere la fattura più recente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="eefd7-113">Get the latest invoice of the subscription.</span></span>

### <span data-ttu-id="eefd7-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="eefd7-114">Example 2</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543
```

<span data-ttu-id="eefd7-115">Ottenere la fattura dell'abbonamento con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="eefd7-115">Get the invoice of the subscription with the specified name.</span></span>

### <span data-ttu-id="eefd7-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="eefd7-116">Example 3</span></span>
```
PS C:\> Get-AzBillingInvoice
```

<span data-ttu-id="eefd7-117">Ottenere tutte le fatture disponibili dell'abbonamento in ordine cronologico inverso a partire dalla fattura più recente senza scaricare l'URL.</span><span class="sxs-lookup"><span data-stu-id="eefd7-117">Get all available invoices of the subscription in reverse chronological order beginning with the most recent invoice without download Url.</span></span> 

### <span data-ttu-id="eefd7-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="eefd7-118">Example 4</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -MaxCount 10
```

<span data-ttu-id="eefd7-119">Ottieni le 10 fatture più recenti dell'abbonamento e includi l'URL di download nei risultati.</span><span class="sxs-lookup"><span data-stu-id="eefd7-119">Get most recent 10 invoices of the subscription and include the download Url in the result.</span></span>

### <span data-ttu-id="eefd7-120">Esempio 5</span><span class="sxs-lookup"><span data-stu-id="eefd7-120">Example 5</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 2017-02-18-432543543 -GenerateDownloadUrl
```

<span data-ttu-id="eefd7-121">Ottenere la fattura specifica per nome e includere l'URL di download nel risultato.</span><span class="sxs-lookup"><span data-stu-id="eefd7-121">Get the specific invoice by name and include download url in the result.</span></span>

### <span data-ttu-id="eefd7-122">Esempio 6</span><span class="sxs-lookup"><span data-stu-id="eefd7-122">Example 6</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="eefd7-123">Ottenere le fatture in base al nome dell'account di fatturazione e includere l'URL di download per ogni fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="eefd7-123">Get invoices by billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="eefd7-124">Esempio 7</span><span class="sxs-lookup"><span data-stu-id="eefd7-124">Example 7</span></span>
```
PS C:\> Get-AzBillingInvoice -Name 0000000000 -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="eefd7-125">Ottenere una fattura specifica in base al nome della fattura e al nome dell'account di fatturazione e includere l'URL di download per ogni fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="eefd7-125">Get specific invoice by invoice name and billing account name and include download url for each invoice in the result.</span></span>

### <span data-ttu-id="eefd7-126">Esempio 8</span><span class="sxs-lookup"><span data-stu-id="eefd7-126">Example 8</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -GenerateDownloadUrl
```

<span data-ttu-id="eefd7-127">Ottieni l'ultima fattura in base al nome dell'account di fatturazione e includi l'URL di download per la fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="eefd7-127">Get latest invoice by billing account name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="eefd7-128">Esempio 9</span><span class="sxs-lookup"><span data-stu-id="eefd7-128">Example 9</span></span>
```
PS C:\> Get-AzBillingInvoice -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -MaxCount 10
```

<span data-ttu-id="eefd7-129">Ottieni le 10 fatture più recenti dell'account di fatturazione specifico e del profilo di fatturazione specifico e includi l'URL di download nel risultato.</span><span class="sxs-lookup"><span data-stu-id="eefd7-129">Get most recent 10 invoices of the specific billing account and specific billing profile and include the download Url in the result.</span></span>

### <span data-ttu-id="eefd7-130">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="eefd7-130">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -Latest -GenerateDownloadUrl -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 
```

<span data-ttu-id="eefd7-131">Ottieni l'ultima fattura in base al nome dell'account di fatturazione e al nome del profilo di fatturazione e includi l'URL di download per la fattura nei risultati.</span><span class="sxs-lookup"><span data-stu-id="eefd7-131">Get latest invoice by billing account name and billing profile name and include download url for invoice in the result.</span></span>

### <span data-ttu-id="eefd7-132">Esempio 10</span><span class="sxs-lookup"><span data-stu-id="eefd7-132">Example 10</span></span>
```
PS C:\> Get-AzBillingInvoice -BillingAccountName 00000000-0000-0000-0000-000000000000:00000000-0000-0000-0000-000000000000_0000-00-00 -BillingProfileName 0000-0000-000-000 -PeriodStartDate 0000-00-00 -PeriodEndDate 0000-00-00
```

<span data-ttu-id="eefd7-133">Ottenere le fatture in base al nome dell'account di fatturazione e al nome del profilo di fatturazione per un periodo di fatturazione specificato in base alla data di inizio e alla data di fine del periodo.</span><span class="sxs-lookup"><span data-stu-id="eefd7-133">Get invoices by billing account name and billing profile name for a billing period specified by perioStart date and periodEnd date.</span></span>


## <span data-ttu-id="eefd7-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eefd7-134">PARAMETERS</span></span>

### <span data-ttu-id="eefd7-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eefd7-135">-DefaultProfile</span></span>
<span data-ttu-id="eefd7-136">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eefd7-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eefd7-137">-GenerateDownloadUrl</span><span class="sxs-lookup"><span data-stu-id="eefd7-137">-GenerateDownloadUrl</span></span>
<span data-ttu-id="eefd7-138">Generare l'URL di download delle fatture.</span><span class="sxs-lookup"><span data-stu-id="eefd7-138">Generate the download url of the invoices.</span></span>

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

### <span data-ttu-id="eefd7-139">-Più recenti</span><span class="sxs-lookup"><span data-stu-id="eefd7-139">-Latest</span></span>
<span data-ttu-id="eefd7-140">Ottieni la fattura più recente.</span><span class="sxs-lookup"><span data-stu-id="eefd7-140">Get the latest invoice.</span></span>

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

### <span data-ttu-id="eefd7-141">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="eefd7-141">-MaxCount</span></span>
<span data-ttu-id="eefd7-142">Determina il numero massimo di record da restituire.</span><span class="sxs-lookup"><span data-stu-id="eefd7-142">Determines the maximum number of records to return.</span></span>

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

### <span data-ttu-id="eefd7-143">-Name</span><span class="sxs-lookup"><span data-stu-id="eefd7-143">-Name</span></span>
<span data-ttu-id="eefd7-144">Nome di una fattura specifica da ottenere o la più recente, se non specificata.</span><span class="sxs-lookup"><span data-stu-id="eefd7-144">Name of a specific invoice to get or the most recent if not specified.</span></span>

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

### <span data-ttu-id="eefd7-145">-BillingAccountName</span><span class="sxs-lookup"><span data-stu-id="eefd7-145">-BillingAccountName</span></span>
<span data-ttu-id="eefd7-146">Nome di un account di fatturazione specifico per cui ottenere le fatture.</span><span class="sxs-lookup"><span data-stu-id="eefd7-146">Name of a specific billing account to get invoices for.</span></span>

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

### <span data-ttu-id="eefd7-147">-BillingProfileName</span><span class="sxs-lookup"><span data-stu-id="eefd7-147">-BillingProfileName</span></span>
<span data-ttu-id="eefd7-148">Nome di un profilo di fatturazione specifico per cui ottenere le fatture.</span><span class="sxs-lookup"><span data-stu-id="eefd7-148">Name of a specific billing profile to get invoices for.</span></span>

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

### <span data-ttu-id="eefd7-149">-PeriodStartDate</span><span class="sxs-lookup"><span data-stu-id="eefd7-149">-PeriodStartDate</span></span>
<span data-ttu-id="eefd7-150">Data di inizio per la fattura.</span><span class="sxs-lookup"><span data-stu-id="eefd7-150">Start date for invoice.</span></span>

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

### <span data-ttu-id="eefd7-151">-PeriodEndDate</span><span class="sxs-lookup"><span data-stu-id="eefd7-151">-PeriodEndDate</span></span>
<span data-ttu-id="eefd7-152">Data di fine per la fattura.</span><span class="sxs-lookup"><span data-stu-id="eefd7-152">End date for invoice.</span></span>

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



### <span data-ttu-id="eefd7-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eefd7-153">CommonParameters</span></span>
<span data-ttu-id="eefd7-154">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eefd7-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eefd7-155">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eefd7-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eefd7-156">INPUT</span><span class="sxs-lookup"><span data-stu-id="eefd7-156">INPUTS</span></span>

### <span data-ttu-id="eefd7-157">Nessuno</span><span class="sxs-lookup"><span data-stu-id="eefd7-157">None</span></span>

## <span data-ttu-id="eefd7-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eefd7-158">OUTPUTS</span></span>

### <span data-ttu-id="eefd7-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span><span class="sxs-lookup"><span data-stu-id="eefd7-159">Microsoft.Azure.Commands.Billing.Models.PSInvoice</span></span>

## <span data-ttu-id="eefd7-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="eefd7-160">NOTES</span></span>

## <span data-ttu-id="eefd7-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eefd7-161">RELATED LINKS</span></span>
