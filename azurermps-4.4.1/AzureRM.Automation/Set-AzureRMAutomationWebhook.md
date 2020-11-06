---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 9EA7F710-36FB-435C-BF28-1015E5D3155F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationWebhook.md
ms.openlocfilehash: b889a3b061556fc6c5ad4be1dfd118dac49f1f62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511359"
---
# <span data-ttu-id="a23f2-101">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a23f2-101">Set-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="a23f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a23f2-102">SYNOPSIS</span></span>
<span data-ttu-id="a23f2-103">Modifica un webhook per un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="a23f2-103">Modifies a webhook for an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a23f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a23f2-104">SYNTAX</span></span>

```
Set-AzureRmAutomationWebhook [-Name] <String> [-IsEnabled] <Boolean> [[-Parameters] <IDictionary>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a23f2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a23f2-105">DESCRIPTION</span></span>
<span data-ttu-id="a23f2-106">Il cmdlet **set-AzureRmAutomationWebhook** modifica un webhook per un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a23f2-106">The **Set-AzureRmAutomationWebhook** cmdlet modifies a webhook for an Azure Automation runbook.</span></span>

## <span data-ttu-id="a23f2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a23f2-107">EXAMPLES</span></span>

### <span data-ttu-id="a23f2-108">Esempio 1: disabilitare un webhook</span><span class="sxs-lookup"><span data-stu-id="a23f2-108">Example 1: Disable a webhook</span></span>
```
PS C:\>Set-AzureAutomationWebhook -Name "Webhook01" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -IsEnabled $False
```

<span data-ttu-id="a23f2-109">Questo comando Disabilita un webhook denominato Webhook01 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="a23f2-109">This command disables a webhook named Webhook01 in the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="a23f2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a23f2-110">PARAMETERS</span></span>

### <span data-ttu-id="a23f2-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a23f2-111">-AutomationAccountName</span></span>
<span data-ttu-id="a23f2-112">Specifica il nome di un account di automazione in cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="a23f2-112">Specifies the name of an Automation account in which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="a23f2-113">-IsEnabled</span><span class="sxs-lookup"><span data-stu-id="a23f2-113">-IsEnabled</span></span>
<span data-ttu-id="a23f2-114">Specifica se il webhook è abilitato.</span><span class="sxs-lookup"><span data-stu-id="a23f2-114">Specifies whether the webhook is enabled.</span></span>

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

### <span data-ttu-id="a23f2-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="a23f2-115">-Name</span></span>
<span data-ttu-id="a23f2-116">Specifica un nome del webhook che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="a23f2-116">Specifies a name of the webhook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a23f2-117">-Parameters</span><span class="sxs-lookup"><span data-stu-id="a23f2-117">-Parameters</span></span>
<span data-ttu-id="a23f2-118">Specifica un dizionario di coppie chiave/valore.</span><span class="sxs-lookup"><span data-stu-id="a23f2-118">Specifies a dictionary of key/value pairs.</span></span>
<span data-ttu-id="a23f2-119">Le chiavi sono i nomi dei parametri Runbook.</span><span class="sxs-lookup"><span data-stu-id="a23f2-119">The keys are the runbook parameter names.</span></span>
<span data-ttu-id="a23f2-120">I valori sono i valori di parametro Runbook.</span><span class="sxs-lookup"><span data-stu-id="a23f2-120">The values are the runbook parameter values.</span></span>
<span data-ttu-id="a23f2-121">Quando Runbook inizia in risposta a un webhook, questi parametri vengono passati a Runbook.</span><span class="sxs-lookup"><span data-stu-id="a23f2-121">When the runbook starts in response to a webhook, these parameters are passed to the runbook.</span></span>

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

### <span data-ttu-id="a23f2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a23f2-122">-ResourceGroupName</span></span>
<span data-ttu-id="a23f2-123">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica un webhook.</span><span class="sxs-lookup"><span data-stu-id="a23f2-123">Specifies the name of the resource group for which this cmdlet modifies a webhook.</span></span>

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

### <span data-ttu-id="a23f2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23f2-124">-DefaultProfile</span></span>
<span data-ttu-id="a23f2-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a23f2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a23f2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23f2-126">CommonParameters</span></span>
<span data-ttu-id="a23f2-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a23f2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23f2-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a23f2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23f2-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a23f2-129">INPUTS</span></span>

## <span data-ttu-id="a23f2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a23f2-130">OUTPUTS</span></span>

### <span data-ttu-id="a23f2-131">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="a23f2-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="a23f2-132">Note</span><span class="sxs-lookup"><span data-stu-id="a23f2-132">NOTES</span></span>

## <span data-ttu-id="a23f2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a23f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="a23f2-134">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a23f2-134">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="a23f2-135">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a23f2-135">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="a23f2-136">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="a23f2-136">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)


