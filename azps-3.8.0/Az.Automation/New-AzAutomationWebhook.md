---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationWebhook.md
ms.openlocfilehash: 88881e9ca5869bc2f63f4cec7c3993facc2cb3f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022909"
---
# <span data-ttu-id="21c66-101">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="21c66-101">New-AzAutomationWebhook</span></span>

## <span data-ttu-id="21c66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21c66-102">SYNOPSIS</span></span>
<span data-ttu-id="21c66-103">Crea un webhook per un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="21c66-103">Creates a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="21c66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21c66-104">SYNTAX</span></span>

```
New-AzAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21c66-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21c66-105">DESCRIPTION</span></span>
<span data-ttu-id="21c66-106">Il cmdlet **New-AzAutomationWebhook** crea un webhook per un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21c66-106">The **New-AzAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>
<span data-ttu-id="21c66-107">Assicurati di salvare l'URL del webhook restituito dal cmdlet, perché non può essere recuperato di nuovo.</span><span class="sxs-lookup"><span data-stu-id="21c66-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="21c66-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21c66-108">EXAMPLES</span></span>

### <span data-ttu-id="21c66-109">Esempio 1: creare un webhook</span><span class="sxs-lookup"><span data-stu-id="21c66-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="21c66-110">Questo comando crea un hook denominato Webhook06 per la runbook denominata ContosoRunbook nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="21c66-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="21c66-111">Il comando Archivia il webhook nella variabile $Webhook.</span><span class="sxs-lookup"><span data-stu-id="21c66-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="21c66-112">Il webhook è abilitato.</span><span class="sxs-lookup"><span data-stu-id="21c66-112">The webhook is enabled.</span></span>
<span data-ttu-id="21c66-113">Il webhook scade al momento specificato.</span><span class="sxs-lookup"><span data-stu-id="21c66-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="21c66-114">Questo comando non offre valori per i parametri webhook.</span><span class="sxs-lookup"><span data-stu-id="21c66-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="21c66-115">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="21c66-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="21c66-116">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="21c66-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="21c66-117">Esempio 2: creare un hook con i parametri</span><span class="sxs-lookup"><span data-stu-id="21c66-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="21c66-118">Il primo comando crea un dizionario di parametri e li archivia nella variabile $Params.</span><span class="sxs-lookup"><span data-stu-id="21c66-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="21c66-119">Il secondo comando crea un hook denominato Webhook11 per la runbook denominata ContosoRunbook nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="21c66-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="21c66-120">Il comando assegna i parametri in $Params al webhook.</span><span class="sxs-lookup"><span data-stu-id="21c66-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="21c66-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21c66-121">PARAMETERS</span></span>

### <span data-ttu-id="21c66-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="21c66-122">-AutomationAccountName</span></span>
<span data-ttu-id="21c66-123">Specifica il nome di un account di automazione in cui questo cmdlet crea un webhook.</span><span class="sxs-lookup"><span data-stu-id="21c66-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="21c66-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c66-124">-DefaultProfile</span></span>
<span data-ttu-id="21c66-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="21c66-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21c66-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="21c66-126">-ExpiryTime</span></span>
<span data-ttu-id="21c66-127">Specifica il tempo di scadenza per il webhook come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="21c66-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="21c66-128">Puoi specificare una stringa o un valore **DateTime** che può essere convertito in **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="21c66-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="21c66-129">-Force</span><span class="sxs-lookup"><span data-stu-id="21c66-129">-Force</span></span>
<span data-ttu-id="21c66-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="21c66-130">ps_force</span></span>

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

### <span data-ttu-id="21c66-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="21c66-131">-IsEnabled</span></span>
<span data-ttu-id="21c66-132">Specifica se il webhook è abilitato.</span><span class="sxs-lookup"><span data-stu-id="21c66-132">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="21c66-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="21c66-133">-Name</span></span>
<span data-ttu-id="21c66-134">Specifica un nome per il webhook.</span><span class="sxs-lookup"><span data-stu-id="21c66-134">Specifies a name for the webhook.</span></span>

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

### <span data-ttu-id="21c66-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="21c66-135">-Parameters</span></span>
<span data-ttu-id="21c66-136">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="21c66-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="21c66-137">Le chiavi sono i nomi dei parametri Runbook.</span><span class="sxs-lookup"><span data-stu-id="21c66-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="21c66-138">I valori sono i valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="21c66-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="21c66-139">Quando Runbook inizia in risposta a un webhook, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="21c66-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="21c66-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c66-140">-ResourceGroupName</span></span>
<span data-ttu-id="21c66-141">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un webhook.</span><span class="sxs-lookup"><span data-stu-id="21c66-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="21c66-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="21c66-142">-RunbookName</span></span>
<span data-ttu-id="21c66-143">Specifica il nome del Runbook da associare al webhook.</span><span class="sxs-lookup"><span data-stu-id="21c66-143">Specifies the name of the runbook to associate to the webhook.</span></span>

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

### <span data-ttu-id="21c66-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="21c66-144">-RunOn</span></span>
<span data-ttu-id="21c66-145">Nome facoltativo del gruppo di lavoratori ibridi che deve eseguire Runbook</span><span class="sxs-lookup"><span data-stu-id="21c66-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

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

### <span data-ttu-id="21c66-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="21c66-146">-Confirm</span></span>
<span data-ttu-id="21c66-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21c66-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21c66-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21c66-148">-WhatIf</span></span>
<span data-ttu-id="21c66-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21c66-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21c66-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21c66-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21c66-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c66-151">CommonParameters</span></span>
<span data-ttu-id="21c66-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21c66-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c66-153">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c66-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c66-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21c66-154">INPUTS</span></span>

### <span data-ttu-id="21c66-155">System. String</span><span class="sxs-lookup"><span data-stu-id="21c66-155">System.String</span></span>

### <span data-ttu-id="21c66-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="21c66-156">System.Boolean</span></span>

### <span data-ttu-id="21c66-157">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="21c66-157">System.DateTimeOffset</span></span>

## <span data-ttu-id="21c66-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21c66-158">OUTPUTS</span></span>

### <span data-ttu-id="21c66-159">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="21c66-159">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="21c66-160">Note</span><span class="sxs-lookup"><span data-stu-id="21c66-160">NOTES</span></span>

## <span data-ttu-id="21c66-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21c66-161">RELATED LINKS</span></span>

[<span data-ttu-id="21c66-162">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="21c66-162">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="21c66-163">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="21c66-163">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="21c66-164">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="21c66-164">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


