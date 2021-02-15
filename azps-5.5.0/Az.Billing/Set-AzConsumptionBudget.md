---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: 89d628790297bfb677dab11f0b19ba525d8b9e47
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196991"
---
# <span data-ttu-id="259ed-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="259ed-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="259ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="259ed-102">SYNOPSIS</span></span>
<span data-ttu-id="259ed-103">Aggiornare un preventivo in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="259ed-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="259ed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="259ed-104">SYNTAX</span></span>

### <span data-ttu-id="259ed-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="259ed-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="259ed-106">Notifica</span><span class="sxs-lookup"><span data-stu-id="259ed-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="259ed-107">Piping</span><span class="sxs-lookup"><span data-stu-id="259ed-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="259ed-108">Piping e notifica</span><span class="sxs-lookup"><span data-stu-id="259ed-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="259ed-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="259ed-109">DESCRIPTION</span></span>
<span data-ttu-id="259ed-110">Il Set-AzConsumptionBudget cmdlet aggiorna un preventivo in una sottoscrizione o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="259ed-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="259ed-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="259ed-111">EXAMPLES</span></span>

### <span data-ttu-id="259ed-112">Esempio 1: Aggiornare un budget in base a un nuovo importo con un nome di budget a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="259ed-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="259ed-113">Esempio 2: Aggiornare un budget con una notifica quando il costo o l'utilizzo raggiunge una soglia del 90% a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="259ed-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -Name PSBudget -NotificationKey notificationKey-ps1234 -NotificationEnabled -NotificationThreshold 90 -ContactEmail johndoe@contoso.com,janesmith@contoso.com -ContactRole Owner,Reader,Contributor
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
Notification:  NotificationKey:  notificationKey-ps1234
               Threshold:  90
               Enabled:  true
               ContactEmail:  johndoe@contoso.com,janesmith@contoso.com
               ContactRole:  Owner,Reader,Contributor
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="259ed-114">Esempio 3: Aggiornare un preventivo in base a un nuovo importo con un nome di preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="259ed-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
```powershell
PS C:\> Set-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -Amount 75
Amount:  75     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="259ed-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="259ed-115">PARAMETERS</span></span>

### <span data-ttu-id="259ed-116">-Importo</span><span class="sxs-lookup"><span data-stu-id="259ed-116">-Amount</span></span>
<span data-ttu-id="259ed-117">Importo del preventivo.</span><span class="sxs-lookup"><span data-stu-id="259ed-117">Amount of a budget.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-118">-Category</span><span class="sxs-lookup"><span data-stu-id="259ed-118">-Category</span></span>
<span data-ttu-id="259ed-119">La categoria del preventivo può essere costo o utilizzo.</span><span class="sxs-lookup"><span data-stu-id="259ed-119">Category of the budget can be cost or usage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Cost, Usage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="259ed-120">-ContactEmail</span></span>
<span data-ttu-id="259ed-121">Indirizzi di posta elettronica a cui inviare la notifica sul budget quando viene superata la soglia.</span><span class="sxs-lookup"><span data-stu-id="259ed-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="259ed-122">-ContactGroup</span></span>
<span data-ttu-id="259ed-123">Gruppi di azioni a cui inviare la notifica sul budget quando viene superata la soglia.</span><span class="sxs-lookup"><span data-stu-id="259ed-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="259ed-124">-ContactRole</span></span>
<span data-ttu-id="259ed-125">Ruoli di contatto a cui inviare la notifica sul budget quando viene superata la soglia.</span><span class="sxs-lookup"><span data-stu-id="259ed-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Notification, Piping and Notification
Aliases:
Accepted values: Owner, Reader, Contributor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="259ed-126">-DefaultProfile</span></span>
<span data-ttu-id="259ed-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="259ed-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="259ed-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="259ed-128">-EndDate</span></span>
<span data-ttu-id="259ed-129">Data di fine (AAAA-MM-GG in UTC) del periodo di tempo di un budget.</span><span class="sxs-lookup"><span data-stu-id="259ed-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="259ed-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="259ed-130">-InputObject</span></span>
<span data-ttu-id="259ed-131">Oggetto Budget.</span><span class="sxs-lookup"><span data-stu-id="259ed-131">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="259ed-132">-MeterFilter</span></span>
<span data-ttu-id="259ed-133">Elenco separato da virgole di metri in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="259ed-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="259ed-134">Obbligatorio se la categoria è di utilizzo.</span><span class="sxs-lookup"><span data-stu-id="259ed-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="259ed-135">-Name</span><span class="sxs-lookup"><span data-stu-id="259ed-135">-Name</span></span>
<span data-ttu-id="259ed-136">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="259ed-136">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="259ed-137">-NotificationEnabled</span></span>
<span data-ttu-id="259ed-138">La notifica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="259ed-138">The notification is enabled.</span></span>
<span data-ttu-id="259ed-139">Se non viene specificato, la notifica è disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="259ed-139">If not specified, the notification is disabled by default.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="259ed-140">-NotificationKey</span></span>
<span data-ttu-id="259ed-141">Chiave di una notifica associata a un budget, necessaria per creare una notifica con opzione di notifica abilitata, soglia di notifica, messaggi di posta elettronica dei contatti, gruppi di contatti o ruoli di contatto.</span><span class="sxs-lookup"><span data-stu-id="259ed-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

```yaml
Type: System.String
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="259ed-142">-NotificationThreshold</span></span>
<span data-ttu-id="259ed-143">Valore soglia associato a una notifica.</span><span class="sxs-lookup"><span data-stu-id="259ed-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="259ed-144">La notifica viene inviata quando il costo o l'utilizzo ha superato la soglia.</span><span class="sxs-lookup"><span data-stu-id="259ed-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="259ed-145">È sempre una percentuale e deve essere compresa tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="259ed-145">It is always percent and has to be between 0 and 1000.</span></span>

