---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200289"
---
# <span data-ttu-id="6ca0c-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6ca0c-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="6ca0c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ca0c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ca0c-103">Elimina una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="6ca0c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ca0c-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ca0c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ca0c-105">DESCRIPTION</span></span>
<span data-ttu-id="6ca0c-106">Il cmdlet **Remove-AzAutomationSchedule** Elimina una programmazione da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="6ca0c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ca0c-107">EXAMPLES</span></span>

### <span data-ttu-id="6ca0c-108">Esempio 1: rimuovere una pianificazione</span><span class="sxs-lookup"><span data-stu-id="6ca0c-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6ca0c-109">Questo comando Elimina la pianificazione denominata Schedule01 in account di automazione Contoso17 nel gruppo risorse ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6ca0c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ca0c-110">PARAMETERS</span></span>

### <span data-ttu-id="6ca0c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6ca0c-111">-AutomationAccountName</span></span>
<span data-ttu-id="6ca0c-112">Specifica il nome di un account di automazione per cui questo cmdlet rimuove una programmazione.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6ca0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ca0c-113">-DefaultProfile</span></span>
<span data-ttu-id="6ca0c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6ca0c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ca0c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6ca0c-115">-Force</span></span>
<span data-ttu-id="6ca0c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="6ca0c-116">ps_force</span></span>

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

### <span data-ttu-id="6ca0c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ca0c-117">-Name</span></span>
<span data-ttu-id="6ca0c-118">Specifica il nome per la pianificazione rimossa da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6ca0c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ca0c-119">-ResourceGroupName</span></span>
<span data-ttu-id="6ca0c-120">Specifica il nome di un gruppo di risorse per cui questo cmdlet rimuove una programmazione.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6ca0c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6ca0c-121">-Confirm</span></span>
<span data-ttu-id="6ca0c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ca0c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ca0c-123">-WhatIf</span></span>
<span data-ttu-id="6ca0c-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ca0c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ca0c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ca0c-126">CommonParameters</span></span>
<span data-ttu-id="6ca0c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ca0c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ca0c-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ca0c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ca0c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ca0c-129">INPUTS</span></span>

### <span data-ttu-id="6ca0c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6ca0c-130">System.String</span></span>

## <span data-ttu-id="6ca0c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ca0c-131">OUTPUTS</span></span>

### <span data-ttu-id="6ca0c-132">System. void</span><span class="sxs-lookup"><span data-stu-id="6ca0c-132">System.Void</span></span>

## <span data-ttu-id="6ca0c-133">Note</span><span class="sxs-lookup"><span data-stu-id="6ca0c-133">NOTES</span></span>

## <span data-ttu-id="6ca0c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ca0c-134">RELATED LINKS</span></span>

[<span data-ttu-id="6ca0c-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6ca0c-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="6ca0c-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6ca0c-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="6ca0c-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6ca0c-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)

