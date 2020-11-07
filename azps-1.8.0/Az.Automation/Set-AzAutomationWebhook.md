---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationWebhook.md
ms.openlocfilehash: 39e0fda02eb41ed591562d9cfc1f7902fa43c38a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684954"
---
# <span data-ttu-id="36065-101">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="36065-101">Set-AzAutomationWebhook</span></span>

## <span data-ttu-id="36065-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36065-102">SYNOPSIS</span></span>
<span data-ttu-id="36065-103">Modifica un webhook per un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="36065-103">Modifies a webhook for an Automation runbook.</span></span>

## <span data-ttu-id="36065-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36065-104">SYNTAX</span></span>

```
Set-AzAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36065-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36065-105">DESCRIPTION</span></span>
<span data-ttu-id="36065-106">Il cmdlet **set-AzAutomationWebhook** modifica un webhook per un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="36065-106">The **Set-AzAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="36065-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36065-107">EXAMPLES</span></span>

### <span data-ttu-id="36065-108">Esempio 1: disabilitare un webhook</span><span class="sxs-lookup"><span data-stu-id="36065-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="36065-109">Questo comando Disabilita un webhook denominato Webhook01 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="36065-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="36065-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36065-110">PARAMETERS</span></span>

### <span data-ttu-id="36065-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="36065-111">-AutomationAccountName</span></span>
<span data-ttu-id="36065-112">Specifica il nome di un account di automazione in cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="36065-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="36065-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36065-113">-DefaultProfile</span></span>
<span data-ttu-id="36065-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="36065-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36065-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="36065-115">-IsEnabled</span></span>
<span data-ttu-id="36065-116">Specifica se il webhook è abilitato.</span><span class="sxs-lookup"><span data-stu-id="36065-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="36065-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="36065-117">-Name</span></span>
<span data-ttu-id="36065-118">Specifica un nome del webhook che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="36065-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="36065-119">-Parameters</span><span class="sxs-lookup"><span data-stu-id="36065-119">-Parameters</span></span>
<span data-ttu-id="36065-120">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="36065-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="36065-121">Le chiavi sono i nomi dei parametri Runbook.</span><span class="sxs-lookup"><span data-stu-id="36065-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="36065-122">I valori sono i valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="36065-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="36065-123">Quando Runbook inizia in risposta a un webhook, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="36065-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="36065-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36065-124">-ResourceGroupName</span></span>
<span data-ttu-id="36065-125">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="36065-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="36065-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36065-126">CommonParameters</span></span>
<span data-ttu-id="36065-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36065-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36065-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36065-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36065-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36065-129">INPUTS</span></span>

### <span data-ttu-id="36065-130">System. String</span><span class="sxs-lookup"><span data-stu-id="36065-130">System.String</span></span>

### <span data-ttu-id="36065-131">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="36065-131">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="36065-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="36065-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="36065-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36065-133">OUTPUTS</span></span>

### <span data-ttu-id="36065-134">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="36065-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="36065-135">Note</span><span class="sxs-lookup"><span data-stu-id="36065-135">NOTES</span></span>

## <span data-ttu-id="36065-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36065-136">RELATED LINKS</span></span>

[<span data-ttu-id="36065-137">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="36065-137">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="36065-138">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="36065-138">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="36065-139">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="36065-139">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)


