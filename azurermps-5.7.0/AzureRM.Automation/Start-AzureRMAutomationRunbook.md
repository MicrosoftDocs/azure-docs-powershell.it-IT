---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c3c59c8c4f503b090a77a93014f50dd7e2ce01dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512752"
---
# <span data-ttu-id="29ea3-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="29ea3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="29ea3-102">SYNOPSIS</span></span>
<span data-ttu-id="29ea3-103">Avvia un processo di Runbook.</span><span class="sxs-lookup"><span data-stu-id="29ea3-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29ea3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="29ea3-104">SYNTAX</span></span>

### <span data-ttu-id="29ea3-105">ByAsynchronousReturnJob (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="29ea3-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29ea3-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="29ea3-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29ea3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="29ea3-107">DESCRIPTION</span></span>
<span data-ttu-id="29ea3-108">Il cmdlet **Start-AzureRmAutomationRunbook** avvia un processo di Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="29ea3-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="29ea3-109">Specificare l'ID o il nome di un Runbook.</span><span class="sxs-lookup"><span data-stu-id="29ea3-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="29ea3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="29ea3-110">EXAMPLES</span></span>

### <span data-ttu-id="29ea3-111">Esempio 1: avviare un processo di Runbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="29ea3-112">Questo comando avvia un processo Runbook per la runbook denominata Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="29ea3-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="29ea3-113">Esempio 2: avviare un processo di Runbook e attendere i risultati</span><span class="sxs-lookup"><span data-stu-id="29ea3-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="29ea3-114">Questo comando avvia un processo Runbook per la runbook denominata Runbk01 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="29ea3-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="29ea3-115">Questo comando specifica il parametro _wait_ .</span><span class="sxs-lookup"><span data-stu-id="29ea3-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="29ea3-116">Di conseguenza, restituisce i risultati dopo il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="29ea3-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="29ea3-117">Il cmdlet attende fino a 1000 secondi per i risultati.</span><span class="sxs-lookup"><span data-stu-id="29ea3-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="29ea3-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="29ea3-118">PARAMETERS</span></span>

### <span data-ttu-id="29ea3-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="29ea3-119">-AutomationAccountName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29ea3-120">-DefaultProfile</span></span>
<span data-ttu-id="29ea3-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="29ea3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="29ea3-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="29ea3-123">Specifica il numero di secondi in cui il cmdlet attende che un processo finisca prima di abbandonare il processo.</span><span class="sxs-lookup"><span data-stu-id="29ea3-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="29ea3-124">Il valore predefinito è 10800 o tre ore.</span><span class="sxs-lookup"><span data-stu-id="29ea3-124">The default value is 10800, or three hours.</span></span>

```yaml
Type: Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="29ea3-125">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-126">-Parameters</span><span class="sxs-lookup"><span data-stu-id="29ea3-126">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29ea3-127">-ResourceGroupName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="29ea3-128">-RunOn</span></span>
<span data-ttu-id="29ea3-129">Specifica il gruppo di lavoro ibrido su cui eseguire Runbook.</span><span class="sxs-lookup"><span data-stu-id="29ea3-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="29ea3-130">-Wait</span></span>
<span data-ttu-id="29ea3-131">Indica che il cmdlet attende che il processo venga completato, sospeso o fallito e quindi restituirà il controllo a Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="29ea3-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29ea3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29ea3-132">CommonParameters</span></span>
<span data-ttu-id="29ea3-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29ea3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29ea3-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29ea3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29ea3-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="29ea3-135">INPUTS</span></span>

### <span data-ttu-id="29ea3-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="29ea3-136">None</span></span>
<span data-ttu-id="29ea3-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="29ea3-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29ea3-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="29ea3-138">OUTPUTS</span></span>

### <span data-ttu-id="29ea3-139">Microsoft. Azure. Commands. Automation. Model. job</span><span class="sxs-lookup"><span data-stu-id="29ea3-139">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="29ea3-140">Questo cmdlet restituisce un oggetto **processo** , a meno che tu non specifichi il parametro _wait_ .</span><span class="sxs-lookup"><span data-stu-id="29ea3-140">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="29ea3-141">Se non specifichi _wait_ , Azure PowerShell restituirà immediatamente un oggetto **processo** .</span><span class="sxs-lookup"><span data-stu-id="29ea3-141">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="29ea3-142">Se si specifica _wait_ , Azure PowerShell completa il processo e quindi restituisce il risultato.</span><span class="sxs-lookup"><span data-stu-id="29ea3-142">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="29ea3-143">Il risultato non è un oggetto **processo** .</span><span class="sxs-lookup"><span data-stu-id="29ea3-143">The result is not a **Job** object.</span></span>

## <span data-ttu-id="29ea3-144">Note</span><span class="sxs-lookup"><span data-stu-id="29ea3-144">NOTES</span></span>

## <span data-ttu-id="29ea3-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="29ea3-145">RELATED LINKS</span></span>

[<span data-ttu-id="29ea3-146">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="29ea3-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="29ea3-148">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="29ea3-149">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="29ea3-150">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="29ea3-151">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="29ea3-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="29ea3-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="29ea3-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
