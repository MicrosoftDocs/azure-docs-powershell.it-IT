---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 0c1f2e5135596dd0911b02414d35b15c824b7936
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182110"
---
# <span data-ttu-id="fbfc1-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fbfc1-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="fbfc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbfc1-102">SYNOPSIS</span></span>
<span data-ttu-id="fbfc1-103">Modifica un webhook per un runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="fbfc1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbfc1-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fbfc1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fbfc1-105">DESCRIPTION</span></span>
<span data-ttu-id="fbfc1-106">Il cmdlet **Set-AzAutomationWebhook** modifica un webhook per un runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="fbfc1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbfc1-107">EXAMPLES</span></span>

### <span data-ttu-id="fbfc1-108">Esempio 1: Disabilitare un webhook</span><span class="sxs-lookup"><span data-stu-id="fbfc1-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="fbfc1-109">Questo comando disabilita un webhook denominato Webhook01 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="fbfc1-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fbfc1-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="fbfc1-111">Questo comando imposta il valore eseguito sul webhook e forza l'esecuzione del runbook in un gruppo di utenti ibridi denominato Windows.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="fbfc1-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="fbfc1-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="fbfc1-113">Questo comando aggiorna il valore eseguito sul webhook e forza l'esecuzione del runbook in un runbook di Azure.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="fbfc1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbfc1-114">PARAMETERS</span></span>

### <span data-ttu-id="fbfc1-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fbfc1-115">-AutomationAccountName</span></span>
<span data-ttu-id="fbfc1-116">Specifica il nome di un account di automazione in cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="fbfc1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbfc1-117">-DefaultProfile</span></span>
<span data-ttu-id="fbfc1-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="fbfc1-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbfc1-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="fbfc1-119">-IsEnabled</span></span>
<span data-ttu-id="fbfc1-120">Specifica se la webhook è abilitata.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-120">Specifies whether the webhook is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfc1-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fbfc1-121">-Name</span></span>
<span data-ttu-id="fbfc1-122">Specifica un nome del webhook modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="fbfc1-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="fbfc1-123">-Parameters</span></span>
<span data-ttu-id="fbfc1-124">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="fbfc1-125">Le chiavi sono i nomi dei parametri del runbook.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="fbfc1-126">I valori sono i valori dei parametri del runbook.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="fbfc1-127">Quando il runbook viene avviato in risposta a un webhook, questi parametri vengono passati al runbook.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbfc1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbfc1-128">-ResourceGroupName</span></span>
<span data-ttu-id="fbfc1-129">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="fbfc1-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="fbfc1-130">-RunOn</span></span>
<span data-ttu-id="fbfc1-131">Nome facoltativo dell'agente ibrido che deve eseguire il runbook</span><span class="sxs-lookup"><span data-stu-id="fbfc1-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="fbfc1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbfc1-132">CommonParameters</span></span>
<span data-ttu-id="fbfc1-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbfc1-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fbfc1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbfc1-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="fbfc1-135">INPUTS</span></span>

### <span data-ttu-id="fbfc1-136">System.String</span><span class="sxs-lookup"><span data-stu-id="fbfc1-136">System.String</span></span>

### <span data-ttu-id="fbfc1-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fbfc1-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fbfc1-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="fbfc1-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="fbfc1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbfc1-139">OUTPUTS</span></span>

### <span data-ttu-id="fbfc1-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="fbfc1-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="fbfc1-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="fbfc1-141">NOTES</span></span>

## <span data-ttu-id="fbfc1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbfc1-142">RELATED LINKS</span></span>

[<span data-ttu-id="fbfc1-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fbfc1-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="fbfc1-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fbfc1-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="fbfc1-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="fbfc1-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


