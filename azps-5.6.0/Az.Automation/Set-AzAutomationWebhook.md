---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 200cc0b6312940606bb4e75f576c60928a84b33f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009805"
---
# <span data-ttu-id="b625a-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b625a-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="b625a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b625a-102">SYNOPSIS</span></span>
<span data-ttu-id="b625a-103">Modifica un webhook per un runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="b625a-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="b625a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b625a-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b625a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b625a-105">DESCRIPTION</span></span>
<span data-ttu-id="b625a-106">Il cmdlet **Set-AzAutomationWebhook** modifica un webhook per un runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="b625a-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="b625a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b625a-107">EXAMPLES</span></span>

### <span data-ttu-id="b625a-108">Esempio 1: Disabilitare un webhook</span><span class="sxs-lookup"><span data-stu-id="b625a-108">Example 1: Disable a webhook</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="b625a-109">Questo comando disabilita un webhook denominato Webhook01 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="b625a-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="b625a-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b625a-110">Example 2</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn 'Windows'
```

<span data-ttu-id="b625a-111">Questo comando imposta il valore eseguito sul webhook e forza l'esecuzione del runbook in un gruppo di utenti ibridi denominato Windows.</span><span class="sxs-lookup"><span data-stu-id="b625a-111">This command sets the run on value for the webhook and forces the runbook to be run on a Hybrid Worker group called Windows.</span></span>

### <span data-ttu-id="b625a-112">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b625a-112">Example 3</span></span>
```powershell
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -RunOn $null
```

<span data-ttu-id="b625a-113">Questo comando aggiorna il valore eseguito sul webhook e forza l'esecuzione del runbook in un runbook di Azure.</span><span class="sxs-lookup"><span data-stu-id="b625a-113">This command updates the run on value for the webhook and forces the runbook to be run on an Azure runbook worker.</span></span> 

## <span data-ttu-id="b625a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b625a-114">PARAMETERS</span></span>

### <span data-ttu-id="b625a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b625a-115">-AutomationAccountName</span></span>
<span data-ttu-id="b625a-116">Specifica il nome di un account di automazione in cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="b625a-116">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="b625a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b625a-117">-DefaultProfile</span></span>
<span data-ttu-id="b625a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b625a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b625a-119">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="b625a-119">-IsEnabled</span></span>
<span data-ttu-id="b625a-120">Specifica se la webhook è abilitata.</span><span class="sxs-lookup"><span data-stu-id="b625a-120">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="b625a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="b625a-121">-Name</span></span>
<span data-ttu-id="b625a-122">Specifica un nome del webhook modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b625a-122">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b625a-123">-Parameters</span><span class="sxs-lookup"><span data-stu-id="b625a-123">-Parameters</span></span>
<span data-ttu-id="b625a-124">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="b625a-124">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="b625a-125">Le chiavi sono i nomi dei parametri del runbook.</span><span class="sxs-lookup"><span data-stu-id="b625a-125">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="b625a-126">I valori sono i valori dei parametri del runbook.</span><span class="sxs-lookup"><span data-stu-id="b625a-126">The values are the runbook parameter values.</span></span>
<span data-ttu-id="b625a-127">Quando il runbook viene avviato in risposta a un webhook, questi parametri vengono passati al runbook.</span><span class="sxs-lookup"><span data-stu-id="b625a-127">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="b625a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b625a-128">-ResourceGroupName</span></span>
<span data-ttu-id="b625a-129">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="b625a-129">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="b625a-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="b625a-130">-RunOn</span></span>
<span data-ttu-id="b625a-131">Nome facoltativo dell'agente ibrido che deve eseguire il runbook</span><span class="sxs-lookup"><span data-stu-id="b625a-131">Optional name of the hybrid agent which should execute the runbook</span></span>

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

### <span data-ttu-id="b625a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b625a-132">CommonParameters</span></span>
<span data-ttu-id="b625a-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b625a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b625a-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b625a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b625a-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="b625a-135">INPUTS</span></span>

### <span data-ttu-id="b625a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b625a-136">System.String</span></span>

### <span data-ttu-id="b625a-137">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b625a-137">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b625a-138">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="b625a-138">System.Collections.IDictionary</span></span>

## <span data-ttu-id="b625a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b625a-139">OUTPUTS</span></span>

### <span data-ttu-id="b625a-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="b625a-140">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="b625a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="b625a-141">NOTES</span></span>

## <span data-ttu-id="b625a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b625a-142">RELATED LINKS</span></span>

[<span data-ttu-id="b625a-143">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b625a-143">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="b625a-144">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b625a-144">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="b625a-145">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="b625a-145">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


