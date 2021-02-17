---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210163"
---
# <span data-ttu-id="21243-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="21243-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="21243-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21243-102">SYNOPSIS</span></span>
<span data-ttu-id="21243-103">Creare un preventivo in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21243-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="21243-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21243-104">SYNTAX</span></span>

### <span data-ttu-id="21243-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="21243-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21243-106">Notifica</span><span class="sxs-lookup"><span data-stu-id="21243-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21243-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21243-107">DESCRIPTION</span></span>
<span data-ttu-id="21243-108">Il cmdlet New-AzConsumptionBudget crea un preventivo in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21243-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="21243-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21243-109">EXAMPLES</span></span>

### <span data-ttu-id="21243-110">Esempio 1: Creare un preventivo con un nome di budget a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="21243-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -Amount 60 -Name PSBudget -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="21243-111">Esempio 2: Creare un preventivo con un nome di preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="21243-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
```powershell
PS C:\> New-AzConsumptionBudget -ResourceGroupName RGBudgets -Amount 60 -Name PSBudgetRG -Category Cost -StartDate 2018-06-01 -EndDate 2018-11-01 -TimeGrain Monthly
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="21243-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21243-112">PARAMETERS</span></span>

### <span data-ttu-id="21243-113">-Importo</span><span class="sxs-lookup"><span data-stu-id="21243-113">-Amount</span></span>
<span data-ttu-id="21243-114">Importo del preventivo.</span><span class="sxs-lookup"><span data-stu-id="21243-114">Amount of a budget.</span></span>

```yaml
Type: System.Decimal
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-115">-Category</span><span class="sxs-lookup"><span data-stu-id="21243-115">-Category</span></span>
<span data-ttu-id="21243-116">La categoria del preventivo può essere costo o utilizzo.</span><span class="sxs-lookup"><span data-stu-id="21243-116">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="21243-117">-ContactEmail</span></span>
<span data-ttu-id="21243-118">Indirizzi di posta elettronica a cui inviare la notifica sul budget quando viene superata la soglia.</span><span class="sxs-lookup"><span data-stu-id="21243-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="21243-119">-ContactGroup</span></span>
<span data-ttu-id="21243-120">Gruppi di azioni a cui inviare la notifica sul budget quando viene superata la soglia.</span><span class="sxs-lookup"><span data-stu-id="21243-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="21243-121">-ContactRole</span></span>
<span data-ttu-id="21243-122">Ruoli di contatto a cui inviare la notifica sul budget quando viene superata la soglia.</span><span class="sxs-lookup"><span data-stu-id="21243-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21243-123">-DefaultProfile</span></span>
<span data-ttu-id="21243-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21243-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21243-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="21243-125">-EndDate</span></span>
<span data-ttu-id="21243-126">Data di fine (AAAA-MM-GG in UTC) del periodo di tempo di un budget.</span><span class="sxs-lookup"><span data-stu-id="21243-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="21243-127">-MeterFilter</span></span>
<span data-ttu-id="21243-128">Elenco separato da virgole di metri in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="21243-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="21243-129">Obbligatorio se la categoria è di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="21243-129">Required if category is usage.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-130">-Name</span><span class="sxs-lookup"><span data-stu-id="21243-130">-Name</span></span>
<span data-ttu-id="21243-131">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="21243-131">Name of a budget.</span></span>

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

### <span data-ttu-id="21243-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="21243-132">-NotificationEnabled</span></span>
<span data-ttu-id="21243-133">La notifica è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="21243-133">The notification is enabled or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="21243-134">-NotificationKey</span></span>
<span data-ttu-id="21243-135">Chiave di una notifica associata a un budget, necessaria per creare una notifica con opzione di notifica abilitata, soglia di notifica, messaggi di posta elettronica dei contatti, gruppi di contatti o ruoli di contatto.</span><span class="sxs-lookup"><span data-stu-id="21243-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="21243-136">-NotificationThreshold</span></span>
<span data-ttu-id="21243-137">Valore soglia associato a una notifica.</span><span class="sxs-lookup"><span data-stu-id="21243-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="21243-138">La notifica viene inviata quando il costo o l'utilizzo ha superato la soglia.</span><span class="sxs-lookup"><span data-stu-id="21243-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="21243-139">È sempre una percentuale e deve essere compresa tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="21243-139">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="21243-140">-ResourceFilter</span></span>
<span data-ttu-id="21243-141">Elenco separato da virgole di istanze di risorse in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="21243-141">Comma-separated list of resource instances to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="21243-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="21243-143">Elenco separato da virgole di gruppi di risorse in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="21243-143">Comma-separated list of resource groups to filter on.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21243-144">-ResourceGroupName</span></span>
<span data-ttu-id="21243-145">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="21243-145">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="21243-146">-StartDate</span></span>
<span data-ttu-id="21243-147">Data di inizio (AAAA-MM-GG in UTC) del periodo di tempo di un budget.</span><span class="sxs-lookup"><span data-stu-id="21243-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="21243-148">Non prima del mese corrente per la grana temporale mensile.</span><span class="sxs-lookup"><span data-stu-id="21243-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="21243-149">Non prima di tre mesi per le grane trimestrali.</span><span class="sxs-lookup"><span data-stu-id="21243-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="21243-150">Non prima di dodici mesi per il grano tempo annuale.</span><span class="sxs-lookup"><span data-stu-id="21243-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="21243-151">Data di inizio futura non superiore a tre mesi.</span><span class="sxs-lookup"><span data-stu-id="21243-151">Future start date not more than three months.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="21243-152">-TimeGrain</span></span>
<span data-ttu-id="21243-153">Le ora del budget possono essere mensili, trimestrali o annuali.</span><span class="sxs-lookup"><span data-stu-id="21243-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21243-154">-Confirm</span></span>
<span data-ttu-id="21243-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21243-155">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21243-156">-WhatIf</span></span>
<span data-ttu-id="21243-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21243-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21243-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21243-158">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21243-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21243-159">CommonParameters</span></span>
<span data-ttu-id="21243-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21243-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21243-161">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21243-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21243-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="21243-162">INPUTS</span></span>

### <span data-ttu-id="21243-163">Nessuno</span><span class="sxs-lookup"><span data-stu-id="21243-163">None</span></span>

## <span data-ttu-id="21243-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21243-164">OUTPUTS</span></span>

### <span data-ttu-id="21243-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="21243-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="21243-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="21243-166">NOTES</span></span>

## <span data-ttu-id="21243-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21243-167">RELATED LINKS</span></span>
