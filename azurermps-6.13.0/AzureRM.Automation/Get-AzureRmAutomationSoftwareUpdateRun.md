---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d49d99f8edd3ffe0c25886447eac0bbd15837fc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686949"
---
# <span data-ttu-id="87885-101">Get-AzureRmAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="87885-101">Get-AzureRmAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="87885-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87885-102">SYNOPSIS</span></span>
<span data-ttu-id="87885-103">Ottiene un elenco di sequenze di aggiornamento del software di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="87885-103">Gets a list of azure automation software update runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87885-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87885-104">SYNTAX</span></span>

### <span data-ttu-id="87885-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="87885-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>]
 [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87885-106">ById</span><span class="sxs-lookup"><span data-stu-id="87885-106">ById</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87885-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="87885-107">BySucName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87885-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="87885-108">BySuc</span></span>
```
Get-AzureRmAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="87885-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87885-109">DESCRIPTION</span></span>
<span data-ttu-id="87885-110">Il cmdlet Get-AzureRmAutomationSoftwareUpdateRun restituisce un elenco di esecuzioni di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="87885-110">The Get-AzureRmAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="87885-111">Poiché una configurazione di aggiornamento software ha una pianificazione associata, può essere attivata più volte.</span><span class="sxs-lookup"><span data-stu-id="87885-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="87885-112">Ogni volta che viene attivata una programmazione verrà generata un'esecuzione di aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="87885-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="87885-113">L'esecuzione dell'aggiornamento è un'aggregazione del risultato di tutte le esecuzioni dei computer.</span><span class="sxs-lookup"><span data-stu-id="87885-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="87885-114">Puoi ottenere l'esecuzione per una configurazione di aggiornamento software specifica passando il parametro SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="87885-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="87885-115">Per ottenere una determinata esecuzione, devi passare il parametro Name.</span><span class="sxs-lookup"><span data-stu-id="87885-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="87885-116">Puoi anche elencare le esecuzioni con uno stato specifico, eseguire la destinazione di un sistema di operatins specifico o eseguire i passaggi avviati dopo un determinato periodo di tempo passando il parametro appropriato.</span><span class="sxs-lookup"><span data-stu-id="87885-116">You can also list runs with specific status, runs targeting specific operatins system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="87885-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87885-117">EXAMPLES</span></span>

### <span data-ttu-id="87885-118">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="87885-118">Example 1</span></span>
<span data-ttu-id="87885-119">Questo esempio elenca tutti gli aggiornamenti eseguiti da una specifica configurazione di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="87885-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
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

## <span data-ttu-id="87885-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87885-120">PARAMETERS</span></span>

### <span data-ttu-id="87885-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="87885-121">-AutomationAccountName</span></span>
<span data-ttu-id="87885-122">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="87885-122">The automation account name.</span></span>

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

### <span data-ttu-id="87885-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87885-123">-DefaultProfile</span></span>
<span data-ttu-id="87885-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87885-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87885-125">-ID</span><span class="sxs-lookup"><span data-stu-id="87885-125">-Id</span></span>
<span data-ttu-id="87885-126">ID dell'esecuzione della configurazione dell'aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="87885-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="87885-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="87885-127">-OperatingSystem</span></span>
<span data-ttu-id="87885-128">Sistema operativo dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="87885-128">The operating system of the run.</span></span>

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

### <span data-ttu-id="87885-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87885-129">-ResourceGroupName</span></span>
<span data-ttu-id="87885-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="87885-130">The resource group name.</span></span>

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

### <span data-ttu-id="87885-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="87885-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="87885-132">La configurazione dell'aggiornamento software ha attivato l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="87885-132">The software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="87885-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="87885-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="87885-134">Il nome della configurazione dell'aggiornamento software ha attivato l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="87885-134">Name of the software update configuration triggered the run.</span></span>

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

### <span data-ttu-id="87885-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="87885-135">-StartTime</span></span>
<span data-ttu-id="87885-136">Ora di inizio minima della corsa.</span><span class="sxs-lookup"><span data-stu-id="87885-136">Minimum start time of the run.</span></span>

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

### <span data-ttu-id="87885-137">-Stato</span><span class="sxs-lookup"><span data-stu-id="87885-137">-Status</span></span>
<span data-ttu-id="87885-138">Stato dell'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="87885-138">Status of the run.</span></span>

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

### <span data-ttu-id="87885-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87885-139">CommonParameters</span></span>
<span data-ttu-id="87885-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87885-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87885-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87885-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87885-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87885-142">INPUTS</span></span>

### <span data-ttu-id="87885-143">System. Guid</span><span class="sxs-lookup"><span data-stu-id="87885-143">System.Guid</span></span>

### <span data-ttu-id="87885-144">System. String</span><span class="sxs-lookup"><span data-stu-id="87885-144">System.String</span></span>

### <span data-ttu-id="87885-145">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="87885-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="87885-146">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. OperatingSystemType, Microsoft. Azure. Commands. ResourceManager. Automation, Version = 5.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="87885-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="87885-147">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. Commands. ResourceManager. Automation, Version = 5.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="87885-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="87885-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="87885-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="87885-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87885-149">OUTPUTS</span></span>

### <span data-ttu-id="87885-150">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="87885-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="87885-151">Note</span><span class="sxs-lookup"><span data-stu-id="87885-151">NOTES</span></span>

## <span data-ttu-id="87885-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87885-152">RELATED LINKS</span></span>
