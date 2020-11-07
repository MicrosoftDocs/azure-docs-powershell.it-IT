---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 1e5c30f1e4ca1fef4aa78b2e4b6394068878b1c4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685022"
---
# <span data-ttu-id="f8065-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8065-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f8065-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8065-102">SYNOPSIS</span></span>
<span data-ttu-id="f8065-103">Crea una configurazione di aggiornamento software di automazione di Azure pianificata.</span><span class="sxs-lookup"><span data-stu-id="f8065-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="f8065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8065-104">SYNTAX</span></span>

### <span data-ttu-id="f8065-105">Windows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f8065-105">Windows (Default)</span></span>
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

### <span data-ttu-id="f8065-106">Linux</span><span class="sxs-lookup"><span data-stu-id="f8065-106">Linux</span></span>
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

## <span data-ttu-id="f8065-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8065-107">DESCRIPTION</span></span>
<span data-ttu-id="f8065-108">Crea una configurazione di aggiornamento software che viene eseguita in una programmazione per aggiornare un elenco di computer.</span><span class="sxs-lookup"><span data-stu-id="f8065-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="f8065-109">I computer includono sia le macchine virtuali Azure che i computer non AZ.</span><span class="sxs-lookup"><span data-stu-id="f8065-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="f8065-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8065-110">EXAMPLES</span></span>

