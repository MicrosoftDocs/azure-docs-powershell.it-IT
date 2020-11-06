---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517652"
---
# <span data-ttu-id="e4106-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4106-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e4106-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4106-102">SYNOPSIS</span></span>
<span data-ttu-id="e4106-103">Crea una configurazione di aggiornamento software di automazione di Azure pianificata.</span><span class="sxs-lookup"><span data-stu-id="e4106-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4106-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4106-104">SYNTAX</span></span>

### <span data-ttu-id="e4106-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4106-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4106-106">Linux</span><span class="sxs-lookup"><span data-stu-id="e4106-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4106-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4106-107">DESCRIPTION</span></span>
<span data-ttu-id="e4106-108">Crea una configurazione di aggiornamento software che viene eseguita in una programmazione per aggiornare un elenco di computer.</span><span class="sxs-lookup"><span data-stu-id="e4106-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="e4106-109">I computer includono sia le macchine virtuali Azure che i computer non Azure.</span><span class="sxs-lookup"><span data-stu-id="e4106-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="e4106-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4106-110">EXAMPLES</span></span>

### <span data-ttu-id="e4106-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e4106-111">Example 1</span></span>
<span data-ttu-id="e4106-112">Crea una configurazione di aggiornamento software per installare gli aggiornamenti critici in due macchine virtuali di Windows Azure una volta ogni sabato 9.</span><span class="sxs-lookup"><span data-stu-id="e4106-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="e4106-113">La durata dell'aggiornamento è impostata su 2 ore in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="e4106-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="e4106-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4106-114">PARAMETERS</span></span>

### <span data-ttu-id="e4106-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e4106-115">-AutomationAccountName</span></span>
<span data-ttu-id="e4106-116">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="e4106-116">The automation account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="e4106-117">-AzureVMResourceId</span></span>
<span data-ttu-id="e4106-118">ID risorsa per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="e4106-118">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4106-119">-DefaultProfile</span></span>
<span data-ttu-id="e4106-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e4106-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4106-121">-Durata</span><span class="sxs-lookup"><span data-stu-id="e4106-121">-Duration</span></span>
<span data-ttu-id="e4106-122">Durata massima per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="e4106-122">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="e4106-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="e4106-124">KB numero di aggiornamenti esclusi.</span><span class="sxs-lookup"><span data-stu-id="e4106-124">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="e4106-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="e4106-126">Maschere di pacchetti Linux escluse.</span><span class="sxs-lookup"><span data-stu-id="e4106-126">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="e4106-127">-IncludedKbNumber</span></span>
<span data-ttu-id="e4106-128">KB numeri di aggiornamenti inclusi.</span><span class="sxs-lookup"><span data-stu-id="e4106-128">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="e4106-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="e4106-130">Classificazioni pacchetto Linux incluse.</span><span class="sxs-lookup"><span data-stu-id="e4106-130">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="e4106-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="e4106-132">Maschere di pacchetti Linux incluse.</span><span class="sxs-lookup"><span data-stu-id="e4106-132">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="e4106-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="e4106-134">Incluse le classificazioni di Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e4106-134">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="e4106-135">-Linux</span></span>
<span data-ttu-id="e4106-136">Indica che la configurazione di aggiornamento software è destinata ai computer del sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="e4106-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-137">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="e4106-137">-NonAzureComputer</span></span>
<span data-ttu-id="e4106-138">Nomi di computer non Azure.</span><span class="sxs-lookup"><span data-stu-id="e4106-138">Non-Azure computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4106-139">-ResourceGroupName</span></span>
<span data-ttu-id="e4106-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4106-140">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-141">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="e4106-141">-Schedule</span></span>
<span data-ttu-id="e4106-142">Pianificare l'oggetto usato per la configurazione dell'aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="e4106-142">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="e4106-143">-Windows</span></span>
<span data-ttu-id="e4106-144">Indica che la configurazione di aggiornamento software è destinata ai computer per sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="e4106-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4106-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4106-145">-Confirm</span></span>
<span data-ttu-id="e4106-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4106-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4106-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4106-147">-WhatIf</span></span>
<span data-ttu-id="e4106-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4106-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4106-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4106-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4106-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4106-150">CommonParameters</span></span>
<span data-ttu-id="e4106-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4106-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4106-152">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4106-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4106-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4106-153">INPUTS</span></span>

### <span data-ttu-id="e4106-154">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="e4106-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="e4106-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e4106-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e4106-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="e4106-156">System.String[]</span></span>

### <span data-ttu-id="e4106-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="e4106-157">System.TimeSpan</span></span>

### <span data-ttu-id="e4106-158">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="e4106-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="e4106-159">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="e4106-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="e4106-160">System. String</span><span class="sxs-lookup"><span data-stu-id="e4106-160">System.String</span></span>

## <span data-ttu-id="e4106-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4106-161">OUTPUTS</span></span>

### <span data-ttu-id="e4106-162">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4106-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="e4106-163">Note</span><span class="sxs-lookup"><span data-stu-id="e4106-163">NOTES</span></span>

## <span data-ttu-id="e4106-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4106-164">RELATED LINKS</span></span>
