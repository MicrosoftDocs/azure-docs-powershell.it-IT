---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 00eb652bc9779554f1c860edd503fc752c7ccaa0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957678"
---
# <span data-ttu-id="2d98e-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="2d98e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d98e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d98e-103">Avvia un processo del runbook.</span><span class="sxs-lookup"><span data-stu-id="2d98e-103">Starts a runbook job.</span></span>

## <span data-ttu-id="2d98e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d98e-104">SYNTAX</span></span>

### <span data-ttu-id="2d98e-105">ByJob(impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2d98e-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d98e-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="2d98e-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d98e-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2d98e-107">DESCRIPTION</span></span>
<span data-ttu-id="2d98e-108">Il cmdlet **Start-AzAutomationRunbook avvia** un processo runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2d98e-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="2d98e-109">Specificare l'ID o il nome di un runbook.</span><span class="sxs-lookup"><span data-stu-id="2d98e-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="2d98e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d98e-110">EXAMPLES</span></span>

### <span data-ttu-id="2d98e-111">Esempio 1: Avviare un processo del runbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2d98e-112">Questo comando avvia un processo di runbook per il runbook denominato Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2d98e-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="2d98e-113">Esempio 2: Avviare un processo runbook Python 2 con parametri</span><span class="sxs-lookup"><span data-stu-id="2d98e-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="2d98e-114">Questo comando avvia un processo runbook per il runbook Python 2 denominato RunbkPy01 nell'account di automazione di Azure denominato Contoso17 con "ValueForPosition1" come primo parametro posizionale e "ValueForPosition2" per il secondo.</span><span class="sxs-lookup"><span data-stu-id="2d98e-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="2d98e-115">Esempio 3: Avviare un processo del runbook e attendere i risultati</span><span class="sxs-lookup"><span data-stu-id="2d98e-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="2d98e-116">Questo comando avvia un processo di runbook per il runbook denominato Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2d98e-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="2d98e-117">Questo comando specifica il _parametro Wait._</span><span class="sxs-lookup"><span data-stu-id="2d98e-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="2d98e-118">Di conseguenza, restituisce i risultati al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="2d98e-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="2d98e-119">Il cmdlet attende fino a 1000 secondi per i risultati.</span><span class="sxs-lookup"><span data-stu-id="2d98e-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="2d98e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d98e-120">PARAMETERS</span></span>

### <span data-ttu-id="2d98e-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2d98e-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="2d98e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d98e-122">-DefaultProfile</span></span>
<span data-ttu-id="2d98e-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="2d98e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d98e-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="2d98e-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="2d98e-125">Specifica il numero di secondi che il cmdlet attende per il completamento di un processo prima che venga abbandonato.</span><span class="sxs-lookup"><span data-stu-id="2d98e-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="2d98e-126">Il valore predefinito è 10800, o tre ore.</span><span class="sxs-lookup"><span data-stu-id="2d98e-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d98e-127">-Name</span><span class="sxs-lookup"><span data-stu-id="2d98e-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d98e-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="2d98e-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d98e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d98e-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2d98e-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="2d98e-130">-RunOn</span></span>
<span data-ttu-id="2d98e-131">Specifica il gruppo di utenti ibridi in cui eseguire il runbook.</span><span class="sxs-lookup"><span data-stu-id="2d98e-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d98e-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="2d98e-132">-Wait</span></span>
<span data-ttu-id="2d98e-133">Indica che il cmdlet attende che il processo completi, sospende o non riesce e quindi restituisca il controllo a Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2d98e-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d98e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d98e-134">CommonParameters</span></span>
<span data-ttu-id="2d98e-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d98e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d98e-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d98e-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d98e-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="2d98e-137">INPUTS</span></span>

### <span data-ttu-id="2d98e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2d98e-138">System.String</span></span>

## <span data-ttu-id="2d98e-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d98e-139">OUTPUTS</span></span>

### <span data-ttu-id="2d98e-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="2d98e-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="2d98e-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="2d98e-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2d98e-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="2d98e-142">NOTES</span></span>

## <span data-ttu-id="2d98e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d98e-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d98e-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="2d98e-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="2d98e-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="2d98e-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2d98e-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2d98e-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="2d98e-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="2d98e-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2d98e-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
