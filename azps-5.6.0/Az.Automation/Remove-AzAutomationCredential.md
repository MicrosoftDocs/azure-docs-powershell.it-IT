---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 3fb795f614e6ccd7c4e97470d89c6c8923fa9165
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009949"
---
# <span data-ttu-id="93001-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93001-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="93001-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93001-102">SYNOPSIS</span></span>
<span data-ttu-id="93001-103">Rimuove le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="93001-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="93001-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93001-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93001-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93001-105">DESCRIPTION</span></span>
<span data-ttu-id="93001-106">Il cmdlet **Remove-AzAutomationCredential** rimuove una credenziali dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="93001-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="93001-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93001-107">EXAMPLES</span></span>

### <span data-ttu-id="93001-108">Esempio 1: Rimuovere le credenziali</span><span class="sxs-lookup"><span data-stu-id="93001-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="93001-109">Questo comando rimuove una credenziali denominata ContosoCredential nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="93001-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="93001-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93001-110">PARAMETERS</span></span>

### <span data-ttu-id="93001-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="93001-111">-AutomationAccountName</span></span>
<span data-ttu-id="93001-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove le credenziali.</span><span class="sxs-lookup"><span data-stu-id="93001-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="93001-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93001-113">-DefaultProfile</span></span>
<span data-ttu-id="93001-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93001-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93001-115">-Name</span><span class="sxs-lookup"><span data-stu-id="93001-115">-Name</span></span>
<span data-ttu-id="93001-116">Specifica il nome delle credenziali rimosse dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93001-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="93001-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93001-117">-ResourceGroupName</span></span>
<span data-ttu-id="93001-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove le credenziali.</span><span class="sxs-lookup"><span data-stu-id="93001-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="93001-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93001-119">-Confirm</span></span>
<span data-ttu-id="93001-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93001-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93001-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93001-121">-WhatIf</span></span>
<span data-ttu-id="93001-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93001-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93001-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93001-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93001-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93001-124">CommonParameters</span></span>
<span data-ttu-id="93001-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93001-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93001-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93001-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93001-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="93001-127">INPUTS</span></span>

### <span data-ttu-id="93001-128">System.String</span><span class="sxs-lookup"><span data-stu-id="93001-128">System.String</span></span>

## <span data-ttu-id="93001-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93001-129">OUTPUTS</span></span>

### <span data-ttu-id="93001-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="93001-130">System.Void</span></span>

## <span data-ttu-id="93001-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="93001-131">NOTES</span></span>

## <span data-ttu-id="93001-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93001-132">RELATED LINKS</span></span>

[<span data-ttu-id="93001-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93001-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="93001-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93001-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="93001-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="93001-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


