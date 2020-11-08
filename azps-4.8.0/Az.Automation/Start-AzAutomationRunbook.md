---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032664"
---
# <span data-ttu-id="42975-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="42975-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42975-102">SYNOPSIS</span></span>
<span data-ttu-id="42975-103">Avvia un processo di Runbook.</span><span class="sxs-lookup"><span data-stu-id="42975-103">Starts a runbook job.</span></span>

## <span data-ttu-id="42975-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42975-104">SYNTAX</span></span>

### <span data-ttu-id="42975-105">ByAsynchronousReturnJob (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42975-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42975-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="42975-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42975-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42975-107">DESCRIPTION</span></span>
<span data-ttu-id="42975-108">Il cmdlet **Start-AzAutomationRunbook** avvia un processo di Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="42975-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="42975-109">Specificare l'ID o il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="42975-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="42975-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42975-110">EXAMPLES</span></span>

### <span data-ttu-id="42975-111">Esempio 1: avviare un processo di Runbook</span><span class="sxs-lookup"><span data-stu-id="42975-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="42975-112">Questo comando avvia un processo Runbook per la runbook denominata Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="42975-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="42975-113">Esempio 2: avviare un processo di Runbook di Python 2 con parametri</span><span class="sxs-lookup"><span data-stu-id="42975-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="42975-114">Questo comando avvia un processo Runbook per il Runbook Python 2 denominato RunbkPy01 nell'account di automazione di Azure denominato Contoso17 con "ValueForPosition1" come primo parametro posizionale e "ValueForPosition2" per il secondo.</span><span class="sxs-lookup"><span data-stu-id="42975-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="42975-115">Esempio 3: avviare un processo di Runbook e attendere i risultati</span><span class="sxs-lookup"><span data-stu-id="42975-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="42975-116">Questo comando avvia un processo Runbook per la runbook denominata Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="42975-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="42975-117">Questo comando specifica il parametro _wait_ .</span><span class="sxs-lookup"><span data-stu-id="42975-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="42975-118">Di conseguenza, restituisce i risultati dopo il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="42975-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="42975-119">Il cmdlet attende fino a 1000 secondi per i risultati.</span><span class="sxs-lookup"><span data-stu-id="42975-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="42975-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42975-120">PARAMETERS</span></span>

### <span data-ttu-id="42975-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="42975-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="42975-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42975-122">-DefaultProfile</span></span>
<span data-ttu-id="42975-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="42975-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42975-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="42975-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="42975-125">Specifica il numero di secondi in cui il cmdlet attende che un processo finisca prima di abbandonare il processo.</span><span class="sxs-lookup"><span data-stu-id="42975-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="42975-126">Il valore predefinito è 10800 o tre ore.</span><span class="sxs-lookup"><span data-stu-id="42975-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="42975-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="42975-127">-Name</span></span>
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

### <span data-ttu-id="42975-128">-Parameters</span><span class="sxs-lookup"><span data-stu-id="42975-128">-Parameters</span></span>
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

### <span data-ttu-id="42975-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42975-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="42975-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="42975-130">-RunOn</span></span>
<span data-ttu-id="42975-131">Specifica il gruppo di lavoro ibrido su cui eseguire Runbook.</span><span class="sxs-lookup"><span data-stu-id="42975-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="42975-132">-Wait</span><span class="sxs-lookup"><span data-stu-id="42975-132">-Wait</span></span>
<span data-ttu-id="42975-133">Indica che il cmdlet attende che il processo venga completato, sospeso o fallito e quindi restituirà il controllo a Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42975-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="42975-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42975-134">CommonParameters</span></span>
<span data-ttu-id="42975-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42975-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42975-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42975-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42975-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42975-137">INPUTS</span></span>

### <span data-ttu-id="42975-138">System. String</span><span class="sxs-lookup"><span data-stu-id="42975-138">System.String</span></span>

## <span data-ttu-id="42975-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42975-139">OUTPUTS</span></span>

### <span data-ttu-id="42975-140">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="42975-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="42975-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="42975-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="42975-142">Note</span><span class="sxs-lookup"><span data-stu-id="42975-142">NOTES</span></span>

## <span data-ttu-id="42975-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42975-143">RELATED LINKS</span></span>

[<span data-ttu-id="42975-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="42975-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="42975-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="42975-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="42975-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="42975-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="42975-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="42975-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="42975-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
