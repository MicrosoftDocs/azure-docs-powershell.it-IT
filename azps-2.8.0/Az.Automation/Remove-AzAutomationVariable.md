---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 760C03A0-12DB-43C4-A180-B013FA77A513
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationVariable.md
ms.openlocfilehash: cfb8aa96da85cbfe1e9c16277c5c1c3539e04ac3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675704"
---
# <span data-ttu-id="e428d-101">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e428d-101">Remove-AzAutomationVariable</span></span>

## <span data-ttu-id="e428d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e428d-102">SYNOPSIS</span></span>
<span data-ttu-id="e428d-103">Rimuove una variabile di automazione.</span><span class="sxs-lookup"><span data-stu-id="e428d-103">Removes an Automation variable.</span></span>

## <span data-ttu-id="e428d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e428d-104">SYNTAX</span></span>

```
Remove-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e428d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e428d-105">DESCRIPTION</span></span>
<span data-ttu-id="e428d-106">Il cmdlet **Remove-AzAutomationVariable** consente di rimuovere una variabile da Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e428d-106">The **Remove-AzAutomationVariable** cmdlet removes a variable from Azure Automation.</span></span>

## <span data-ttu-id="e428d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e428d-107">EXAMPLES</span></span>

### <span data-ttu-id="e428d-108">Esempio 1: rimuovere una variabile</span><span class="sxs-lookup"><span data-stu-id="e428d-108">Example 1: Remove a variable</span></span>
```
PS C:\>Remove-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e428d-109">Questo comando consente di rimuovere una variabile denominata StringVariable22 nell'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e428d-109">This command removes a variable named StringVariable22 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="e428d-110">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="e428d-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e428d-111">Pertanto, non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="e428d-111">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e428d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e428d-112">PARAMETERS</span></span>

### <span data-ttu-id="e428d-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e428d-113">-AutomationAccountName</span></span>
<span data-ttu-id="e428d-114">Specifica il nome dell'account di automazione che contiene la variabile eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e428d-114">Specifies the name of the Automation account that contains the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e428d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e428d-115">-DefaultProfile</span></span>
<span data-ttu-id="e428d-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e428d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e428d-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e428d-117">-Name</span></span>
<span data-ttu-id="e428d-118">Specifica il nome della variabile eliminata dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e428d-118">Specifies the name of the variable that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="e428d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e428d-119">-ResourceGroupName</span></span>
<span data-ttu-id="e428d-120">Specifica il gruppo di risorse per cui questo cmdlet elimina una variabile.</span><span class="sxs-lookup"><span data-stu-id="e428d-120">Specifies the resource group for which this cmdlet deletes a variable.</span></span>

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

### <span data-ttu-id="e428d-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e428d-121">-Confirm</span></span>
<span data-ttu-id="e428d-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e428d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e428d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e428d-123">-WhatIf</span></span>
<span data-ttu-id="e428d-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e428d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e428d-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e428d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e428d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e428d-126">CommonParameters</span></span>
<span data-ttu-id="e428d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e428d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e428d-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e428d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e428d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e428d-129">INPUTS</span></span>

### <span data-ttu-id="e428d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e428d-130">System.String</span></span>

## <span data-ttu-id="e428d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e428d-131">OUTPUTS</span></span>

### <span data-ttu-id="e428d-132">System. void</span><span class="sxs-lookup"><span data-stu-id="e428d-132">System.Void</span></span>

## <span data-ttu-id="e428d-133">Note</span><span class="sxs-lookup"><span data-stu-id="e428d-133">NOTES</span></span>

## <span data-ttu-id="e428d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e428d-134">RELATED LINKS</span></span>

[<span data-ttu-id="e428d-135">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e428d-135">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="e428d-136">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e428d-136">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="e428d-137">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e428d-137">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


