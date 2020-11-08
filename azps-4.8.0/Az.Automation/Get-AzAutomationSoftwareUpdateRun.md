---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032680"
---
# <span data-ttu-id="92807-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="92807-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="92807-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="92807-102">SYNOPSIS</span></span>
<span data-ttu-id="92807-103">Ottiene un elenco di sequenze di aggiornamento del software di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="92807-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="92807-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92807-104">SYNTAX</span></span>

### <span data-ttu-id="92807-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92807-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92807-106">ById</span><span class="sxs-lookup"><span data-stu-id="92807-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92807-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="92807-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92807-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="92807-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="92807-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92807-109">DESCRIPTION</span></span>
<span data-ttu-id="92807-110">Il cmdlet Get-AzAutomationSoftwareUpdateRun restituisce un elenco di esecuzioni di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="92807-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="92807-111">Poiché una configurazione di aggiornamento software ha una pianificazione associata, può essere attivata più volte.</span><span class="sxs-lookup"><span data-stu-id="92807-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="92807-112">Ogni volta che viene attivata una programmazione verrà generata un'esecuzione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="92807-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="92807-113">L'esecuzione dell'aggiornamento è un'aggregazione del risultato di tutte le esecuzioni dei computer.</span><span class="sxs-lookup"><span data-stu-id="92807-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="92807-114">Puoi ottenere l'esecuzione per una configurazione di aggiornamento software specifica passando il parametro SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="92807-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="92807-115">Per ottenere una determinata esecuzione, devi passare il parametro Name.</span><span class="sxs-lookup"><span data-stu-id="92807-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="92807-116">È anche possibile elencare le esecuzioni con uno stato specifico, eseguire la destinazione di un sistema operativo specifico o eseguire l'avvio dopo un determinato periodo di tempo passando il parametro appropriato.</span><span class="sxs-lookup"><span data-stu-id="92807-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="92807-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92807-117">EXAMPLES</span></span>

### <span data-ttu-id="92807-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92807-118">Example 1</span></span>
<span data-ttu-id="92807-119">Questo esempio elenca tutti gli aggiornamenti eseguiti da una specifica configurazione di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="92807-119">This example list all update runs triggered by a specific software update configuration.</span></span>

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

## <span data-ttu-id="92807-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="92807-120">PARAMETERS</span></span>

### <span data-ttu-id="92807-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="92807-121">-AutomationAccountName</span></span>
<span data-ttu-id="92807-122">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="92807-122">The automation account name.</span></span>

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

### <span data-ttu-id="92807-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92807-123">-DefaultProfile</span></span>
<span data-ttu-id="92807-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92807-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92807-125">-ID</span><span class="sxs-lookup"><span data-stu-id="92807-125">-Id</span></span>
<span data-ttu-id="92807-126">ID dell'esecuzione della configurazione dell'aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="92807-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="92807-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="92807-127">-OperatingSystem</span></span>
<span data-ttu-id="92807-128">Sistema operativo dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="92807-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="92807-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92807-129">-ResourceGroupName</span></span>
<span data-ttu-id="92807-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="92807-130">The resource group name.</span></span>

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

### <span data-ttu-id="92807-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="92807-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="92807-132">La configurazione dell'aggiornamento software ha attivato l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="92807-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="92807-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="92807-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="92807-134">Il nome della configurazione dell'aggiornamento software ha attivato l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="92807-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="92807-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="92807-135">-StartTime</span></span>
<span data-ttu-id="92807-136">Ora di inizio minima della corsa.</span><span class="sxs-lookup"><span data-stu-id="92807-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="92807-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="92807-137">-Status</span></span>
<span data-ttu-id="92807-138">Stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="92807-138">Status of the run.</span></span>

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

### <span data-ttu-id="92807-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92807-139">CommonParameters</span></span>
<span data-ttu-id="92807-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92807-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92807-141">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92807-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92807-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="92807-142">INPUTS</span></span>

### <span data-ttu-id="92807-143">System. Guid</span><span class="sxs-lookup"><span data-stu-id="92807-143">System.Guid</span></span>

### <span data-ttu-id="92807-144">System. String</span><span class="sxs-lookup"><span data-stu-id="92807-144">System.String</span></span>

### <span data-ttu-id="92807-145">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="92807-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="92807-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. PowerShell. cmdlet. Automation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="92807-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="92807-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. PowerShell. cmdlet. Automation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="92807-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="92807-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="92807-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="92807-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92807-149">OUTPUTS</span></span>

### <span data-ttu-id="92807-150">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="92807-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="92807-151">Note</span><span class="sxs-lookup"><span data-stu-id="92807-151">NOTES</span></span>

## <span data-ttu-id="92807-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92807-152">RELATED LINKS</span></span>
