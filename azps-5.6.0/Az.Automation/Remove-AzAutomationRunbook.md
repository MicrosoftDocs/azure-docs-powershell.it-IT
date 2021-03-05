---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: a7dc06e4ddbeac224daf9b8a80be40d343514a18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009886"
---
# <span data-ttu-id="3a321-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="3a321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a321-102">SYNOPSIS</span></span>
<span data-ttu-id="3a321-103">Rimuove un runbook.</span><span class="sxs-lookup"><span data-stu-id="3a321-103">Removes a runbook.</span></span>

## <span data-ttu-id="3a321-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3a321-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a321-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3a321-105">DESCRIPTION</span></span>
<span data-ttu-id="3a321-106">Il cmdlet **Remove-AzAutomationRunbook** rimuove un runbook dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3a321-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="3a321-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3a321-107">EXAMPLES</span></span>

### <span data-ttu-id="3a321-108">Esempio 1: Rimuovere un runbook</span><span class="sxs-lookup"><span data-stu-id="3a321-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3a321-109">Questo comando rimuove il runbook denominato Runbook03 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3a321-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3a321-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a321-110">PARAMETERS</span></span>

### <span data-ttu-id="3a321-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a321-111">-AutomationAccountName</span></span>
<span data-ttu-id="3a321-112">Specifica il nome dell'account di automazione in cui questo cmdlet rimuove un runbook.</span><span class="sxs-lookup"><span data-stu-id="3a321-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="3a321-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a321-113">-DefaultProfile</span></span>
<span data-ttu-id="3a321-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3a321-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a321-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3a321-115">-Force</span></span>
<span data-ttu-id="3a321-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="3a321-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a321-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3a321-117">-Name</span></span>
<span data-ttu-id="3a321-118">Specifica il nome del runbook rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a321-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a321-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a321-119">-ResourceGroupName</span></span>
<span data-ttu-id="3a321-120">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un runbook.</span><span class="sxs-lookup"><span data-stu-id="3a321-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="3a321-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a321-121">-Confirm</span></span>
<span data-ttu-id="3a321-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a321-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a321-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a321-123">-WhatIf</span></span>
<span data-ttu-id="3a321-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a321-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a321-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3a321-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a321-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a321-126">CommonParameters</span></span>
<span data-ttu-id="3a321-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a321-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a321-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a321-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a321-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="3a321-129">INPUTS</span></span>

### <span data-ttu-id="3a321-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3a321-130">System.String</span></span>

## <span data-ttu-id="3a321-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3a321-131">OUTPUTS</span></span>

### <span data-ttu-id="3a321-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="3a321-132">System.Void</span></span>

## <span data-ttu-id="3a321-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="3a321-133">NOTES</span></span>

## <span data-ttu-id="3a321-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3a321-134">RELATED LINKS</span></span>

[<span data-ttu-id="3a321-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="3a321-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="3a321-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="3a321-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="3a321-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="3a321-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="3a321-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="3a321-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3a321-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


