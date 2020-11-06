---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A0A956E9-6C4F-4432-A39F-A180CD519C04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationWebhook.md
ms.openlocfilehash: 1868f7995a8e3f426f8e4657f9e6df638f06662e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519643"
---
# <span data-ttu-id="c044d-101">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c044d-101">Get-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="c044d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c044d-102">SYNOPSIS</span></span>
<span data-ttu-id="c044d-103">Ottiene i webhook dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="c044d-103">Gets webhooks from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c044d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c044d-104">SYNTAX</span></span>

### <span data-ttu-id="c044d-105">ByAll (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c044d-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationWebhook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c044d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c044d-106">ByName</span></span>
```
Get-AzureRmAutomationWebhook -Name <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c044d-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="c044d-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationWebhook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c044d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c044d-108">DESCRIPTION</span></span>
<span data-ttu-id="c044d-109">Il cmdlet **Get-AzureRmAutomationWebhook** ottiene i webhook.</span><span class="sxs-lookup"><span data-stu-id="c044d-109">The **Get-AzureRmAutomationWebhook** cmdlet gets webhooks.</span></span>
<span data-ttu-id="c044d-110">Per ottenere webhook specifici, specificare un nome webhook o specificare il nome di un Runbook di automazione di Azure per ottenere il collegamento a webhook.</span><span class="sxs-lookup"><span data-stu-id="c044d-110">To get specific webhooks, specify a webhook name or specify the name of an Azure Automation runbook to get the webhooks connected to it.</span></span>

## <span data-ttu-id="c044d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c044d-111">EXAMPLES</span></span>

### <span data-ttu-id="c044d-112">Esempio 1: ottenere tutti i webhook per un Runbook</span><span class="sxs-lookup"><span data-stu-id="c044d-112">Example 1: Get all webhooks for a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationWebhook -RunbookName "Runbook03" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01"
```

<span data-ttu-id="c044d-113">Questo comando ottiene tutti i webhook per un Runbook denominato Runbook03 nell'account di automazione denominato AutomationAccount01 nel gruppo di risorse denominato ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c044d-113">This command gets all webhooks for a runbook named Runbook03 in the Automation account named AutomationAccount01 in the resource group named ResourceGroup01.</span></span>

## <span data-ttu-id="c044d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c044d-114">PARAMETERS</span></span>

### <span data-ttu-id="c044d-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c044d-115">-AutomationAccountName</span></span>
<span data-ttu-id="c044d-116">Specifica il nome di un account di automazione in cui questo cmdlet ottiene un webhook.</span><span class="sxs-lookup"><span data-stu-id="c044d-116">Specifies the name of an Automation account in which this cmdlet gets a webhook.</span></span>

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

### <span data-ttu-id="c044d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c044d-117">-Name</span></span>
<span data-ttu-id="c044d-118">Specifica il nome del webhook ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c044d-118">Specifies the name of the webhook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c044d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c044d-119">-ResourceGroupName</span></span>
<span data-ttu-id="c044d-120">Specifica il nome del gruppo di risorse per cui questo cmdlet ottiene i webhook.</span><span class="sxs-lookup"><span data-stu-id="c044d-120">Specifies the name of the resource group for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="c044d-121">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="c044d-121">-RunbookName</span></span>
<span data-ttu-id="c044d-122">Specifica il nome di un Runbook per cui questo cmdlet ottiene i webhook.</span><span class="sxs-lookup"><span data-stu-id="c044d-122">Specifies the name of a runbook for which this cmdlet gets webhooks.</span></span>

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

### <span data-ttu-id="c044d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c044d-123">-DefaultProfile</span></span>
<span data-ttu-id="c044d-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c044d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c044d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c044d-125">CommonParameters</span></span>
<span data-ttu-id="c044d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c044d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c044d-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c044d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c044d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c044d-128">INPUTS</span></span>

## <span data-ttu-id="c044d-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c044d-129">OUTPUTS</span></span>

### <span data-ttu-id="c044d-130">Microsoft. Azure. Commands. Automation. Model. webhook</span><span class="sxs-lookup"><span data-stu-id="c044d-130">Microsoft.Azure.Commands.Automation.Model.Webhook</span></span>

## <span data-ttu-id="c044d-131">Note</span><span class="sxs-lookup"><span data-stu-id="c044d-131">NOTES</span></span>

## <span data-ttu-id="c044d-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c044d-132">RELATED LINKS</span></span>

[<span data-ttu-id="c044d-133">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c044d-133">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="c044d-134">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c044d-134">Remove-AzureRmAutomationWebhook</span></span>](./Remove-AzureRMAutomationWebhook.md)

[<span data-ttu-id="c044d-135">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="c044d-135">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


