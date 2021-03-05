---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: da687cc3831f4a3cb278dbf032905b39750b8c8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004765"
---
# <span data-ttu-id="992b8-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="992b8-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="992b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="992b8-102">SYNOPSIS</span></span>
<span data-ttu-id="992b8-103">Elimina una pianificazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="992b8-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="992b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="992b8-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="992b8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="992b8-105">DESCRIPTION</span></span>
<span data-ttu-id="992b8-106">Il cmdlet **Remove-AzAutomationSchedule** elimina una pianificazione dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="992b8-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="992b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="992b8-107">EXAMPLES</span></span>

### <span data-ttu-id="992b8-108">Esempio 1: Rimuovere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="992b8-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="992b8-109">Questo comando elimina la pianificazione denominata Schedule01 nell'account di automazione Contoso17 nel gruppo di risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="992b8-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="992b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="992b8-110">PARAMETERS</span></span>

### <span data-ttu-id="992b8-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="992b8-111">-AutomationAccountName</span></span>
<span data-ttu-id="992b8-112">Specifica il nome di un account di automazione per cui questo cmdlet rimuove una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="992b8-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="992b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="992b8-113">-DefaultProfile</span></span>
<span data-ttu-id="992b8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="992b8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="992b8-115">-Force</span><span class="sxs-lookup"><span data-stu-id="992b8-115">-Force</span></span>
<span data-ttu-id="992b8-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="992b8-116">ps_force</span></span>

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

### <span data-ttu-id="992b8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="992b8-117">-Name</span></span>
<span data-ttu-id="992b8-118">Specifica il nome della pianificazione rimossa dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="992b8-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="992b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="992b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="992b8-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet rimuove una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="992b8-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="992b8-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="992b8-121">-Confirm</span></span>
<span data-ttu-id="992b8-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="992b8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="992b8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="992b8-123">-WhatIf</span></span>
<span data-ttu-id="992b8-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="992b8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="992b8-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="992b8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="992b8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="992b8-126">CommonParameters</span></span>
<span data-ttu-id="992b8-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="992b8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="992b8-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="992b8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="992b8-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="992b8-129">INPUTS</span></span>

### <span data-ttu-id="992b8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="992b8-130">System.String</span></span>

## <span data-ttu-id="992b8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="992b8-131">OUTPUTS</span></span>

### <span data-ttu-id="992b8-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="992b8-132">System.Void</span></span>

## <span data-ttu-id="992b8-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="992b8-133">NOTES</span></span>

## <span data-ttu-id="992b8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="992b8-134">RELATED LINKS</span></span>

[<span data-ttu-id="992b8-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="992b8-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="992b8-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="992b8-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="992b8-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="992b8-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


