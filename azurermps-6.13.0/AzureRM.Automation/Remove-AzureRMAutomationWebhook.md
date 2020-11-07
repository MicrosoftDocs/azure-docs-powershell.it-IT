---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationWebhook.md
ms.openlocfilehash: 5f90f80c9ec0ebcb506e1a7f7a506a000224c142
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686644"
---
# <span data-ttu-id="cf00c-101">Remove-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf00c-101">Remove-AzureRmAutomationWebhook</span></span>

## <span data-ttu-id="cf00c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cf00c-102">SYNOPSIS</span></span>
<span data-ttu-id="cf00c-103">Rimuove un webhook da un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="cf00c-103">Removes a webhook from an Automation runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cf00c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cf00c-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationWebhook [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cf00c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cf00c-105">DESCRIPTION</span></span>
<span data-ttu-id="cf00c-106">Il cmdlet **Remove-AzureRmAutomationWebhook** rimuove un webhook da un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cf00c-106">The **Remove-AzureRmAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="cf00c-107">Il webhook viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="cf00c-107">The webhook is deleted.</span></span>

## <span data-ttu-id="cf00c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cf00c-108">EXAMPLES</span></span>

### <span data-ttu-id="cf00c-109">Esempio 1: rimuovere un hook</span><span class="sxs-lookup"><span data-stu-id="cf00c-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzureRmAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="cf00c-110">Questo comando rimuove un webhook denominato Webhook11 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="cf00c-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="cf00c-111">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="cf00c-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cf00c-112">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="cf00c-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="cf00c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cf00c-113">PARAMETERS</span></span>

### <span data-ttu-id="cf00c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cf00c-114">-AutomationAccountName</span></span>
<span data-ttu-id="cf00c-115">Specifica il nome di un account di automazione da cui questo cmdlet rimuove un webhook.</span><span class="sxs-lookup"><span data-stu-id="cf00c-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="cf00c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf00c-116">-DefaultProfile</span></span>
<span data-ttu-id="cf00c-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cf00c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf00c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cf00c-118">-Name</span></span>
<span data-ttu-id="cf00c-119">Specifica il nome del webhook rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf00c-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cf00c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf00c-120">-ResourceGroupName</span></span>
<span data-ttu-id="cf00c-121">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove un webhook.</span><span class="sxs-lookup"><span data-stu-id="cf00c-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="cf00c-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cf00c-122">-Confirm</span></span>
<span data-ttu-id="cf00c-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cf00c-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf00c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf00c-124">-WhatIf</span></span>
<span data-ttu-id="cf00c-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf00c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf00c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cf00c-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf00c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf00c-127">CommonParameters</span></span>
<span data-ttu-id="cf00c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cf00c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf00c-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf00c-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf00c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cf00c-130">INPUTS</span></span>

### <span data-ttu-id="cf00c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="cf00c-131">System.String</span></span>

## <span data-ttu-id="cf00c-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cf00c-132">OUTPUTS</span></span>

### <span data-ttu-id="cf00c-133">System. void</span><span class="sxs-lookup"><span data-stu-id="cf00c-133">System.Void</span></span>

## <span data-ttu-id="cf00c-134">Note</span><span class="sxs-lookup"><span data-stu-id="cf00c-134">NOTES</span></span>

## <span data-ttu-id="cf00c-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cf00c-135">RELATED LINKS</span></span>

[<span data-ttu-id="cf00c-136">Get-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf00c-136">Get-AzureRmAutomationWebhook</span></span>](./Get-AzureRMAutomationWebhook.md)

[<span data-ttu-id="cf00c-137">New-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf00c-137">New-AzureRmAutomationWebhook</span></span>](./New-AzureRMAutomationWebhook.md)

[<span data-ttu-id="cf00c-138">Set-AzureRmAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="cf00c-138">Set-AzureRmAutomationWebhook</span></span>](./Set-AzureRMAutomationWebhook.md)


