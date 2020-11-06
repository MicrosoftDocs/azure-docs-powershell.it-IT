---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: 47d384c6ca55fb428922dc3d9e59de84aa0db166
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507652"
---
# <span data-ttu-id="1e4fd-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4fd-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="1e4fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4fd-103">Modifica un webhook per un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e4fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e4fd-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1e4fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e4fd-105">DESCRIPTION</span></span>
<span data-ttu-id="1e4fd-106">Il cmdlet **set-AzureRmAutomationWebhook** modifica un webhook per un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="1e4fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e4fd-107">EXAMPLES</span></span>

### <span data-ttu-id="1e4fd-108">Esempio 1: disabilitare un webhook</span><span class="sxs-lookup"><span data-stu-id="1e4fd-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="1e4fd-109">Questo comando Disabilita un webhook denominato Webhook01 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="1e4fd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e4fd-110">PARAMETERS</span></span>

### <span data-ttu-id="1e4fd-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e4fd-111">-AutomationAccountName</span></span>
<span data-ttu-id="1e4fd-112">Specifica il nome di un account di automazione in cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="1e4fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4fd-113">-DefaultProfile</span></span>
<span data-ttu-id="1e4fd-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1e4fd-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4fd-115">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="1e4fd-115">-IsEnabled</span></span>
<span data-ttu-id="1e4fd-116">Specifica se il webhook è abilitato.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-116">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="1e4fd-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e4fd-117">-Name</span></span>
<span data-ttu-id="1e4fd-118">Specifica un nome del webhook che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-118">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1e4fd-119">-Parameters</span><span class="sxs-lookup"><span data-stu-id="1e4fd-119">-Parameters</span></span>
<span data-ttu-id="1e4fd-120">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-120">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="1e4fd-121">Le chiavi sono i nomi dei parametri Runbook.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-121">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="1e4fd-122">I valori sono i valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-122">The values are the runbook parameter values.</span></span>
<span data-ttu-id="1e4fd-123">Quando Runbook inizia in risposta a un webhook, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-123">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="1e4fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="1e4fd-125">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-125">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="1e4fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4fd-126">CommonParameters</span></span>
<span data-ttu-id="1e4fd-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4fd-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e4fd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4fd-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e4fd-129">INPUTS</span></span>

### <span data-ttu-id="1e4fd-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1e4fd-130">System.String</span></span>

### <span data-ttu-id="1e4fd-131">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1e4fd-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1e4fd-132">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="1e4fd-132">System.Collections.IDictionary</span></span>

## <span data-ttu-id="1e4fd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e4fd-133">OUTPUTS</span></span>

### <span data-ttu-id="1e4fd-134">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="1e4fd-134">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="1e4fd-135">Note</span><span class="sxs-lookup"><span data-stu-id="1e4fd-135">NOTES</span></span>

## <span data-ttu-id="1e4fd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e4fd-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e4fd-137">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4fd-137">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="1e4fd-138">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4fd-138">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="1e4fd-139">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="1e4fd-139">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


