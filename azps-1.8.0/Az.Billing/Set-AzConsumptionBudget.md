---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: c159ab71befb52e8131ade0b90e69c4ba8158885
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684899"
---
# <span data-ttu-id="a820a-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="a820a-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="a820a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a820a-102">SYNOPSIS</span></span>
<span data-ttu-id="a820a-103">Aggiornare un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a820a-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="a820a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a820a-104">SYNTAX</span></span>

### <span data-ttu-id="a820a-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a820a-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a820a-106">Notifica</span><span class="sxs-lookup"><span data-stu-id="a820a-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a820a-107">Tubazioni</span><span class="sxs-lookup"><span data-stu-id="a820a-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a820a-108">Piping e notifica</span><span class="sxs-lookup"><span data-stu-id="a820a-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a820a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a820a-109">DESCRIPTION</span></span>
<span data-ttu-id="a820a-110">Il cmdlet Set-AzConsumptionBudget aggiorna un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a820a-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="a820a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a820a-111">EXAMPLES</span></span>

### <span data-ttu-id="a820a-112">Esempio 1: aggiornare un preventivo in base a un nuovo importo con un nome preventivo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="a820a-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
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

### <span data-ttu-id="a820a-113">Esempio 2: aggiornare un preventivo con una notifica quando il costo o l'utilizzo raggiunge una soglia pari a 90% di importo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="a820a-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
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

### <span data-ttu-id="a820a-114">Esempio 3: aggiornare un preventivo in base a un nuovo importo con un nome preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a820a-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
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

## <span data-ttu-id="a820a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a820a-115">PARAMETERS</span></span>

### <span data-ttu-id="a820a-116">-Importo</span><span class="sxs-lookup"><span data-stu-id="a820a-116">-Amount</span></span>
<span data-ttu-id="a820a-117">Importo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="a820a-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="a820a-118">-Categoria</span><span class="sxs-lookup"><span data-stu-id="a820a-118">-Category</span></span>
<span data-ttu-id="a820a-119">La categoria del preventivo può essere costo o uso.</span><span class="sxs-lookup"><span data-stu-id="a820a-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="a820a-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="a820a-120">-ContactEmail</span></span>
<span data-ttu-id="a820a-121">Indirizzi di posta elettronica per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="a820a-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="a820a-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="a820a-122">-ContactGroup</span></span>
<span data-ttu-id="a820a-123">Gruppi di azioni per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="a820a-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="a820a-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="a820a-124">-ContactRole</span></span>
<span data-ttu-id="a820a-125">Contattare i ruoli per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="a820a-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="a820a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a820a-126">-DefaultProfile</span></span>
<span data-ttu-id="a820a-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a820a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a820a-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="a820a-128">-EndDate</span></span>
<span data-ttu-id="a820a-129">Data di fine (AAAA-MM-DD in UTC) del periodo di tempo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="a820a-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="a820a-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a820a-130">-InputObject</span></span>
<span data-ttu-id="a820a-131">Oggetto preventivo.</span><span class="sxs-lookup"><span data-stu-id="a820a-131">Budget object.</span></span>

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

### <span data-ttu-id="a820a-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="a820a-132">-MeterFilter</span></span>
<span data-ttu-id="a820a-133">Elenco delimitato da virgole di metri per il filtro.</span><span class="sxs-lookup"><span data-stu-id="a820a-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="a820a-134">Obbligatorio se Category è l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="a820a-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="a820a-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="a820a-135">-Name</span></span>
<span data-ttu-id="a820a-136">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="a820a-136">Name of a budget.</span></span>

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

### <span data-ttu-id="a820a-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="a820a-137">-NotificationEnabled</span></span>
<span data-ttu-id="a820a-138">La notifica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a820a-138">The notification is enabled.</span></span>
<span data-ttu-id="a820a-139">Se non viene specificato, la notifica viene disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a820a-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="a820a-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="a820a-140">-NotificationKey</span></span>
<span data-ttu-id="a820a-141">Chiave di una notifica associata a un preventivo, necessaria per creare una notifica con l'opzione di notifica attivata, la soglia di notifica, i messaggi di contatto, i gruppi di contatti o i ruoli di contatto.</span><span class="sxs-lookup"><span data-stu-id="a820a-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="a820a-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="a820a-142">-NotificationThreshold</span></span>
<span data-ttu-id="a820a-143">Valore soglia associato a una notifica.</span><span class="sxs-lookup"><span data-stu-id="a820a-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="a820a-144">La notifica viene inviata quando il costo o l'utilizzo supera la soglia.</span><span class="sxs-lookup"><span data-stu-id="a820a-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="a820a-145">È sempre percentuale e deve essere compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="a820a-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="a820a-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="a820a-146">-ResourceFilter</span></span>
<span data-ttu-id="a820a-147">Elenco delimitato da virgole delle istanze delle risorse per il filtro.</span><span class="sxs-lookup"><span data-stu-id="a820a-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="a820a-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="a820a-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="a820a-149">Elenco di gruppi di risorse delimitato da virgole per il filtro.</span><span class="sxs-lookup"><span data-stu-id="a820a-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="a820a-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a820a-150">-ResourceGroupName</span></span>
<span data-ttu-id="a820a-151">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="a820a-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="a820a-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="a820a-152">-StartDate</span></span>
<span data-ttu-id="a820a-153">Data di inizio (AAAA-MM-DD in UTC) del periodo di tempo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="a820a-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="a820a-154">Non prima del mese corrente per il periodo di tempo mensile.</span><span class="sxs-lookup"><span data-stu-id="a820a-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="a820a-155">Non prima di tre mesi per la granulosità del tempo trimestrale.</span><span class="sxs-lookup"><span data-stu-id="a820a-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="a820a-156">Non prima di dodici mesi per il periodo di tempo annuo.</span><span class="sxs-lookup"><span data-stu-id="a820a-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="a820a-157">Data di inizio futura non superiore a tre mesi.</span><span class="sxs-lookup"><span data-stu-id="a820a-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="a820a-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="a820a-158">-TimeGrain</span></span>
<span data-ttu-id="a820a-159">La granulosità temporale del preventivo può essere mensile, trimestrale o annuale.</span><span class="sxs-lookup"><span data-stu-id="a820a-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="a820a-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a820a-160">-Confirm</span></span>
<span data-ttu-id="a820a-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a820a-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a820a-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a820a-162">-WhatIf</span></span>
<span data-ttu-id="a820a-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a820a-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a820a-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a820a-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a820a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a820a-165">CommonParameters</span></span>
<span data-ttu-id="a820a-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a820a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a820a-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a820a-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a820a-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a820a-168">INPUTS</span></span>

### <span data-ttu-id="a820a-169">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="a820a-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="a820a-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a820a-170">OUTPUTS</span></span>

### <span data-ttu-id="a820a-171">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="a820a-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="a820a-172">Note</span><span class="sxs-lookup"><span data-stu-id="a820a-172">NOTES</span></span>

## <span data-ttu-id="a820a-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a820a-173">RELATED LINKS</span></span>
