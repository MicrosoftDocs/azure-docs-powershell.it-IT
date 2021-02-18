---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200998"
---
# <span data-ttu-id="a4f77-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a4f77-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="a4f77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4f77-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f77-103">Crea un webhook per un runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="a4f77-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="a4f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a4f77-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f77-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a4f77-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f77-106">Il cmdlet **New-AzAutomationWebhook** crea un webhook per un runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f77-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="a4f77-107">Assicurarsi di salvare l'URL webhook restituito dal cmdlet, perché non può essere recuperato di nuovo.</span><span class="sxs-lookup"><span data-stu-id="a4f77-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="a4f77-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a4f77-108">EXAMPLES</span></span>

### <span data-ttu-id="a4f77-109">Esempio 1: Creare un webhook</span><span class="sxs-lookup"><span data-stu-id="a4f77-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a4f77-110">Questo comando crea un webhook denominato Webhook06 per il runbook denominato ContosoRunbook nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a4f77-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a4f77-111">Il comando archivia il webhook nella variabile $Webhook variabile.</span><span class="sxs-lookup"><span data-stu-id="a4f77-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="a4f77-112">La webhook è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a4f77-112">The webhook is enabled.</span></span>
<span data-ttu-id="a4f77-113">Il webhook scade all'ora specificata.</span><span class="sxs-lookup"><span data-stu-id="a4f77-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="a4f77-114">Questo comando non fornisce alcun valore per i parametri webhook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="a4f77-115">Questo comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="a4f77-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="a4f77-116">Di conseguenza, non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="a4f77-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="a4f77-117">Esempio 2: Creare un webhook con parametri</span><span class="sxs-lookup"><span data-stu-id="a4f77-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="a4f77-118">Il primo comando crea un dizionario di parametri e li archivia nella $Params variabile.</span><span class="sxs-lookup"><span data-stu-id="a4f77-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="a4f77-119">Il secondo comando crea un webhook denominato Webhook11 per il runbook denominato ContosoRunbook nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a4f77-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="a4f77-120">Il comando assegna i parametri in $Params al webhook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="a4f77-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4f77-121">PARAMETERS</span></span>

### <span data-ttu-id="a4f77-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a4f77-122">-AutomationAccountName</span></span>
<span data-ttu-id="a4f77-123">Specifica il nome di un account di automazione in cui questo cmdlet crea un webhook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="a4f77-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f77-124">-DefaultProfile</span></span>
<span data-ttu-id="a4f77-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="a4f77-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a4f77-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="a4f77-126">-ExpiryTime</span></span>
<span data-ttu-id="a4f77-127">Specifica la data di scadenza per il webhook come **oggetto DateTimeObject.**</span><span class="sxs-lookup"><span data-stu-id="a4f77-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="a4f77-128">È possibile specificare una stringa o **un valore DateTime** che può essere convertito in un valore **DateTime Offset valido.**</span><span class="sxs-lookup"><span data-stu-id="a4f77-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a4f77-129">-Force</span></span>
<span data-ttu-id="a4f77-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="a4f77-130">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a4f77-131">-IsEnabled</span></span>
<span data-ttu-id="a4f77-132">Specifica se la webhook è abilitata.</span><span class="sxs-lookup"><span data-stu-id="a4f77-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-133">-Name</span><span class="sxs-lookup"><span data-stu-id="a4f77-133">-Name</span></span>
<span data-ttu-id="a4f77-134">Specifica un nome per il webhook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-134">Specifies a name for the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="a4f77-135">-Parameters</span></span>
<span data-ttu-id="a4f77-136">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="a4f77-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="a4f77-137">Le chiavi sono i nomi dei parametri del runbook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="a4f77-138">I valori sono i valori dei parametri del runbook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="a4f77-139">Quando il runbook viene avviato in risposta a un webhook, questi parametri vengono passati al runbook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4f77-140">-ResourceGroupName</span></span>
<span data-ttu-id="a4f77-141">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un webhook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="a4f77-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="a4f77-142">-RunbookName</span></span>
<span data-ttu-id="a4f77-143">Specifica il nome del runbook da associare al webhook.</span><span class="sxs-lookup"><span data-stu-id="a4f77-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="a4f77-144">-RunOn</span></span>
<span data-ttu-id="a4f77-145">Nome facoltativo del gruppo di utenti ibridi che deve eseguire il runbook</span><span class="sxs-lookup"><span data-stu-id="a4f77-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4f77-146">-Confirm</span></span>
<span data-ttu-id="a4f77-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f77-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f77-148">-WhatIf</span></span>
<span data-ttu-id="a4f77-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4f77-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4f77-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a4f77-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4f77-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f77-151">CommonParameters</span></span>
<span data-ttu-id="a4f77-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f77-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f77-153">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f77-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f77-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="a4f77-154">INPUTS</span></span>

### <span data-ttu-id="a4f77-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a4f77-155">System.String</span></span>

### <span data-ttu-id="a4f77-156">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a4f77-156">System.Boolean</span></span>

### <span data-ttu-id="a4f77-157">System.DateTime Offset</span><span class="sxs-lookup"><span data-stu-id="a4f77-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="a4f77-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a4f77-158">OUTPUTS</span></span>

### <span data-ttu-id="a4f77-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="a4f77-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="a4f77-160">NOTE</span><span class="sxs-lookup"><span data-stu-id="a4f77-160">NOTES</span></span>

## <span data-ttu-id="a4f77-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a4f77-161">RELATED LINKS</span></span>

[<span data-ttu-id="a4f77-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a4f77-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="a4f77-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a4f77-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="a4f77-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a4f77-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


