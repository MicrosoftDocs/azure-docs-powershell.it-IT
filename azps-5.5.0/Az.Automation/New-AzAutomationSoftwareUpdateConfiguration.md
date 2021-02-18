---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201022"
---
# <span data-ttu-id="36c6a-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="36c6a-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="36c6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36c6a-102">SYNOPSIS</span></span>
<span data-ttu-id="36c6a-103">Crea una configurazione dell'aggiornamento software di automazione di Azure pianificata.</span><span class="sxs-lookup"><span data-stu-id="36c6a-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="36c6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36c6a-104">SYNTAX</span></span>

### <span data-ttu-id="36c6a-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36c6a-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36c6a-106">Linux</span><span class="sxs-lookup"><span data-stu-id="36c6a-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36c6a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="36c6a-107">DESCRIPTION</span></span>
<span data-ttu-id="36c6a-108">Crea una configurazione di aggiornamento software che viene eseguita in base a una pianificazione per aggiornare un elenco di computer.</span><span class="sxs-lookup"><span data-stu-id="36c6a-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="36c6a-109">I computer includono sia macchine virtuali di Azure che computer non az.</span><span class="sxs-lookup"><span data-stu-id="36c6a-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="36c6a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36c6a-110">EXAMPLES</span></span>

### <span data-ttu-id="36c6a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="36c6a-111">Example 1</span></span>
<span data-ttu-id="36c6a-112">Crea una configurazione di aggiornamento software per installare gli aggiornamenti critici in due macchine virtuali di Windows Azure una volta ogni sabato 21.00.</span><span class="sxs-lookup"><span data-stu-id="36c6a-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="36c6a-113">In questo esempio la durata dell'aggiornamento è impostata su 2 ore.</span><span class="sxs-lookup"><span data-stu-id="36c6a-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
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

## <span data-ttu-id="36c6a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36c6a-114">PARAMETERS</span></span>

### <span data-ttu-id="36c6a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="36c6a-115">-AutomationAccountName</span></span>
<span data-ttu-id="36c6a-116">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="36c6a-116">The automation account name.</span></span>

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

### <span data-ttu-id="36c6a-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="36c6a-117">-AzureQuery</span></span>
<span data-ttu-id="36c6a-118">Query azure di gruppo dinamico.</span><span class="sxs-lookup"><span data-stu-id="36c6a-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="36c6a-119">-AzureVMResourceId</span></span>
<span data-ttu-id="36c6a-120">ID risorsa per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="36c6a-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="36c6a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36c6a-121">-DefaultProfile</span></span>
<span data-ttu-id="36c6a-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="36c6a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-123">-Durata</span><span class="sxs-lookup"><span data-stu-id="36c6a-123">-Duration</span></span>
<span data-ttu-id="36c6a-124">Durata massima dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="36c6a-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="36c6a-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="36c6a-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="36c6a-126">Numero di KB di aggiornamenti esclusi.</span><span class="sxs-lookup"><span data-stu-id="36c6a-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="36c6a-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="36c6a-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="36c6a-128">Maschere di pacchetto Linux escluse.</span><span class="sxs-lookup"><span data-stu-id="36c6a-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="36c6a-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="36c6a-129">-IncludedKbNumber</span></span>
<span data-ttu-id="36c6a-130">Numero di aggiornamenti inclusi nella Knowledge Base.</span><span class="sxs-lookup"><span data-stu-id="36c6a-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="36c6a-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="36c6a-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="36c6a-132">Classificazioni di pacchetti Linux incluse.</span><span class="sxs-lookup"><span data-stu-id="36c6a-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="36c6a-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="36c6a-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="36c6a-134">Maschere di pacchetto Linux incluse.</span><span class="sxs-lookup"><span data-stu-id="36c6a-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="36c6a-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="36c6a-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="36c6a-136">Classificazioni di Windows Update incluse.</span><span class="sxs-lookup"><span data-stu-id="36c6a-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="36c6a-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="36c6a-137">-Linux</span></span>
<span data-ttu-id="36c6a-138">Indica che la configurazione dell'aggiornamento software è mirata ai computer del sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="36c6a-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="36c6a-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="36c6a-139">-NonAzureComputer</span></span>
<span data-ttu-id="36c6a-140">Nomi di computer non AZ.</span><span class="sxs-lookup"><span data-stu-id="36c6a-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="36c6a-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="36c6a-141">-NonAzureQuery</span></span>
<span data-ttu-id="36c6a-142">Query di gruppo dinamico non Azure.</span><span class="sxs-lookup"><span data-stu-id="36c6a-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="36c6a-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="36c6a-144">Pubblicare un'attività.</span><span class="sxs-lookup"><span data-stu-id="36c6a-144">Post task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="36c6a-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="36c6a-146">Parametro post-attività.</span><span class="sxs-lookup"><span data-stu-id="36c6a-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="36c6a-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="36c6a-148">Pre-attività.</span><span class="sxs-lookup"><span data-stu-id="36c6a-148">Pre task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="36c6a-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="36c6a-150">Parametro pre-attività.</span><span class="sxs-lookup"><span data-stu-id="36c6a-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="36c6a-151">-RebootOnly</span></span>
<span data-ttu-id="36c6a-152">Indica che la configurazione dell'aggiornamento software riavvierà solo i computer.</span><span class="sxs-lookup"><span data-stu-id="36c6a-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="36c6a-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="36c6a-153">-RebootSetting</span></span>
<span data-ttu-id="36c6a-154">Impostazione del riavvio.</span><span class="sxs-lookup"><span data-stu-id="36c6a-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36c6a-155">-ResourceGroupName</span></span>
<span data-ttu-id="36c6a-156">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="36c6a-156">The resource group name.</span></span>

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

### <span data-ttu-id="36c6a-157">-Pianificazione</span><span class="sxs-lookup"><span data-stu-id="36c6a-157">-Schedule</span></span>
<span data-ttu-id="36c6a-158">Oggetto Schedule usato per la configurazione degli aggiornamenti software.</span><span class="sxs-lookup"><span data-stu-id="36c6a-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="36c6a-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="36c6a-159">-Windows</span></span>
<span data-ttu-id="36c6a-160">Indica che la configurazione dell'aggiornamento software è mirata ai computer del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="36c6a-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="36c6a-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36c6a-161">-Confirm</span></span>
<span data-ttu-id="36c6a-162">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36c6a-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36c6a-163">-WhatIf</span></span>
<span data-ttu-id="36c6a-164">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36c6a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36c6a-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36c6a-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36c6a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36c6a-166">CommonParameters</span></span>
<span data-ttu-id="36c6a-167">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36c6a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36c6a-168">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36c6a-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36c6a-169">INPUT</span><span class="sxs-lookup"><span data-stu-id="36c6a-169">INPUTS</span></span>

### <span data-ttu-id="36c6a-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="36c6a-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="36c6a-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36c6a-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="36c6a-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="36c6a-172">System.String[]</span></span>

### <span data-ttu-id="36c6a-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="36c6a-173">System.TimeSpan</span></span>

### <span data-ttu-id="36c6a-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="36c6a-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="36c6a-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="36c6a-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="36c6a-176">System.String</span><span class="sxs-lookup"><span data-stu-id="36c6a-176">System.String</span></span>

## <span data-ttu-id="36c6a-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36c6a-177">OUTPUTS</span></span>

### <span data-ttu-id="36c6a-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="36c6a-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="36c6a-179">NOTE</span><span class="sxs-lookup"><span data-stu-id="36c6a-179">NOTES</span></span>

## <span data-ttu-id="36c6a-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36c6a-180">RELATED LINKS</span></span>
