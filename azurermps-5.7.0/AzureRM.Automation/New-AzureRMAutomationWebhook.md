---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: E1FC931E-4EB8-4DCA-92BD-8013DDC13219
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationWebhook.md
ms.openlocfilehash: 417ab3f7f787a76041caceebbfcf32f9733717b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521464"
---
# <span data-ttu-id="28b0d-101">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="28b0d-101">New-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="28b0d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="28b0d-103">Crea un webhook per un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="28b0d-103">Creates a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28b0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28b0d-104">SYNTAX</span></span>

```
New-AzureRmAutomationWebhook [-Name] <String> [-RunbookName] <String> [-IsEnabled] <Boolean>
 [-ExpiryTime] <DateTimeOffset> [-Parameters <IDictionary>] [-Force] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28b0d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28b0d-105">DESCRIPTION</span></span>
<span data-ttu-id="28b0d-106">Il cmdlet **New-AzureRmAutomationWebhook** crea un webhook per un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="28b0d-106">The **New-AzureRmAutomationWebhook** cmdlet creates a webhook for an Azure Automation runbook.</span></span>

<span data-ttu-id="28b0d-107">Assicurati di salvare l'URL del webhook restituito dal cmdlet, perché non può essere recuperato di nuovo.</span><span class="sxs-lookup"><span data-stu-id="28b0d-107">Be sure to save the webhook URL that this cmdlet returns, because it cannot be retrieved again.</span></span>

## <span data-ttu-id="28b0d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28b0d-108">EXAMPLES</span></span>

### <span data-ttu-id="28b0d-109">Esempio 1: creare un webhook</span><span class="sxs-lookup"><span data-stu-id="28b0d-109">Example 1: Create a webhook</span></span>
```
PS C:\>$Webhook = New-AzureRmAutomationWebhook -Name "Webhook06" -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="28b0d-110">Questo comando crea un hook denominato Webhook06 per la runbook denominata ContosoRunbook nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="28b0d-110">This command creates a webhook named Webhook06 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="28b0d-111">Il comando Archivia il webhook nella variabile $Webhook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-111">The command stores the webhook in the $Webhook variable.</span></span>
<span data-ttu-id="28b0d-112">Il webhook è abilitato.</span><span class="sxs-lookup"><span data-stu-id="28b0d-112">The webhook is enabled.</span></span>
<span data-ttu-id="28b0d-113">Il webhook scade al momento specificato.</span><span class="sxs-lookup"><span data-stu-id="28b0d-113">The webhook expires at the specified time.</span></span>
<span data-ttu-id="28b0d-114">Questo comando non offre valori per i parametri webhook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-114">This command does not provide any values for webhook parameters.</span></span>
<span data-ttu-id="28b0d-115">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="28b0d-115">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="28b0d-116">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="28b0d-116">Therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="28b0d-117">Esempio 2: creare un hook con i parametri</span><span class="sxs-lookup"><span data-stu-id="28b0d-117">Example 2: Create a webhook with parameters</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> $Webhook = New-AzureRmAutomationWebhook -Name "Webhook11" -Parameters $Params -IsEnabled $True -ExpiryTime "10/2/2016" -RunbookName "ContosoRunbook" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="28b0d-118">Il primo comando crea un dizionario di parametri e li archivia nella variabile $Params.</span><span class="sxs-lookup"><span data-stu-id="28b0d-118">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="28b0d-119">Il secondo comando crea un hook denominato Webhook11 per la runbook denominata ContosoRunbook nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="28b0d-119">The second command creates a webhook named Webhook11 for the runbook named ContosoRunbook in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="28b0d-120">Il comando assegna i parametri in $Params al webhook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-120">The command assigns the parameters in $Params to the webhook.</span></span>

## <span data-ttu-id="28b0d-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28b0d-121">PARAMETERS</span></span>

