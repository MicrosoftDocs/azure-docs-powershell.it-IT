---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: c77413f27bcde145334221465cbe792a5e1eaa5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684987"
---
# <span data-ttu-id="a52c4-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="a52c4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a52c4-102">SYNOPSIS</span></span>
<span data-ttu-id="a52c4-103">Rimuove un Runbook.</span><span class="sxs-lookup"><span data-stu-id="a52c4-103">Removes a runbook.</span></span>

## <span data-ttu-id="a52c4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a52c4-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a52c4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a52c4-105">DESCRIPTION</span></span>
<span data-ttu-id="a52c4-106">Il cmdlet **Remove-AzAutomationRunbook** rimuove un Runbook da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a52c4-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="a52c4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a52c4-107">EXAMPLES</span></span>

### <span data-ttu-id="a52c4-108">Esempio 1: rimuovere un Runbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a52c4-109">Questo comando rimuove il Runbook denominato Runbook03 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a52c4-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="a52c4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a52c4-110">PARAMETERS</span></span>

### <span data-ttu-id="a52c4-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a52c4-111">-AutomationAccountName</span></span>
<span data-ttu-id="a52c4-112">Specifica il nome dell'account di automazione in cui questo cmdlet rimuove un Runbook.</span><span class="sxs-lookup"><span data-stu-id="a52c4-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="a52c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a52c4-113">-DefaultProfile</span></span>
<span data-ttu-id="a52c4-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a52c4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a52c4-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a52c4-115">-Force</span></span>
<span data-ttu-id="a52c4-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="a52c4-116">ps_force</span></span>

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

### <span data-ttu-id="a52c4-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="a52c4-117">-Name</span></span>
<span data-ttu-id="a52c4-118">Specifica il nome del Runbook rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a52c4-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a52c4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a52c4-119">-ResourceGroupName</span></span>
<span data-ttu-id="a52c4-120">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="a52c4-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="a52c4-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a52c4-121">-Confirm</span></span>
<span data-ttu-id="a52c4-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a52c4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a52c4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a52c4-123">-WhatIf</span></span>
<span data-ttu-id="a52c4-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a52c4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a52c4-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a52c4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a52c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a52c4-126">CommonParameters</span></span>
<span data-ttu-id="a52c4-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a52c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a52c4-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a52c4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a52c4-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a52c4-129">INPUTS</span></span>

### <span data-ttu-id="a52c4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a52c4-130">System.String</span></span>

## <span data-ttu-id="a52c4-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a52c4-131">OUTPUTS</span></span>

### <span data-ttu-id="a52c4-132">System. void</span><span class="sxs-lookup"><span data-stu-id="a52c4-132">System.Void</span></span>

## <span data-ttu-id="a52c4-133">Note</span><span class="sxs-lookup"><span data-stu-id="a52c4-133">NOTES</span></span>

## <span data-ttu-id="a52c4-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a52c4-134">RELATED LINKS</span></span>

[<span data-ttu-id="a52c4-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="a52c4-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="a52c4-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="a52c4-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a52c4-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="a52c4-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="a52c4-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="a52c4-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="a52c4-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