### <span data-ttu-id="f8065-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8065-111">Example 1</span></span>
<span data-ttu-id="f8065-112">Crea una configurazione di aggiornamento software per installare gli aggiornamenti critici in due macchine virtuali di Windows Azure una volta ogni sabato 9.</span><span class="sxs-lookup"><span data-stu-id="f8065-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="f8065-113">La durata dell'aggiornamento è impostata su 2 ore in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="f8065-113">Update duration is set to 2 hours in this example.</span></span>

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
                                                 -AzVMResourceId $targetMachines `
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

## <span data-ttu-id="f8065-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8065-114">PARAMETERS</span></span>

### <span data-ttu-id="f8065-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f8065-115">-AutomationAccountName</span></span>
<span data-ttu-id="f8065-116">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="f8065-116">The automation account name.</span></span>

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

### <span data-ttu-id="f8065-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="f8065-117">-AzureQuery</span></span>
<span data-ttu-id="f8065-118">Query Dynamic Group Azure.</span><span class="sxs-lookup"><span data-stu-id="f8065-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="f8065-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="f8065-119">-AzureVMResourceId</span></span>
<span data-ttu-id="f8065-120">ID risorsa per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8065-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="f8065-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8065-121">-DefaultProfile</span></span>
<span data-ttu-id="f8065-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f8065-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8065-123">-Durata</span><span class="sxs-lookup"><span data-stu-id="f8065-123">-Duration</span></span>
<span data-ttu-id="f8065-124">Durata massima per l'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="f8065-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="f8065-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="f8065-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="f8065-126">KB numero di aggiornamenti esclusi.</span><span class="sxs-lookup"><span data-stu-id="f8065-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="f8065-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="f8065-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="f8065-128">Maschere di pacchetti Linux escluse.</span><span class="sxs-lookup"><span data-stu-id="f8065-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="f8065-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="f8065-129">-IncludedKbNumber</span></span>
<span data-ttu-id="f8065-130">KB numeri di aggiornamenti inclusi.</span><span class="sxs-lookup"><span data-stu-id="f8065-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="f8065-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="f8065-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="f8065-132">Classificazioni pacchetto Linux incluse.</span><span class="sxs-lookup"><span data-stu-id="f8065-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="f8065-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="f8065-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="f8065-134">Maschere di pacchetti Linux incluse.</span><span class="sxs-lookup"><span data-stu-id="f8065-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="f8065-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="f8065-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="f8065-136">Incluse le classificazioni di Windows Update.</span><span class="sxs-lookup"><span data-stu-id="f8065-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="f8065-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="f8065-137">-Linux</span></span>
<span data-ttu-id="f8065-138">Indica che la configurazione di aggiornamento software è destinata ai computer del sistema operativo Linux.</span><span class="sxs-lookup"><span data-stu-id="f8065-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="f8065-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="f8065-139">-NonAzureComputer</span></span>
<span data-ttu-id="f8065-140">Nomi di computer non AZ.</span><span class="sxs-lookup"><span data-stu-id="f8065-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="f8065-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="f8065-141">-NonAzureQuery</span></span>
<span data-ttu-id="f8065-142">Query di gruppo dinamico non Azure.</span><span class="sxs-lookup"><span data-stu-id="f8065-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="f8065-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="f8065-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="f8065-144">Pubblica attività.</span><span class="sxs-lookup"><span data-stu-id="f8065-144">Post task.</span></span>

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

### <span data-ttu-id="f8065-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="f8065-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="f8065-146">Parametro Post-attività.</span><span class="sxs-lookup"><span data-stu-id="f8065-146">Post task parameter.</span></span>

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

### <span data-ttu-id="f8065-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="f8065-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="f8065-148">Attività preliminare.</span><span class="sxs-lookup"><span data-stu-id="f8065-148">Pre task.</span></span>

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

### <span data-ttu-id="f8065-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="f8065-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="f8065-150">Parametro pre-attività.</span><span class="sxs-lookup"><span data-stu-id="f8065-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="f8065-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="f8065-151">-RebootOnly</span></span>
<span data-ttu-id="f8065-152">Indica che la configurazione dell'aggiornamento software riavvierà solo i computer.</span><span class="sxs-lookup"><span data-stu-id="f8065-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="f8065-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="f8065-153">-RebootSetting</span></span>
<span data-ttu-id="f8065-154">Riavviare seeting.</span><span class="sxs-lookup"><span data-stu-id="f8065-154">Reboot Seeting.</span></span>

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

### <span data-ttu-id="f8065-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8065-155">-ResourceGroupName</span></span>
<span data-ttu-id="f8065-156">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f8065-156">The resource group name.</span></span>

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

### <span data-ttu-id="f8065-157">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="f8065-157">-Schedule</span></span>
<span data-ttu-id="f8065-158">Pianificare l'oggetto usato per la configurazione dell'aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="f8065-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="f8065-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="f8065-159">-Windows</span></span>
<span data-ttu-id="f8065-160">Indica che la configurazione di aggiornamento software è destinata ai computer per sistemi operativi Windows.</span><span class="sxs-lookup"><span data-stu-id="f8065-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="f8065-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8065-161">-Confirm</span></span>
<span data-ttu-id="f8065-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8065-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8065-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8065-163">-WhatIf</span></span>
<span data-ttu-id="f8065-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8065-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8065-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8065-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8065-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8065-166">CommonParameters</span></span>
<span data-ttu-id="f8065-167">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8065-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8065-168">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8065-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8065-169">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8065-169">INPUTS</span></span>

### <span data-ttu-id="f8065-170">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="f8065-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="f8065-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f8065-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f8065-172">System. String []</span><span class="sxs-lookup"><span data-stu-id="f8065-172">System.String[]</span></span>

### <span data-ttu-id="f8065-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="f8065-173">System.TimeSpan</span></span>

### <span data-ttu-id="f8065-174">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. WindowsUpdateClasses []</span><span class="sxs-lookup"><span data-stu-id="f8065-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="f8065-175">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. LinuxPackageClasses []</span><span class="sxs-lookup"><span data-stu-id="f8065-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="f8065-176">System. String</span><span class="sxs-lookup"><span data-stu-id="f8065-176">System.String</span></span>

## <span data-ttu-id="f8065-177">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8065-177">OUTPUTS</span></span>

### <span data-ttu-id="f8065-178">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8065-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f8065-179">Note</span><span class="sxs-lookup"><span data-stu-id="f8065-179">NOTES</span></span>

## <span data-ttu-id="f8065-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8065-180">RELATED LINKS</span></span>