### <span data-ttu-id="28b0d-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="28b0d-122">-AutomationAccountName</span></span>
<span data-ttu-id="28b0d-123">Specifica il nome di un account di automazione in cui questo cmdlet crea un webhook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-123">Specifies the name of an Automation account in which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="28b0d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28b0d-124">-DefaultProfile</span></span>
<span data-ttu-id="28b0d-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="28b0d-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28b0d-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="28b0d-126">-ExpiryTime</span></span>
<span data-ttu-id="28b0d-127">Specifica il tempo di scadenza per il webhook come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="28b0d-127">Specifies the expiry time for the webhook as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="28b0d-128">Puoi specificare una stringa o un valore **DateTime** che può essere convertito in **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="28b0d-128">You can specify a string or a **DateTime** that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-129">-Force</span><span class="sxs-lookup"><span data-stu-id="28b0d-129">-Force</span></span>
<span data-ttu-id="28b0d-130">ps_force</span><span class="sxs-lookup"><span data-stu-id="28b0d-130">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-131">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="28b0d-131">-IsEnabled</span></span>
<span data-ttu-id="28b0d-132">Specifica se il webhook è abilitato.</span><span class="sxs-lookup"><span data-stu-id="28b0d-132">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="28b0d-133">-Name</span></span>
<span data-ttu-id="28b0d-134">Specifica un nome per il webhook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-134">Specifies a name for the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-135">-Parameters</span><span class="sxs-lookup"><span data-stu-id="28b0d-135">-Parameters</span></span>
<span data-ttu-id="28b0d-136">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="28b0d-136">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="28b0d-137">Le chiavi sono i nomi dei parametri Runbook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-137">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="28b0d-138">I valori sono i valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-138">The values are the runbook parameter values.</span></span>
<span data-ttu-id="28b0d-139">Quando Runbook inizia in risposta a un webhook, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-139">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="28b0d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28b0d-140">-ResourceGroupName</span></span>
<span data-ttu-id="28b0d-141">Specifica il nome del gruppo di risorse per cui questo cmdlet crea un webhook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-141">Specifies the name of the resource group for which this cmdlet creates a webhook.</span></span>

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

### <span data-ttu-id="28b0d-142">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="28b0d-142">-RunbookName</span></span>
<span data-ttu-id="28b0d-143">Specifica il nome del Runbook da associare al webhook.</span><span class="sxs-lookup"><span data-stu-id="28b0d-143">Specifies the name of the runbook to associate to the webhook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-144">-RunOn</span><span class="sxs-lookup"><span data-stu-id="28b0d-144">-RunOn</span></span>
<span data-ttu-id="28b0d-145">Nome facoltativo del gruppo di lavoratori ibridi che deve eseguire Runbook</span><span class="sxs-lookup"><span data-stu-id="28b0d-145">Optional name of the hybrid worker group which should execute the runbook</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28b0d-146">-Confirm</span></span>
<span data-ttu-id="28b0d-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28b0d-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28b0d-148">-WhatIf</span></span>
<span data-ttu-id="28b0d-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28b0d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28b0d-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28b0d-150">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28b0d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28b0d-151">CommonParameters</span></span>
<span data-ttu-id="28b0d-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28b0d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28b0d-153">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28b0d-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28b0d-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28b0d-154">INPUTS</span></span>

### <span data-ttu-id="28b0d-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28b0d-155">None</span></span>
<span data-ttu-id="28b0d-156">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="28b0d-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="28b0d-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28b0d-157">OUTPUTS</span></span>

### <span data-ttu-id="28b0d-158">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="28b0d-158">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="28b0d-159">Note</span><span class="sxs-lookup"><span data-stu-id="28b0d-159">NOTES</span></span>

## <span data-ttu-id="28b0d-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28b0d-160">RELATED LINKS</span></span>

[<span data-ttu-id="28b0d-161">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="28b0d-161">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="28b0d-162">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="28b0d-162">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="28b0d-163">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="28b0d-163">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


