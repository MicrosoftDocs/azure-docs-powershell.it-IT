---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b2f7410f45a5b60a768d22fe7e66b7d8c1e4ad94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184998"
---
# <span data-ttu-id="8cba7-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8cba7-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="8cba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cba7-102">SYNOPSIS</span></span>
<span data-ttu-id="8cba7-103">Crea un'impostazione di gradazione automatica.</span><span class="sxs-lookup"><span data-stu-id="8cba7-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="8cba7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cba7-104">SYNTAX</span></span>

### <span data-ttu-id="8cba7-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8cba7-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cba7-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8cba7-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cba7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cba7-107">DESCRIPTION</span></span>
<span data-ttu-id="8cba7-108">Il cmdlet **Add-AzAutoscaleSetting** crea un'impostazione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="8cba7-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="8cba7-109">Questo cmdlet implementa il criterio ShouldProcess, ad esempio potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere effettivamente la risorsa.</span><span class="sxs-lookup"><span data-stu-id="8cba7-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="8cba7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cba7-110">EXAMPLES</span></span>

### <span data-ttu-id="8cba7-111">Esempio 1: Creare un'impostazione di gradazione automatica</span><span class="sxs-lookup"><span data-stu-id="8cba7-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="8cba7-112">I primi due comandi usano [Nuovo-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) per creare due regole di scala $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="8cba7-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="8cba7-113">Il terzo e il quarto comando usano [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) per creare profili di gradazione automatica, $Profile 1 e $Profile 2, usando $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="8cba7-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="8cba7-114">Il comando finale crea un'impostazione di gradazione automatica usando i profili disponibili in $Profile 1 e $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="8cba7-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="8cba7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cba7-115">PARAMETERS</span></span>

### <span data-ttu-id="8cba7-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="8cba7-116">-AutoscaleProfile</span></span>
<span data-ttu-id="8cba7-117">Specifica un elenco di profili da aggiungere all'impostazione di gradazione automatica oppure $Null non aggiungere alcun profilo.</span><span class="sxs-lookup"><span data-stu-id="8cba7-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="8cba7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cba7-118">-DefaultProfile</span></span>
<span data-ttu-id="8cba7-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="8cba7-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cba7-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="8cba7-120">-DisableSetting</span></span>
<span data-ttu-id="8cba7-121">Disabilita un'impostazione di gradazione automatica esistente.</span><span class="sxs-lookup"><span data-stu-id="8cba7-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="8cba7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cba7-122">-InputObject</span></span>
<span data-ttu-id="8cba7-123">Specifiche complete di una reimpostazione della scala automatica</span><span class="sxs-lookup"><span data-stu-id="8cba7-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="8cba7-124">-Location</span><span class="sxs-lookup"><span data-stu-id="8cba7-124">-Location</span></span>
<span data-ttu-id="8cba7-125">Specifica la posizione dell'impostazione di scala automatica.</span><span class="sxs-lookup"><span data-stu-id="8cba7-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="8cba7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="8cba7-126">-Name</span></span>
<span data-ttu-id="8cba7-127">Specifica il nome dell'impostazione di scala automatica da creare.</span><span class="sxs-lookup"><span data-stu-id="8cba7-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="8cba7-128">-Notifica</span><span class="sxs-lookup"><span data-stu-id="8cba7-128">-Notification</span></span>
<span data-ttu-id="8cba7-129">Specifica un elenco di notifiche separate da virgola.</span><span class="sxs-lookup"><span data-stu-id="8cba7-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="8cba7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cba7-130">-ResourceGroupName</span></span>
<span data-ttu-id="8cba7-131">Specifica il nome del gruppo di risorse per la risorsa associata all'impostazione di scalabilità automatica.</span><span class="sxs-lookup"><span data-stu-id="8cba7-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="8cba7-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="8cba7-132">-TargetResourceId</span></span>
<span data-ttu-id="8cba7-133">Specifica l'ID della risorsa da scalare automaticamente.</span><span class="sxs-lookup"><span data-stu-id="8cba7-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="8cba7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cba7-134">-Confirm</span></span>
<span data-ttu-id="8cba7-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cba7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cba7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cba7-136">-WhatIf</span></span>
<span data-ttu-id="8cba7-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cba7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cba7-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cba7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cba7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cba7-139">CommonParameters</span></span>
<span data-ttu-id="8cba7-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cba7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cba7-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8cba7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cba7-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cba7-142">INPUTS</span></span>

### <span data-ttu-id="8cba7-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8cba7-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="8cba7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8cba7-144">System.String</span></span>

### <span data-ttu-id="8cba7-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8cba7-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8cba7-146">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8cba7-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8cba7-147">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8cba7-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8cba7-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cba7-148">OUTPUTS</span></span>

### <span data-ttu-id="8cba7-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8cba7-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="8cba7-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cba7-150">NOTES</span></span>

## <span data-ttu-id="8cba7-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cba7-151">RELATED LINKS</span></span>

[<span data-ttu-id="8cba7-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8cba7-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="8cba7-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="8cba7-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="8cba7-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="8cba7-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="8cba7-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="8cba7-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


