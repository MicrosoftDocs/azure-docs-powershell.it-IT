---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/set-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Set-AzConsumptionBudget.md
ms.openlocfilehash: 89d628790297bfb677dab11f0b19ba525d8b9e47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478124"
---
# <span data-ttu-id="c7a54-101">Set-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="c7a54-101">Set-AzConsumptionBudget</span></span>

## <span data-ttu-id="c7a54-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7a54-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a54-103">Aggiornare un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7a54-103">Update a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="c7a54-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7a54-104">SYNTAX</span></span>

### <span data-ttu-id="c7a54-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c7a54-105">Subscription (Default)</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a54-106">Notifica</span><span class="sxs-lookup"><span data-stu-id="c7a54-106">Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>] [-ContactGroup <String[]>]
 [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7a54-107">Tubazioni</span><span class="sxs-lookup"><span data-stu-id="c7a54-107">Piping</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7a54-108">Piping e notifica</span><span class="sxs-lookup"><span data-stu-id="c7a54-108">Piping and Notification</span></span>
```
Set-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-Amount <Decimal>]
 [-Category <String>] [-TimeGrain <String>] [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-MeterFilter <String[]>] [-ResourceFilter <String[]>] [-ResourceGroupFilter <String[]>]
 -NotificationKey <String> [-NotificationEnabled] [-NotificationThreshold <Decimal>] [-ContactEmail <String[]>]
 [-ContactGroup <String[]>] [-ContactRole <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7a54-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7a54-109">DESCRIPTION</span></span>
<span data-ttu-id="c7a54-110">Il cmdlet Set-AzConsumptionBudget aggiorna un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7a54-110">The Set-AzConsumptionBudget cmdlet updates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="c7a54-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7a54-111">EXAMPLES</span></span>

### <span data-ttu-id="c7a54-112">Esempio 1: aggiornare un preventivo in base a un nuovo importo con un nome preventivo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="c7a54-112">Example 1: Update a budget by a new amount with a budget name at subscription level</span></span>
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

### <span data-ttu-id="c7a54-113">Esempio 2: aggiornare un preventivo con una notifica quando il costo o l'utilizzo raggiunge una soglia pari a 90% di importo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="c7a54-113">Example 2: Update a budget with a notification when cost or usage reaches a threshold of 90 percent of amount at subscription level</span></span>
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

### <span data-ttu-id="c7a54-114">Esempio 3: aggiornare un preventivo in base a un nuovo importo con un nome preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c7a54-114">Example 3: Update a budget by a new amount with a budget name at resource group level</span></span>
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

## <span data-ttu-id="c7a54-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7a54-115">PARAMETERS</span></span>

### <span data-ttu-id="c7a54-116">-Importo</span><span class="sxs-lookup"><span data-stu-id="c7a54-116">-Amount</span></span>
<span data-ttu-id="c7a54-117">Importo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-117">Amount of a budget.</span></span>

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

### <span data-ttu-id="c7a54-118">-Categoria</span><span class="sxs-lookup"><span data-stu-id="c7a54-118">-Category</span></span>
<span data-ttu-id="c7a54-119">La categoria del preventivo può essere costo o uso.</span><span class="sxs-lookup"><span data-stu-id="c7a54-119">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="c7a54-120">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="c7a54-120">-ContactEmail</span></span>
<span data-ttu-id="c7a54-121">Indirizzi di posta elettronica per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="c7a54-121">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="c7a54-122">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="c7a54-122">-ContactGroup</span></span>
<span data-ttu-id="c7a54-123">Gruppi di azioni per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="c7a54-123">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="c7a54-124">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="c7a54-124">-ContactRole</span></span>
<span data-ttu-id="c7a54-125">Contattare i ruoli per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="c7a54-125">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="c7a54-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a54-126">-DefaultProfile</span></span>
<span data-ttu-id="c7a54-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a54-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a54-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c7a54-128">-EndDate</span></span>
<span data-ttu-id="c7a54-129">Data di fine (AAAA-MM-DD in UTC) del periodo di tempo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-129">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="c7a54-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7a54-130">-InputObject</span></span>
<span data-ttu-id="c7a54-131">Oggetto preventivo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-131">Budget object.</span></span>

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

### <span data-ttu-id="c7a54-132">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="c7a54-132">-MeterFilter</span></span>
<span data-ttu-id="c7a54-133">Elenco delimitato da virgole di metri per il filtro.</span><span class="sxs-lookup"><span data-stu-id="c7a54-133">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="c7a54-134">Obbligatorio se Category è l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-134">Required if category is usage.</span></span>

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

### <span data-ttu-id="c7a54-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7a54-135">-Name</span></span>
<span data-ttu-id="c7a54-136">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-136">Name of a budget.</span></span>

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

### <span data-ttu-id="c7a54-137">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="c7a54-137">-NotificationEnabled</span></span>
<span data-ttu-id="c7a54-138">La notifica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="c7a54-138">The notification is enabled.</span></span>
<span data-ttu-id="c7a54-139">Se non viene specificato, la notifica viene disabilitata per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="c7a54-139">If not specified, the notification is disabled by default.</span></span>

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

### <span data-ttu-id="c7a54-140">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="c7a54-140">-NotificationKey</span></span>
<span data-ttu-id="c7a54-141">Chiave di una notifica associata a un preventivo, necessaria per creare una notifica con l'opzione di notifica attivata, la soglia di notifica, i messaggi di contatto, i gruppi di contatti o i ruoli di contatto.</span><span class="sxs-lookup"><span data-stu-id="c7a54-141">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="c7a54-142">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="c7a54-142">-NotificationThreshold</span></span>
<span data-ttu-id="c7a54-143">Valore soglia associato a una notifica.</span><span class="sxs-lookup"><span data-stu-id="c7a54-143">Threshold value associated with a notification.</span></span>
<span data-ttu-id="c7a54-144">La notifica viene inviata quando il costo o l'utilizzo supera la soglia.</span><span class="sxs-lookup"><span data-stu-id="c7a54-144">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="c7a54-145">È sempre percentuale e deve essere compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="c7a54-145">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="c7a54-146">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="c7a54-146">-ResourceFilter</span></span>
<span data-ttu-id="c7a54-147">Elenco delimitato da virgole delle istanze delle risorse per il filtro.</span><span class="sxs-lookup"><span data-stu-id="c7a54-147">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="c7a54-148">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="c7a54-148">-ResourceGroupFilter</span></span>
<span data-ttu-id="c7a54-149">Elenco di gruppi di risorse delimitato da virgole per il filtro.</span><span class="sxs-lookup"><span data-stu-id="c7a54-149">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="c7a54-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a54-150">-ResourceGroupName</span></span>
<span data-ttu-id="c7a54-151">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-151">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="c7a54-152">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c7a54-152">-StartDate</span></span>
<span data-ttu-id="c7a54-153">Data di inizio (AAAA-MM-DD in UTC) del periodo di tempo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-153">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="c7a54-154">Non prima del mese corrente per il periodo di tempo mensile.</span><span class="sxs-lookup"><span data-stu-id="c7a54-154">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="c7a54-155">Non prima di tre mesi per la granulosità del tempo trimestrale.</span><span class="sxs-lookup"><span data-stu-id="c7a54-155">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="c7a54-156">Non prima di dodici mesi per il periodo di tempo annuo.</span><span class="sxs-lookup"><span data-stu-id="c7a54-156">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="c7a54-157">Data di inizio futura non superiore a tre mesi.</span><span class="sxs-lookup"><span data-stu-id="c7a54-157">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="c7a54-158">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="c7a54-158">-TimeGrain</span></span>
<span data-ttu-id="c7a54-159">La granulosità temporale del preventivo può essere mensile, trimestrale o annuale.</span><span class="sxs-lookup"><span data-stu-id="c7a54-159">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="c7a54-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7a54-160">-Confirm</span></span>
<span data-ttu-id="c7a54-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a54-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a54-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a54-162">-WhatIf</span></span>
<span data-ttu-id="c7a54-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7a54-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a54-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7a54-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a54-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a54-165">CommonParameters</span></span>
<span data-ttu-id="c7a54-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a54-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a54-167">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7a54-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a54-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7a54-168">INPUTS</span></span>

### <span data-ttu-id="c7a54-169">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="c7a54-169">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="c7a54-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7a54-170">OUTPUTS</span></span>

### <span data-ttu-id="c7a54-171">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="c7a54-171">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="c7a54-172">Note</span><span class="sxs-lookup"><span data-stu-id="c7a54-172">NOTES</span></span>

## <span data-ttu-id="c7a54-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7a54-173">RELATED LINKS</span></span>
