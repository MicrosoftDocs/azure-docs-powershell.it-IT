---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationWebhook.md
ms.openlocfilehash: ceca8c13b2cac0cc8685b1fa9fa3b26ab6017856
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202577"
---
# <span data-ttu-id="cf3bf-101">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf3bf-101">Get-AzAutomationWebhook</span></span>

## <span data-ttu-id="cf3bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf3bf-102">SYNOPSIS</span></span>
<span data-ttu-id="cf3bf-103">Ottiene i webhook dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-103">Gets webhooks from Automation.</span></span>

## <span data-ttu-id="cf3bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf3bf-104">SYNTAX</span></span>

### <span data-ttu-id="cf3bf-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cf3bf-105">ByAll (Default)</span></span>
```
Get-AzAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf3bf-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cf3bf-106">ByName</span></span>
```
Get-AzAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf3bf-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="cf3bf-107">ByRunbookName</span></span>
```
Get-AzAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf3bf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf3bf-108">DESCRIPTION</span></span>
<span data-ttu-id="cf3bf-109">Il cmdlet **Get-AzAutomationWebhook** ottiene i webhook.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-109">The **Get-AzAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="cf3bf-110">Per ottenere webhook specifici, specificare un nome webhook o specificare il nome di un Runbook di automazione di Azure per ottenere il collegamento a webhook.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="cf3bf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf3bf-111">EXAMPLES</span></span>

### <span data-ttu-id="cf3bf-112">Esempio 1: ottenere tutti i webhook per un Runbook</span><span class="sxs-lookup"><span data-stu-id="cf3bf-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="cf3bf-113">Questo comando ottiene tutti i webhook per un Runbook denominato Runbook03 nell'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="cf3bf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf3bf-114">PARAMETERS</span></span>

### <span data-ttu-id="cf3bf-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf3bf-115">-AutomationAccountName</span></span>
<span data-ttu-id="cf3bf-116">Specifica il nome di un account di automazione in cui questo cmdlet ottiene un webhook.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="cf3bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf3bf-117">-DefaultProfile</span></span>
<span data-ttu-id="cf3bf-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cf3bf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf3bf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf3bf-119">-Name</span></span>
<span data-ttu-id="cf3bf-120">Specifica il nome del webhook ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-120">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="cf3bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf3bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="cf3bf-122">Specifica il nome del gruppo di risorse per cui questo cmdlet ottiene i webhook.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-122">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="cf3bf-123">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="cf3bf-123">-RunbookName</span></span>
<span data-ttu-id="cf3bf-124">Specifica il nome di un Runbook per cui questo cmdlet ottiene i webhook.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-124">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="cf3bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf3bf-125">CommonParameters</span></span>
<span data-ttu-id="cf3bf-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf3bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf3bf-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf3bf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf3bf-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf3bf-128">INPUTS</span></span>

### <span data-ttu-id="cf3bf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cf3bf-129">System.String</span></span>

## <span data-ttu-id="cf3bf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf3bf-130">OUTPUTS</span></span>

### <span data-ttu-id="cf3bf-131">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="cf3bf-131">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="cf3bf-132">Note</span><span class="sxs-lookup"><span data-stu-id="cf3bf-132">NOTES</span></span>

## <span data-ttu-id="cf3bf-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf3bf-133">RELATED LINKS</span></span>

[<span data-ttu-id="cf3bf-134">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf3bf-134">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="cf3bf-135">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf3bf-135">Remove-AzAutomationWebhook</span></span>](./Remove-AzAutomationWebhook.md)

[<span data-ttu-id="cf3bf-136">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf3bf-136">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


