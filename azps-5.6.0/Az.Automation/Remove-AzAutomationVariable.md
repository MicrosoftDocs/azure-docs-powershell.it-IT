---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: 46dee36dccc4a6e73620732df18059f64ccb6587
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004749"
---
# <span data-ttu-id="8d1ee-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8d1ee-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="8d1ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d1ee-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1ee-103">Rimuove una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="8d1ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d1ee-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d1ee-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d1ee-105">DESCRIPTION</span></span>
<span data-ttu-id="8d1ee-106">Il cmdlet **Remove-AzAutomationVariable** rimuove una variabile dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="8d1ee-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d1ee-107">EXAMPLES</span></span>

### <span data-ttu-id="8d1ee-108">Esempio 1: Rimuovere una variabile</span><span class="sxs-lookup"><span data-stu-id="8d1ee-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8d1ee-109">Questo comando rimuove una variabile denominata StringVariable22 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="8d1ee-110">Questo comando specifica il *parametro Force.*</span><span class="sxs-lookup"><span data-stu-id="8d1ee-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="8d1ee-111">Di conseguenza, non richiede conferma.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="8d1ee-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d1ee-112">PARAMETERS</span></span>

### <span data-ttu-id="8d1ee-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8d1ee-113">-AutomationAccountName</span></span>
<span data-ttu-id="8d1ee-114">Specifica il nome dell'account di automazione che contiene la variabile che il cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8d1ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1ee-115">-DefaultProfile</span></span>
<span data-ttu-id="8d1ee-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8d1ee-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d1ee-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8d1ee-117">-Name</span></span>
<span data-ttu-id="8d1ee-118">Specifica il nome della variabile che il cmdlet elimina.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="8d1ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="8d1ee-120">Specifica il gruppo di risorse per cui questo cmdlet elimina una variabile.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="8d1ee-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d1ee-121">-Confirm</span></span>
<span data-ttu-id="8d1ee-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d1ee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d1ee-123">-WhatIf</span></span>
<span data-ttu-id="8d1ee-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d1ee-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d1ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1ee-126">CommonParameters</span></span>
<span data-ttu-id="8d1ee-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d1ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1ee-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d1ee-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1ee-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d1ee-129">INPUTS</span></span>

### <span data-ttu-id="8d1ee-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8d1ee-130">System.String</span></span>

## <span data-ttu-id="8d1ee-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d1ee-131">OUTPUTS</span></span>

### <span data-ttu-id="8d1ee-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="8d1ee-132">System.Void</span></span>

## <span data-ttu-id="8d1ee-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d1ee-133">NOTES</span></span>

## <span data-ttu-id="8d1ee-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d1ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="8d1ee-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8d1ee-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="8d1ee-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8d1ee-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="8d1ee-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="8d1ee-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


