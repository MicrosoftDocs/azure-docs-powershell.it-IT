---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031380"
---
# <span data-ttu-id="164e5-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="164e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="164e5-102">SYNOPSIS</span></span>
<span data-ttu-id="164e5-103">Rimuove un Runbook.</span><span class="sxs-lookup"><span data-stu-id="164e5-103">Removes a runbook.</span></span>

## <span data-ttu-id="164e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="164e5-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="164e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="164e5-105">DESCRIPTION</span></span>
<span data-ttu-id="164e5-106">Il cmdlet **Remove-AzAutomationRunbook** rimuove un Runbook da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="164e5-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="164e5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="164e5-107">EXAMPLES</span></span>

### <span data-ttu-id="164e5-108">Esempio 1: rimuovere un Runbook</span><span class="sxs-lookup"><span data-stu-id="164e5-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="164e5-109">Questo comando rimuove il Runbook denominato Runbook03 nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="164e5-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="164e5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="164e5-110">PARAMETERS</span></span>

### <span data-ttu-id="164e5-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="164e5-111">-AutomationAccountName</span></span>
<span data-ttu-id="164e5-112">Specifica il nome dell'account di automazione in cui questo cmdlet rimuove un Runbook.</span><span class="sxs-lookup"><span data-stu-id="164e5-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="164e5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="164e5-113">-DefaultProfile</span></span>
<span data-ttu-id="164e5-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="164e5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="164e5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="164e5-115">-Force</span></span>
<span data-ttu-id="164e5-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="164e5-116">ps_force</span></span>

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

### <span data-ttu-id="164e5-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="164e5-117">-Name</span></span>
<span data-ttu-id="164e5-118">Specifica il nome del Runbook rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="164e5-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="164e5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="164e5-119">-ResourceGroupName</span></span>
<span data-ttu-id="164e5-120">Specifica il nome del gruppo di risorse per cui questo cmdlet pubblica un Runbook.</span><span class="sxs-lookup"><span data-stu-id="164e5-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="164e5-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="164e5-121">-Confirm</span></span>
<span data-ttu-id="164e5-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="164e5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="164e5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="164e5-123">-WhatIf</span></span>
<span data-ttu-id="164e5-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="164e5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="164e5-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="164e5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="164e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="164e5-126">CommonParameters</span></span>
<span data-ttu-id="164e5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="164e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="164e5-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="164e5-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="164e5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="164e5-129">INPUTS</span></span>

### <span data-ttu-id="164e5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="164e5-130">System.String</span></span>

## <span data-ttu-id="164e5-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="164e5-131">OUTPUTS</span></span>

### <span data-ttu-id="164e5-132">System. void</span><span class="sxs-lookup"><span data-stu-id="164e5-132">System.Void</span></span>

## <span data-ttu-id="164e5-133">Note</span><span class="sxs-lookup"><span data-stu-id="164e5-133">NOTES</span></span>

## <span data-ttu-id="164e5-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="164e5-134">RELATED LINKS</span></span>

[<span data-ttu-id="164e5-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="164e5-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="164e5-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="164e5-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="164e5-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="164e5-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="164e5-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="164e5-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="164e5-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