```yaml
Type: System.Nullable`1[System.Decimal]
Parameter Sets: Notification, Piping and Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="259ed-146">-ResourceFilter</span></span>
<span data-ttu-id="259ed-147">Elenco separato da virgole di istanze di risorse in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="259ed-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="259ed-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="259ed-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="259ed-149">Elenco separato da virgole di gruppi di risorse in base a cui filtrare.</span><span class="sxs-lookup"><span data-stu-id="259ed-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="259ed-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="259ed-150">-ResourceGroupName</span></span>
<span data-ttu-id="259ed-151">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="259ed-151">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription, Notification
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="259ed-152">-StartDate</span></span>
<span data-ttu-id="259ed-153">Data di inizio (AAAA-MM-GG in UTC) del periodo di tempo di un budget.</span><span class="sxs-lookup"><span data-stu-id="259ed-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="259ed-154">Non prima del mese corrente per la grana temporale mensile.</span><span class="sxs-lookup"><span data-stu-id="259ed-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="259ed-155">Non prima di tre mesi per le grane trimestrali.</span><span class="sxs-lookup"><span data-stu-id="259ed-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="259ed-156">Non prima di dodici mesi per il grano tempo annuale.</span><span class="sxs-lookup"><span data-stu-id="259ed-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="259ed-157">Data di inizio futura non superiore a tre mesi.</span><span class="sxs-lookup"><span data-stu-id="259ed-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="259ed-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="259ed-158">-TimeGrain</span></span>
<span data-ttu-id="259ed-159">Le ora del budget possono essere mensili, trimestrali o annuali.</span><span class="sxs-lookup"><span data-stu-id="259ed-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Monthly, Quarterly, Annually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="259ed-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="259ed-160">-Confirm</span></span>
<span data-ttu-id="259ed-161">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="259ed-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="259ed-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="259ed-162">-WhatIf</span></span>
<span data-ttu-id="259ed-163">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="259ed-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="259ed-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="259ed-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="259ed-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="259ed-165">CommonParameters</span></span>
<span data-ttu-id="259ed-166">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="259ed-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="259ed-167">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="259ed-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="259ed-168">INPUT</span><span class="sxs-lookup"><span data-stu-id="259ed-168">INPUTS</span></span>

### <span data-ttu-id="259ed-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="259ed-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="259ed-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="259ed-170">OUTPUTS</span></span>

### <span data-ttu-id="259ed-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="259ed-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="259ed-172">NOTE</span><span class="sxs-lookup"><span data-stu-id="259ed-172">NOTES</span></span>

## <span data-ttu-id="259ed-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="259ed-173">RELATED LINKS</span></span>
