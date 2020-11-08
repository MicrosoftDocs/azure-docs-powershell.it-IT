---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203177"
---
# <span data-ttu-id="22070-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="22070-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="22070-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22070-102">SYNOPSIS</span></span>
<span data-ttu-id="22070-103">Viene eseguito un elenco di computer di configurazione dell'aggiornamento software di automazione Azure.</span><span class="sxs-lookup"><span data-stu-id="22070-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="22070-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22070-104">SYNTAX</span></span>

### <span data-ttu-id="22070-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22070-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22070-106">ById</span><span class="sxs-lookup"><span data-stu-id="22070-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22070-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="22070-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22070-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="22070-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22070-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22070-109">DESCRIPTION</span></span>
<span data-ttu-id="22070-110">Questo cmdlet restituisce un elenco di esecuzioni dei computer.</span><span class="sxs-lookup"><span data-stu-id="22070-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="22070-111">Ogni esecuzione di aggiornamento software attiverà un'esecuzione del computer per ogni computer di destinazione della configurazione dell'aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="22070-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="22070-112">Per ottenere un'esecuzione specifica del computer, passare il parametro ID.</span><span class="sxs-lookup"><span data-stu-id="22070-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="22070-113">È possibile elencare tutte le esecuzioni del computer, tutte le esecuzioni di un PC specifico, tutte eseguite con uno stato specifico passando i parametri corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="22070-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="22070-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22070-114">EXAMPLES</span></span>

### <span data-ttu-id="22070-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="22070-115">Example 1</span></span>
<span data-ttu-id="22070-116">Questo esempio restituisce tutte le esecuzioni di computer non riuscite per la macchina virtuale di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="22070-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="22070-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22070-117">PARAMETERS</span></span>

### <span data-ttu-id="22070-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22070-118">-AutomationAccountName</span></span>
<span data-ttu-id="22070-119">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="22070-119">The automation account name.</span></span>

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

### <span data-ttu-id="22070-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22070-120">-DefaultProfile</span></span>
<span data-ttu-id="22070-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22070-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22070-122">-ID</span><span class="sxs-lookup"><span data-stu-id="22070-122">-Id</span></span>
<span data-ttu-id="22070-123">ID dell'esecuzione del computer di aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="22070-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="22070-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22070-124">-ResourceGroupName</span></span>
<span data-ttu-id="22070-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22070-125">The resource group name.</span></span>

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

### <span data-ttu-id="22070-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="22070-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="22070-127">L'aggiornamento del software viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22070-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22070-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="22070-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="22070-129">ID dell'esecuzione dell'aggiornamento software.</span><span class="sxs-lookup"><span data-stu-id="22070-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22070-130">-Stato</span><span class="sxs-lookup"><span data-stu-id="22070-130">-Status</span></span>
<span data-ttu-id="22070-131">Stato dell'esecuzione del computer.</span><span class="sxs-lookup"><span data-stu-id="22070-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22070-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="22070-132">-TargetComputer</span></span>
<span data-ttu-id="22070-133">computer di destinazione per l'esecuzione del computer.</span><span class="sxs-lookup"><span data-stu-id="22070-133">target computer for the machine run.</span></span>
<span data-ttu-id="22070-134">Può essere un nome di computer non AZ o un ID delle risorse di Azure VM.</span><span class="sxs-lookup"><span data-stu-id="22070-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22070-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22070-135">CommonParameters</span></span>
<span data-ttu-id="22070-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22070-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22070-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22070-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22070-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22070-138">INPUTS</span></span>

### <span data-ttu-id="22070-139">System. Guid</span><span class="sxs-lookup"><span data-stu-id="22070-139">System.Guid</span></span>

### <span data-ttu-id="22070-140">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="22070-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="22070-141">System. Nullable ' 1 [[Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRunStatus, Microsoft. Azure. PowerShell. cmdlet. Automation, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22070-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="22070-142">System. String</span><span class="sxs-lookup"><span data-stu-id="22070-142">System.String</span></span>

## <span data-ttu-id="22070-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22070-143">OUTPUTS</span></span>

### <span data-ttu-id="22070-144">Microsoft. Azure. Commands. Automation. Model. UpdateManagement. SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="22070-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="22070-145">Note</span><span class="sxs-lookup"><span data-stu-id="22070-145">NOTES</span></span>

## <span data-ttu-id="22070-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22070-146">RELATED LINKS</span></span>
