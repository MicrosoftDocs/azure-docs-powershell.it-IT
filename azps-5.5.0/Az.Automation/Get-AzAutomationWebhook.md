---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201135"
---
# <span data-ttu-id="40e4f-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="40e4f-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="40e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="40e4f-103">Recupera gli webhook dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="40e4f-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="40e4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40e4f-104">SYNTAX</span></span>

### <span data-ttu-id="40e4f-105">Pertutti (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40e4f-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40e4f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="40e4f-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40e4f-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="40e4f-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40e4f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="40e4f-108">DESCRIPTION</span></span>
<span data-ttu-id="40e4f-109">Il cmdlet **Get-AzAutomationWebhook** ottiene webhook.</span><span class="sxs-lookup"><span data-stu-id="40e4f-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="40e4f-110">Per ottenere webhook specifici, specificare un nome di webhook o specificare il nome di un runbook di automazione di Azure per collegarsi ai webhook.</span><span class="sxs-lookup"><span data-stu-id="40e4f-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="40e4f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40e4f-111">EXAMPLES</span></span>

### <span data-ttu-id="40e4f-112">Esempio 1: Ottenere tutti gli webhook per un runbook</span><span class="sxs-lookup"><span data-stu-id="40e4f-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="40e4f-113">Questo comando recupera tutti gli webhook per un runbook denominato Runbook03 nell'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="40e4f-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="40e4f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40e4f-114">PARAMETERS</span></span>

### <span data-ttu-id="40e4f-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="40e4f-115">-AutomationAccountName</span></span>
<span data-ttu-id="40e4f-116">Specifica il nome di un account di automazione in cui questo cmdlet ottiene un webhook.</span><span class="sxs-lookup"><span data-stu-id="40e4f-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="40e4f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e4f-117">-DefaultProfile</span></span>
<span data-ttu-id="40e4f-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="40e4f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40e4f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="40e4f-119">-Name</span></span>
<span data-ttu-id="40e4f-120">Specifica il nome del webhook che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40e4f-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="40e4f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40e4f-121">-ResourceGroupName</span></span>
<span data-ttu-id="40e4f-122">Specifica il nome del gruppo di risorse per cui questo cmdlet ottiene gli webhook.</span><span class="sxs-lookup"><span data-stu-id="40e4f-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="40e4f-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="40e4f-123">-RunbookName</span></span>
<span data-ttu-id="40e4f-124">Specifica il nome di un runbook per cui questo cmdlet ottiene webhook.</span><span class="sxs-lookup"><span data-stu-id="40e4f-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="40e4f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e4f-125">CommonParameters</span></span>
<span data-ttu-id="40e4f-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40e4f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e4f-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e4f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e4f-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="40e4f-128">INPUTS</span></span>

### <span data-ttu-id="40e4f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="40e4f-129">System.String</span></span>

## <span data-ttu-id="40e4f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40e4f-130">OUTPUTS</span></span>

### <span data-ttu-id="40e4f-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span><span class="sxs-lookup"><span data-stu-id="40e4f-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="40e4f-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="40e4f-132">NOTES</span></span>

## <span data-ttu-id="40e4f-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40e4f-133">RELATED LINKS</span></span>

[<span data-ttu-id="40e4f-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="40e4f-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="40e4f-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="40e4f-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="40e4f-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="40e4f-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


