---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 71043093-DEE5-4395-B67A-2F104CF67893
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationwebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationWebhook.md
ms.openlocfilehash: 13eeb70905225b89cfc362a13425ec77e0ef9521
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018533"
---
# <span data-ttu-id="403ea-101">Remove-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="403ea-101">Remove-AzAutomationWebhook</span></span>

## <span data-ttu-id="403ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="403ea-102">SYNOPSIS</span></span>
<span data-ttu-id="403ea-103">Rimuove un webhook da un Runbook di automazione.</span><span class="sxs-lookup"><span data-stu-id="403ea-103">Removes a webhook from an Automation runbook.</span></span>

## <span data-ttu-id="403ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="403ea-104">SYNTAX</span></span>

```
Remove-AzAutomationWebhook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="403ea-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="403ea-105">DESCRIPTION</span></span>
<span data-ttu-id="403ea-106">Il cmdlet **Remove-AzAutomationWebhook** rimuove un webhook da un Runbook di automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="403ea-106">The **Remove-AzAutomationWebhook** cmdlet removes a webhook from an Azure Automation runbook.</span></span>
<span data-ttu-id="403ea-107">Il webhook viene eliminato.</span><span class="sxs-lookup"><span data-stu-id="403ea-107">The webhook is deleted.</span></span>

## <span data-ttu-id="403ea-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="403ea-108">EXAMPLES</span></span>

### <span data-ttu-id="403ea-109">Esempio 1: rimuovere un hook</span><span class="sxs-lookup"><span data-stu-id="403ea-109">Example 1: Remove a webhook</span></span>
```
PS C:\>Remove-AzAutomationWebhook -Name "Webhook11" -ResourceGroup "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Force
```

<span data-ttu-id="403ea-110">Questo comando rimuove un webhook denominato Webhook11 nell'account di automazione denominato AutomationAccount01.</span><span class="sxs-lookup"><span data-stu-id="403ea-110">This command removes a webhook named Webhook11 in the Automation account named AutomationAccount01.</span></span>
<span data-ttu-id="403ea-111">Il comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="403ea-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="403ea-112">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="403ea-112">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="403ea-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="403ea-113">PARAMETERS</span></span>

### <span data-ttu-id="403ea-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="403ea-114">-AutomationAccountName</span></span>
<span data-ttu-id="403ea-115">Specifica il nome di un account di automazione da cui questo cmdlet rimuove un webhook.</span><span class="sxs-lookup"><span data-stu-id="403ea-115">Specifies the name of an Automation account from which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="403ea-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="403ea-116">-DefaultProfile</span></span>
<span data-ttu-id="403ea-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="403ea-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="403ea-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="403ea-118">-Name</span></span>
<span data-ttu-id="403ea-119">Specifica il nome del webhook rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="403ea-119">Specifies the name of the webhook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="403ea-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="403ea-120">-ResourceGroupName</span></span>
<span data-ttu-id="403ea-121">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove un webhook.</span><span class="sxs-lookup"><span data-stu-id="403ea-121">Specifies the name of the resource group for which this cmdlet removes a webhook.</span></span>

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

### <span data-ttu-id="403ea-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="403ea-122">-Confirm</span></span>
<span data-ttu-id="403ea-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="403ea-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="403ea-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="403ea-124">-WhatIf</span></span>
<span data-ttu-id="403ea-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="403ea-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="403ea-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="403ea-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="403ea-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="403ea-127">CommonParameters</span></span>
<span data-ttu-id="403ea-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="403ea-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="403ea-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="403ea-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="403ea-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="403ea-130">INPUTS</span></span>

### <span data-ttu-id="403ea-131">System. String</span><span class="sxs-lookup"><span data-stu-id="403ea-131">System.String</span></span>

## <span data-ttu-id="403ea-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="403ea-132">OUTPUTS</span></span>

### <span data-ttu-id="403ea-133">System. void</span><span class="sxs-lookup"><span data-stu-id="403ea-133">System.Void</span></span>

## <span data-ttu-id="403ea-134">Note</span><span class="sxs-lookup"><span data-stu-id="403ea-134">NOTES</span></span>

## <span data-ttu-id="403ea-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="403ea-135">RELATED LINKS</span></span>

[<span data-ttu-id="403ea-136">Get-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="403ea-136">Get-AzAutomationWebhook</span></span>](./Get-AzAutomationWebhook.md)

[<span data-ttu-id="403ea-137">New-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="403ea-137">New-AzAutomationWebhook</span></span>](./New-AzAutomationWebhook.md)

[<span data-ttu-id="403ea-138">Set-AzAutomationWebhook</span><span class="sxs-lookup"><span data-stu-id="403ea-138">Set-AzAutomationWebhook</span></span>](./Set-AzAutomationWebhook.md)


