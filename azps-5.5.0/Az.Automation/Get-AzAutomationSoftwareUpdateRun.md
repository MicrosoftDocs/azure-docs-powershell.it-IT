---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201159"
---
# <span data-ttu-id="3415e-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="3415e-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="3415e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3415e-102">SYNOPSIS</span></span>
<span data-ttu-id="3415e-103">Ottiene un elenco di aggiornamenti software di automazione di Azure eseguiti.</span><span class="sxs-lookup"><span data-stu-id="3415e-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="3415e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3415e-104">SYNTAX</span></span>

### <span data-ttu-id="3415e-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3415e-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3415e-106">ById</span><span class="sxs-lookup"><span data-stu-id="3415e-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3415e-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="3415e-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3415e-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="3415e-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3415e-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3415e-109">DESCRIPTION</span></span>
<span data-ttu-id="3415e-110">Il Get-AzAutomationSoftwareUpdateRun cmdlet di aggiornamento software restituisce un elenco di esecuzioni dell'aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="3415e-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="3415e-111">Poiché a una configurazione di aggiornamento software è associata una pianificazione, questa può essere attivata più volte.</span><span class="sxs-lookup"><span data-stu-id="3415e-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="3415e-112">Ogni volta che viene attivata una pianificazione, viene creata un'esecuzione dell'aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="3415e-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="3415e-113">L'esecuzione degli aggiornamenti è un'aggregazione del risultato di tutte le esecuzioni del computer.</span><span class="sxs-lookup"><span data-stu-id="3415e-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="3415e-114">È possibile ottenere l'esecuzione per una specifica configurazione di aggiornamento software passando il parametro SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="3415e-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="3415e-115">Per ottenere una esecuzione specifica, è necessario passare il parametro name.</span><span class="sxs-lookup"><span data-stu-id="3415e-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="3415e-116">È anche possibile elencare le esecuzioni con uno stato specifico, eseguire l'esecuzione in base al sistema operativo specifico o viene avviata dopo un'ora specifica passando il parametro appropriato.</span><span class="sxs-lookup"><span data-stu-id="3415e-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="3415e-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3415e-117">EXAMPLES</span></span>

### <span data-ttu-id="3415e-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3415e-118">Example 1</span></span>
<span data-ttu-id="3415e-119">Questo esempio elenca tutti gli aggiornamenti eseguiti da una specifica configurazione di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="3415e-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="3415e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3415e-120">PARAMETERS</span></span>

### <span data-ttu-id="3415e-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3415e-121">-AutomationAccountName</span></span>
<span data-ttu-id="3415e-122">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="3415e-122">The automation account name.</span></span>

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

### <span data-ttu-id="3415e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3415e-123">-DefaultProfile</span></span>
<span data-ttu-id="3415e-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3415e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3415e-125">-Id</span><span class="sxs-lookup"><span data-stu-id="3415e-125">-Id</span></span>
<span data-ttu-id="3415e-126">ID della configurazione di aggiornamento software eseguita.</span><span class="sxs-lookup"><span data-stu-id="3415e-126">Id of the software update configuration run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415e-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="3415e-127">-OperatingSystem</span></span>
<span data-ttu-id="3415e-128">Sistema operativo dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3415e-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3415e-129">-ResourceGroupName</span></span>
<span data-ttu-id="3415e-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3415e-130">The resource group name.</span></span>

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

### <span data-ttu-id="3415e-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3415e-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="3415e-132">La configurazione dell'aggiornamento software ha attivato l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3415e-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415e-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3415e-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="3415e-134">Nome della configurazione di aggiornamento software attivata per l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3415e-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415e-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="3415e-135">-StartTime</span></span>
<span data-ttu-id="3415e-136">Ora di inizio minima dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3415e-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415e-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="3415e-137">-Status</span></span>
<span data-ttu-id="3415e-138">Stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3415e-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3415e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3415e-139">CommonParameters</span></span>
<span data-ttu-id="3415e-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3415e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3415e-141">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3415e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3415e-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="3415e-142">INPUTS</span></span>

### <span data-ttu-id="3415e-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3415e-143">System.Guid</span></span>

### <span data-ttu-id="3415e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3415e-144">System.String</span></span>

### <span data-ttu-id="3415e-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3415e-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="3415e-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3415e-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3415e-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="3415e-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="3415e-148">System.DateTime Offset</span><span class="sxs-lookup"><span data-stu-id="3415e-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="3415e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3415e-149">OUTPUTS</span></span>

### <span data-ttu-id="3415e-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="3415e-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="3415e-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="3415e-151">NOTES</span></span>

## <span data-ttu-id="3415e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3415e-152">RELATED LINKS</span></span>
