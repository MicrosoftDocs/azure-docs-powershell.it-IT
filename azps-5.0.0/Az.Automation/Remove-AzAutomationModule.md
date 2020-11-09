---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310963"
---
# <span data-ttu-id="fd90c-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fd90c-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="fd90c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd90c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd90c-103">Rimuove un modulo dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="fd90c-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="fd90c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd90c-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd90c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd90c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd90c-106">Il cmdlet **Remove-AzAutomationModule** rimuove un modulo da un account di automazione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fd90c-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="fd90c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd90c-107">EXAMPLES</span></span>

### <span data-ttu-id="fd90c-108">Esempio 1: rimuovere un modulo</span><span class="sxs-lookup"><span data-stu-id="fd90c-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fd90c-109">Questo comando rimuove un modulo denominato ContosoModule dall'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fd90c-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="fd90c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd90c-110">PARAMETERS</span></span>

### <span data-ttu-id="fd90c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd90c-111">-AutomationAccountName</span></span>
<span data-ttu-id="fd90c-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove un modulo.</span><span class="sxs-lookup"><span data-stu-id="fd90c-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="fd90c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd90c-113">-DefaultProfile</span></span>
<span data-ttu-id="fd90c-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fd90c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd90c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd90c-115">-Force</span></span>
<span data-ttu-id="fd90c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="fd90c-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd90c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd90c-117">-Name</span></span>
<span data-ttu-id="fd90c-118">Specifica il nome del modulo rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd90c-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fd90c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd90c-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd90c-120">Specifica il nome di un gruppo di risorse in cui questo cmdlet rimuove un modulo.</span><span class="sxs-lookup"><span data-stu-id="fd90c-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="fd90c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd90c-121">-Confirm</span></span>
<span data-ttu-id="fd90c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd90c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd90c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd90c-123">-WhatIf</span></span>
<span data-ttu-id="fd90c-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd90c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd90c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd90c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd90c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd90c-126">CommonParameters</span></span>
<span data-ttu-id="fd90c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd90c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd90c-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd90c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd90c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd90c-129">INPUTS</span></span>

### <span data-ttu-id="fd90c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fd90c-130">System.String</span></span>

## <span data-ttu-id="fd90c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd90c-131">OUTPUTS</span></span>

### <span data-ttu-id="fd90c-132">System. void</span><span class="sxs-lookup"><span data-stu-id="fd90c-132">System.Void</span></span>

## <span data-ttu-id="fd90c-133">Note</span><span class="sxs-lookup"><span data-stu-id="fd90c-133">NOTES</span></span>

## <span data-ttu-id="fd90c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd90c-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd90c-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fd90c-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="fd90c-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fd90c-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="fd90c-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fd90c-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


