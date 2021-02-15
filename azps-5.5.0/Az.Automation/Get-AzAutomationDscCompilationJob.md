---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182191"
---
# <span data-ttu-id="67d7e-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="67d7e-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="67d7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="67d7e-103">Recupera i processi di compilazione DSC nell'automazione.</span><span class="sxs-lookup"><span data-stu-id="67d7e-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="67d7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67d7e-104">SYNTAX</span></span>

### <span data-ttu-id="67d7e-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="67d7e-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="67d7e-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="67d7e-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67d7e-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="67d7e-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67d7e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="67d7e-108">DESCRIPTION</span></span>
<span data-ttu-id="67d7e-109">Il cmdlet **Get-AzAutomationDscCompilationJob** ottiene i processi di compilazione APS Desired State Configuration (DSC) nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="67d7e-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="67d7e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67d7e-110">EXAMPLES</span></span>

### <span data-ttu-id="67d7e-111">Esempio 1: Ottenere tutti i processi di compilazione DSC</span><span class="sxs-lookup"><span data-stu-id="67d7e-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="67d7e-112">Questo comando recupera tutti i processi di compilazione nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="67d7e-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="67d7e-113">Esempio 2: Ottenere processi di compilazione DSC per una configurazione</span><span class="sxs-lookup"><span data-stu-id="67d7e-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="67d7e-114">Questo comando recupera tutti i processi di compilazione per la configurazione DSC denominata ContosoConfiguration nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="67d7e-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="67d7e-115">Esempio 3: Ottenere un processo di compilazione DSC specifico</span><span class="sxs-lookup"><span data-stu-id="67d7e-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="67d7e-116">Questo comando recupera il processo di compilazione con l'ID specificato nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="67d7e-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="67d7e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67d7e-117">PARAMETERS</span></span>

### <span data-ttu-id="67d7e-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67d7e-118">-AutomationAccountName</span></span>
<span data-ttu-id="67d7e-119">Specifica il nome dell'account di automazione che contiene i processi di compilazione DSC che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d7e-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="67d7e-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="67d7e-120">-ConfigurationName</span></span>
<span data-ttu-id="67d7e-121">Specifica il nome della configurazione DSC per cui il cmdlet riceve i processi di compilazione.</span><span class="sxs-lookup"><span data-stu-id="67d7e-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d7e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67d7e-122">-DefaultProfile</span></span>
<span data-ttu-id="67d7e-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="67d7e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67d7e-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="67d7e-124">-EndTime</span></span>
<span data-ttu-id="67d7e-125">Specifica un'ora di fine.</span><span class="sxs-lookup"><span data-stu-id="67d7e-125">Specifies an end time.</span></span>
<span data-ttu-id="67d7e-126">Questo cmdlet recupera i processi di compilazione avviati fino alla data specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="67d7e-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d7e-127">-Id</span><span class="sxs-lookup"><span data-stu-id="67d7e-127">-Id</span></span>
<span data-ttu-id="67d7e-128">Specifica l'ID univoco del processo di compilazione DSC che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d7e-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67d7e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d7e-129">-ResourceGroupName</span></span>
<span data-ttu-id="67d7e-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene i processi di compilazione DSC.</span><span class="sxs-lookup"><span data-stu-id="67d7e-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="67d7e-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="67d7e-131">-StartTime</span></span>
<span data-ttu-id="67d7e-132">Specifica un'ora di inizio.</span><span class="sxs-lookup"><span data-stu-id="67d7e-132">Specifies a start time.</span></span>
<span data-ttu-id="67d7e-133">Questo cmdlet ottiene processi che iniziano in corrispondenza o dopo l'ora specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="67d7e-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d7e-134">-Stato</span><span class="sxs-lookup"><span data-stu-id="67d7e-134">-Status</span></span>
<span data-ttu-id="67d7e-135">Specifica lo stato dei processi che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67d7e-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="67d7e-136">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="67d7e-136">Valid values are:</span></span> 
- <span data-ttu-id="67d7e-137">Completato</span><span class="sxs-lookup"><span data-stu-id="67d7e-137">Completed</span></span> 
- <span data-ttu-id="67d7e-138">Operazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="67d7e-138">Failed</span></span> 
- <span data-ttu-id="67d7e-139">In coda</span><span class="sxs-lookup"><span data-stu-id="67d7e-139">Queued</span></span> 
- <span data-ttu-id="67d7e-140">Avvio in corso</span><span class="sxs-lookup"><span data-stu-id="67d7e-140">Starting</span></span> 
- <span data-ttu-id="67d7e-141">Ripresa</span><span class="sxs-lookup"><span data-stu-id="67d7e-141">Resuming</span></span> 
- <span data-ttu-id="67d7e-142">In esecuzione</span><span class="sxs-lookup"><span data-stu-id="67d7e-142">Running</span></span> 
- <span data-ttu-id="67d7e-143">Arrestato</span><span class="sxs-lookup"><span data-stu-id="67d7e-143">Stopped</span></span> 
- <span data-ttu-id="67d7e-144">Arresto in corso</span><span class="sxs-lookup"><span data-stu-id="67d7e-144">Stopping</span></span> 
- <span data-ttu-id="67d7e-145">Sospeso</span><span class="sxs-lookup"><span data-stu-id="67d7e-145">Suspended</span></span> 
- <span data-ttu-id="67d7e-146">Sospensione</span><span class="sxs-lookup"><span data-stu-id="67d7e-146">Suspending</span></span> 
- <span data-ttu-id="67d7e-147">Attivazione</span><span class="sxs-lookup"><span data-stu-id="67d7e-147">Activating</span></span>
- <span data-ttu-id="67d7e-148">Nuovo</span><span class="sxs-lookup"><span data-stu-id="67d7e-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67d7e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d7e-149">CommonParameters</span></span>
<span data-ttu-id="67d7e-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67d7e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d7e-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d7e-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d7e-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="67d7e-152">INPUTS</span></span>

### <span data-ttu-id="67d7e-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="67d7e-153">System.Guid</span></span>

### <span data-ttu-id="67d7e-154">System.String</span><span class="sxs-lookup"><span data-stu-id="67d7e-154">System.String</span></span>

## <span data-ttu-id="67d7e-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67d7e-155">OUTPUTS</span></span>

### <span data-ttu-id="67d7e-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="67d7e-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="67d7e-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="67d7e-157">NOTES</span></span>

## <span data-ttu-id="67d7e-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67d7e-158">RELATED LINKS</span></span>

[<span data-ttu-id="67d7e-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="67d7e-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="67d7e-160">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="67d7e-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


