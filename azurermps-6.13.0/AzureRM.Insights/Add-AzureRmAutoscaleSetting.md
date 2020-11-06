---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 3f78c12dfacdaaacc43025fa613c2bf5f61f5553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515260"
---
# <span data-ttu-id="04ff9-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="04ff9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="04ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="04ff9-103">Crea un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="04ff9-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04ff9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04ff9-104">SYNTAX</span></span>

### <span data-ttu-id="04ff9-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04ff9-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04ff9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="04ff9-107">DESCRIPTION</span></span>
<span data-ttu-id="04ff9-108">Il cmdlet **Add-AzureRmAutoscaleSetting** crea un'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="04ff9-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="04ff9-109">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere conferma all'utente prima di creare, modificare o rimuovere la risorsa.</span><span class="sxs-lookup"><span data-stu-id="04ff9-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="04ff9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04ff9-110">EXAMPLES</span></span>

### <span data-ttu-id="04ff9-111">Esempio 1: creare un'impostazione di scalabilità verticale</span><span class="sxs-lookup"><span data-stu-id="04ff9-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="04ff9-112">I primi due comandi usano New-AzureRmAutoscaleRule per creare due regole di scalabilità, $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="04ff9-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="04ff9-113">Il terzo e il quarto comando usano New-AzureRmAutoscaleProfile per creare profili di scala, $Profile 1 e $Profile 2, usando $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="04ff9-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="04ff9-114">Il comando finale crea un'impostazione di scalabilità verticale usando i profili in $Profile 1 e $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="04ff9-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="04ff9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="04ff9-115">PARAMETERS</span></span>

### <span data-ttu-id="04ff9-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="04ff9-116">-AutoscaleProfile</span></span>
<span data-ttu-id="04ff9-117">Specifica un elenco di profili da aggiungere all'impostazione di scalabilità verticale oppure $Null per aggiungere nessun profilo.</span><span class="sxs-lookup"><span data-stu-id="04ff9-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="04ff9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ff9-118">-DefaultProfile</span></span>
<span data-ttu-id="04ff9-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="04ff9-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04ff9-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-120">-DisableSetting</span></span>
<span data-ttu-id="04ff9-121">Disabilita un'impostazione di scalabilità esistente.</span><span class="sxs-lookup"><span data-stu-id="04ff9-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="04ff9-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04ff9-122">-InputObject</span></span>
<span data-ttu-id="04ff9-123">Specifica completa di un AutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="04ff9-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="04ff9-124">-Location</span></span>
<span data-ttu-id="04ff9-125">Specifica la posizione dell'impostazione di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="04ff9-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="04ff9-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="04ff9-126">-Name</span></span>
<span data-ttu-id="04ff9-127">Specifica il nome dell'impostazione di scalabilità verticale da creare.</span><span class="sxs-lookup"><span data-stu-id="04ff9-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="04ff9-128">-Notifica</span><span class="sxs-lookup"><span data-stu-id="04ff9-128">-Notification</span></span>
<span data-ttu-id="04ff9-129">Specifica un elenco di notifiche separate da virgole.</span><span class="sxs-lookup"><span data-stu-id="04ff9-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="04ff9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ff9-130">-ResourceGroupName</span></span>
<span data-ttu-id="04ff9-131">Specifica il nome del gruppo di risorse per la risorsa associata all'impostazione di scala.</span><span class="sxs-lookup"><span data-stu-id="04ff9-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="04ff9-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="04ff9-132">-TargetResourceId</span></span>
<span data-ttu-id="04ff9-133">Specifica l'ID della risorsa da scalare.</span><span class="sxs-lookup"><span data-stu-id="04ff9-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="04ff9-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="04ff9-134">-Confirm</span></span>
<span data-ttu-id="04ff9-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04ff9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04ff9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04ff9-136">-WhatIf</span></span>
<span data-ttu-id="04ff9-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04ff9-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04ff9-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04ff9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04ff9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ff9-139">CommonParameters</span></span>
<span data-ttu-id="04ff9-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ff9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ff9-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ff9-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ff9-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="04ff9-142">INPUTS</span></span>

### <span data-ttu-id="04ff9-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="04ff9-144">System. String</span><span class="sxs-lookup"><span data-stu-id="04ff9-144">System.String</span></span>

### <span data-ttu-id="04ff9-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="04ff9-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="04ff9-146">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. AutoscaleProfile, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="04ff9-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="04ff9-147">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. AutoscaleNotification, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="04ff9-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="04ff9-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04ff9-148">OUTPUTS</span></span>

### <span data-ttu-id="04ff9-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="04ff9-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="04ff9-150">Note</span><span class="sxs-lookup"><span data-stu-id="04ff9-150">NOTES</span></span>

## <span data-ttu-id="04ff9-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04ff9-151">RELATED LINKS</span></span>

[<span data-ttu-id="04ff9-152">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-152">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="04ff9-153">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="04ff9-153">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="04ff9-154">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="04ff9-154">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="04ff9-155">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="04ff9-155">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


