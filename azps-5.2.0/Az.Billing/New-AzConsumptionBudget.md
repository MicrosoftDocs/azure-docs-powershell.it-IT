---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/new-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/New-AzConsumptionBudget.md
ms.openlocfilehash: 1b6e815a8ccb02fe462393df8a91af9800b425df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344779"
---
# <span data-ttu-id="abf86-101">New-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="abf86-101">New-AzConsumptionBudget</span></span>

## <span data-ttu-id="abf86-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="abf86-102">SYNOPSIS</span></span>
<span data-ttu-id="abf86-103">Creare un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="abf86-103">Create a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="abf86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="abf86-104">SYNTAX</span></span>

### <span data-ttu-id="abf86-105">Abbonamento (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="abf86-105">Subscription (Default)</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abf86-106">Notifica</span><span class="sxs-lookup"><span data-stu-id="abf86-106">Notification</span></span>
```
New-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String> -Amount <Decimal>
 -Category <String> -TimeGrain <String> -StartDate <DateTime> [-EndDate <DateTime>]
 [-ResourceGroupName <String>] [-MeterFilter <String[]>] [-ResourceFilter <String[]>]
 [-ResourceGroupFilter <String[]>] -NotificationKey <String> [-NotificationEnabled]
 -NotificationThreshold <Decimal> -ContactEmail <String[]> [-ContactGroup <String[]>] [-ContactRole <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abf86-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="abf86-107">DESCRIPTION</span></span>
<span data-ttu-id="abf86-108">Il cmdlet New-AzConsumptionBudget crea un preventivo in un abbonamento o in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="abf86-108">The New-AzConsumptionBudget cmdlet creates a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="abf86-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="abf86-109">EXAMPLES</span></span>

### <span data-ttu-id="abf86-110">Esempio 1: creare un budget di costo con un nome preventivo a livello di abbonamento</span><span class="sxs-lookup"><span data-stu-id="abf86-110">Example 1: Create a cost budget with a budget name at subscription level</span></span>
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

### <span data-ttu-id="abf86-111">Esempio 2: creare un budget di costo con un nome preventivo a livello di gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="abf86-111">Example 2: Create a cost budget with a budget name at resource group level</span></span>
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

## <span data-ttu-id="abf86-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="abf86-112">PARAMETERS</span></span>

### <span data-ttu-id="abf86-113">-Importo</span><span class="sxs-lookup"><span data-stu-id="abf86-113">-Amount</span></span>
<span data-ttu-id="abf86-114">Importo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="abf86-114">Amount of a budget.</span></span>

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

### <span data-ttu-id="abf86-115">-Categoria</span><span class="sxs-lookup"><span data-stu-id="abf86-115">-Category</span></span>
<span data-ttu-id="abf86-116">La categoria del preventivo può essere costo o uso.</span><span class="sxs-lookup"><span data-stu-id="abf86-116">Category of the budget can be cost or usage.</span></span>

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

### <span data-ttu-id="abf86-117">-ContactEmail</span><span class="sxs-lookup"><span data-stu-id="abf86-117">-ContactEmail</span></span>
<span data-ttu-id="abf86-118">Indirizzi di posta elettronica per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="abf86-118">Email addresses to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="abf86-119">-ContactGroup</span><span class="sxs-lookup"><span data-stu-id="abf86-119">-ContactGroup</span></span>
<span data-ttu-id="abf86-120">Gruppi di azioni per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="abf86-120">Action groups to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="abf86-121">-ContactRole</span><span class="sxs-lookup"><span data-stu-id="abf86-121">-ContactRole</span></span>
<span data-ttu-id="abf86-122">Contattare i ruoli per inviare la notifica preventiva quando la soglia viene superata.</span><span class="sxs-lookup"><span data-stu-id="abf86-122">Contact roles to send the budget notification to when the threshold is exceeded.</span></span>

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

### <span data-ttu-id="abf86-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abf86-123">-DefaultProfile</span></span>
<span data-ttu-id="abf86-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="abf86-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abf86-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="abf86-125">-EndDate</span></span>
<span data-ttu-id="abf86-126">Data di fine (AAAA-MM-DD in UTC) del periodo di tempo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="abf86-126">End date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>

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

### <span data-ttu-id="abf86-127">-MeterFilter</span><span class="sxs-lookup"><span data-stu-id="abf86-127">-MeterFilter</span></span>
<span data-ttu-id="abf86-128">Elenco delimitato da virgole di metri per il filtro.</span><span class="sxs-lookup"><span data-stu-id="abf86-128">Comma-separated list of meters to filter on.</span></span>
<span data-ttu-id="abf86-129">Obbligatorio se Category è l'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="abf86-129">Required if category is usage.</span></span>

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

### <span data-ttu-id="abf86-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="abf86-130">-Name</span></span>
<span data-ttu-id="abf86-131">Nome di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="abf86-131">Name of a budget.</span></span>

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

### <span data-ttu-id="abf86-132">-NotificationEnabled</span><span class="sxs-lookup"><span data-stu-id="abf86-132">-NotificationEnabled</span></span>
<span data-ttu-id="abf86-133">La notifica è abilitata o meno.</span><span class="sxs-lookup"><span data-stu-id="abf86-133">The notification is enabled or not.</span></span>

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

### <span data-ttu-id="abf86-134">-NotificationKey</span><span class="sxs-lookup"><span data-stu-id="abf86-134">-NotificationKey</span></span>
<span data-ttu-id="abf86-135">Chiave di una notifica associata a un preventivo, necessaria per creare una notifica con l'opzione di notifica attivata, la soglia di notifica, i messaggi di contatto, i gruppi di contatti o i ruoli di contatto.</span><span class="sxs-lookup"><span data-stu-id="abf86-135">Key of a notification associated with a budget, required to create a notification with notification enabled switch, notification threshold, contact emails, contact groups, or contact roles.</span></span>

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

### <span data-ttu-id="abf86-136">-NotificationThreshold</span><span class="sxs-lookup"><span data-stu-id="abf86-136">-NotificationThreshold</span></span>
<span data-ttu-id="abf86-137">Valore soglia associato a una notifica.</span><span class="sxs-lookup"><span data-stu-id="abf86-137">Threshold value associated with a notification.</span></span>
<span data-ttu-id="abf86-138">La notifica viene inviata quando il costo o l'utilizzo supera la soglia.</span><span class="sxs-lookup"><span data-stu-id="abf86-138">Notification is sent when the cost or usage exceeded the threshold.</span></span>
<span data-ttu-id="abf86-139">È sempre percentuale e deve essere compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="abf86-139">It is always percent and has to be between 0 and 1000.</span></span>

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

### <span data-ttu-id="abf86-140">-ResourceFilter</span><span class="sxs-lookup"><span data-stu-id="abf86-140">-ResourceFilter</span></span>
<span data-ttu-id="abf86-141">Elenco delimitato da virgole delle istanze delle risorse per il filtro.</span><span class="sxs-lookup"><span data-stu-id="abf86-141">Comma-separated list of resource instances to filter on.</span></span>

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

### <span data-ttu-id="abf86-142">-ResourceGroupFilter</span><span class="sxs-lookup"><span data-stu-id="abf86-142">-ResourceGroupFilter</span></span>
<span data-ttu-id="abf86-143">Elenco di gruppi di risorse delimitato da virgole per il filtro.</span><span class="sxs-lookup"><span data-stu-id="abf86-143">Comma-separated list of resource groups to filter on.</span></span>

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

### <span data-ttu-id="abf86-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abf86-144">-ResourceGroupName</span></span>
<span data-ttu-id="abf86-145">Gruppo di risorse di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="abf86-145">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="abf86-146">-StartDate</span><span class="sxs-lookup"><span data-stu-id="abf86-146">-StartDate</span></span>
<span data-ttu-id="abf86-147">Data di inizio (AAAA-MM-DD in UTC) del periodo di tempo di un preventivo.</span><span class="sxs-lookup"><span data-stu-id="abf86-147">Start date (YYYY-MM-DD in UTC) of time period of a budget.</span></span>
<span data-ttu-id="abf86-148">Non prima del mese corrente per il periodo di tempo mensile.</span><span class="sxs-lookup"><span data-stu-id="abf86-148">Not prior to current month for monthly time grain.</span></span>
<span data-ttu-id="abf86-149">Non prima di tre mesi per la granulosità del tempo trimestrale.</span><span class="sxs-lookup"><span data-stu-id="abf86-149">Not prior to three months for quarterly time grain.</span></span>
<span data-ttu-id="abf86-150">Non prima di dodici mesi per il periodo di tempo annuo.</span><span class="sxs-lookup"><span data-stu-id="abf86-150">Not prior to twelve months for yearly time grain.</span></span>
<span data-ttu-id="abf86-151">Data di inizio futura non superiore a tre mesi.</span><span class="sxs-lookup"><span data-stu-id="abf86-151">Future start date not more than three months.</span></span>

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

### <span data-ttu-id="abf86-152">-TimeGrain</span><span class="sxs-lookup"><span data-stu-id="abf86-152">-TimeGrain</span></span>
<span data-ttu-id="abf86-153">La granulosità temporale del preventivo può essere mensile, trimestrale o annuale.</span><span class="sxs-lookup"><span data-stu-id="abf86-153">Time grain of the budget can be monthly, quarterly, or annually.</span></span>

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

### <span data-ttu-id="abf86-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="abf86-154">-Confirm</span></span>
<span data-ttu-id="abf86-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abf86-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abf86-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abf86-156">-WhatIf</span></span>
<span data-ttu-id="abf86-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abf86-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abf86-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="abf86-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abf86-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abf86-159">CommonParameters</span></span>
<span data-ttu-id="abf86-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abf86-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abf86-161">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abf86-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abf86-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="abf86-162">INPUTS</span></span>

### <span data-ttu-id="abf86-163">Nessuno</span><span class="sxs-lookup"><span data-stu-id="abf86-163">None</span></span>

## <span data-ttu-id="abf86-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="abf86-164">OUTPUTS</span></span>

### <span data-ttu-id="abf86-165">Microsoft. Azure. Commands. consume. Models. PSBudget</span><span class="sxs-lookup"><span data-stu-id="abf86-165">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="abf86-166">Note</span><span class="sxs-lookup"><span data-stu-id="abf86-166">NOTES</span></span>

## <span data-ttu-id="abf86-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="abf86-167">RELATED LINKS</span></span>
