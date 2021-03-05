---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: 00125a7ad3d74d3e710b782d0be7fdb20004ef4a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014110"
---
# <span data-ttu-id="65009-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="65009-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="65009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65009-102">SYNOPSIS</span></span>
<span data-ttu-id="65009-103">Recupera gli webhook dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="65009-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="65009-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="65009-104">SYNTAX</span></span>

### <span data-ttu-id="65009-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="65009-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65009-106">ByName</span><span class="sxs-lookup"><span data-stu-id="65009-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65009-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="65009-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65009-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="65009-108">DESCRIPTION</span></span>
<span data-ttu-id="65009-109">Il cmdlet **Get-AzAutomationWebhook** ottiene webhook.</span><span class="sxs-lookup"><span data-stu-id="65009-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="65009-110">Per ottenere webhook specifici, specificare un nome di webhook o specificare il nome di un runbook di automazione di Azure per collegarsi ai webhook.</span><span class="sxs-lookup"><span data-stu-id="65009-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span><br>
<span data-ttu-id="65009-111">**Nota:** WebhookUri viene restituito come stringa vuota per motivi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="65009-111">**Note:** The WebhookUri is returned as empty string due to security concerns.</span></span> <span data-ttu-id="65009-112">Assicurarsi di salvare l'URL Webhook restituito dal cmdlet **New-AzAutomationWebhook,** perché non può essere recuperato con **Get-AzAutomationWebhook.**</span><span class="sxs-lookup"><span data-stu-id="65009-112">Please make sure to save the webhook URL that **New-AzAutomationWebhook** cmdlet returns, because it cannot be retrieved by using **Get-AzAutomationWebhook**.</span></span>

## <span data-ttu-id="65009-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="65009-113">EXAMPLES</span></span>

### <span data-ttu-id="65009-114">Esempio 1: Ottenere tutti gli webhook per un runbook</span><span class="sxs-lookup"><span data-stu-id="65009-114">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="65009-115">Questo comando recupera tutti gli webhook per un runbook denominato Runbook03 nell'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="65009-115">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="65009-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65009-116">PARAMETERS</span></span>

### <span data-ttu-id="65009-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="65009-117">-AutomationAccountName</span></span>
<span data-ttu-id="65009-118">Specifica il nome di un account di automazione in cui questo cmdlet ottiene un webhook.</span><span class="sxs-lookup"><span data-stu-id="65009-118">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="65009-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65009-119">-DefaultProfile</span></span>
<span data-ttu-id="65009-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="65009-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65009-121">-Name</span><span class="sxs-lookup"><span data-stu-id="65009-121">-Name</span></span>
<span data-ttu-id="65009-122">Specifica il nome del webhook che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65009-122">Specifies the name of the webhook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: WebhookName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65009-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65009-123">-ResourceGroupName</span></span>
<span data-ttu-id="65009-124">Specifica il nome del gruppo di risorse per cui questo cmdlet ottiene gli webhook.</span><span class="sxs-lookup"><span data-stu-id="65009-124">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="65009-125">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="65009-125">-RunbookName</span></span>
<span data-ttu-id="65009-126">Specifica il nome di un runbook per cui questo cmdlet ottiene webhook.</span><span class="sxs-lookup"><span data-stu-id="65009-126">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65009-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65009-127">CommonParameters</span></span>
<span data-ttu-id="65009-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65009-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65009-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65009-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65009-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="65009-130">INPUTS</span></span>

### <span data-ttu-id="65009-131">System.String</span><span class="sxs-lookup"><span data-stu-id="65009-131">System.String</span></span>

## <span data-ttu-id="65009-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="65009-132">OUTPUTS</span></span>

### <span data-ttu-id="65009-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="65009-133">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="65009-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="65009-134">NOTES</span></span>

## <span data-ttu-id="65009-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="65009-135">RELATED LINKS</span></span>

[<span data-ttu-id="65009-136">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="65009-136">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="65009-137">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="65009-137">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="65009-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="65009-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


