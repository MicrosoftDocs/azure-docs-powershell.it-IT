---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: 3da9950f2dfdf38bc4e1b461ffd1fcf409b445e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673837"
---
# <span data-ttu-id="7cebb-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="7cebb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cebb-102">SYNOPSIS</span></span>
<span data-ttu-id="7cebb-103">Crea un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="7cebb-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="7cebb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cebb-104">SYNTAX</span></span>

### <span data-ttu-id="7cebb-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7cebb-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cebb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cebb-107">DESCRIPTION</span></span>
<span data-ttu-id="7cebb-108">Il cmdlet **Add-AzAutoscaleSetting** crea un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="7cebb-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="7cebb-109">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="7cebb-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7cebb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cebb-110">EXAMPLES</span></span>

### <span data-ttu-id="7cebb-111">Esempio 1: creare un'impostazione di scalabilità verticale</span><span class="sxs-lookup"><span data-stu-id="7cebb-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="7cebb-112">I primi due comandi usano New-AzAutoscaleRule per creare due regole di scalabilità, $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="7cebb-112">The first two commands use New-AzAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="7cebb-113">Il terzo e il quarto comando usano New-AzAutoscaleProfile per creare profili di scala, $Profile 1 e $Profile 2, usando $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="7cebb-113">The third and fourth commands use New-AzAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="7cebb-114">Il comando finale crea un'impostazione di scalabilità verticale usando i profili in $Profile 1 e $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="7cebb-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="7cebb-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cebb-115">PARAMETERS</span></span>

### <span data-ttu-id="7cebb-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="7cebb-116">-AutoscaleProfile</span></span>
<span data-ttu-id="7cebb-117">Specifica un elenco di profili da aggiungere all'impostazione di scalabilità verticale oppure $Null per aggiungere nessun profilo.</span><span class="sxs-lookup"><span data-stu-id="7cebb-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cebb-118">-DefaultProfile</span></span>
<span data-ttu-id="7cebb-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7cebb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7cebb-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-120">-DisableSetting</span></span>
<span data-ttu-id="7cebb-121">Disabilita un'impostazione di scalabilità esistente.</span><span class="sxs-lookup"><span data-stu-id="7cebb-121">Disables an existing Autoscale setting.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cebb-122">-InputObject</span></span>
<span data-ttu-id="7cebb-123">Specifica completa di un AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7cebb-124">-Location</span></span>
<span data-ttu-id="7cebb-125">Specifica la posizione dell'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="7cebb-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cebb-126">-Name</span></span>
<span data-ttu-id="7cebb-127">Specifica il nome dell'impostazione di scalabilità verticale da creare.</span><span class="sxs-lookup"><span data-stu-id="7cebb-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-128">-Notifica</span><span class="sxs-lookup"><span data-stu-id="7cebb-128">-Notification</span></span>
<span data-ttu-id="7cebb-129">Specifica un elenco di notifiche separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="7cebb-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cebb-130">-ResourceGroupName</span></span>
<span data-ttu-id="7cebb-131">Specifica il nome del gruppo di risorse per la risorsa associata all'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="7cebb-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7cebb-132">-TargetResourceId</span></span>
<span data-ttu-id="7cebb-133">Specifica l'ID della risorsa da scalare.</span><span class="sxs-lookup"><span data-stu-id="7cebb-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cebb-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7cebb-134">-Confirm</span></span>
<span data-ttu-id="7cebb-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cebb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cebb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cebb-136">-WhatIf</span></span>
<span data-ttu-id="7cebb-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cebb-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cebb-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7cebb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cebb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cebb-139">CommonParameters</span></span>
<span data-ttu-id="7cebb-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cebb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cebb-141">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cebb-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cebb-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cebb-142">INPUTS</span></span>

### <span data-ttu-id="7cebb-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="7cebb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="7cebb-144">System.String</span></span>

### <span data-ttu-id="7cebb-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7cebb-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7cebb-146">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. AutoscaleProfile, Microsoft. Azure. PowerShell. cmdlet. monitor, versione = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7cebb-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7cebb-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification, Microsoft. Azure. PowerShell. cmdlet. monitor, versione = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7cebb-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="7cebb-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cebb-148">OUTPUTS</span></span>

### <span data-ttu-id="7cebb-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7cebb-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="7cebb-150">Note</span><span class="sxs-lookup"><span data-stu-id="7cebb-150">NOTES</span></span>

## <span data-ttu-id="7cebb-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cebb-151">RELATED LINKS</span></span>

[<span data-ttu-id="7cebb-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="7cebb-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="7cebb-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="7cebb-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="7cebb-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="7cebb-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="7cebb-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)

