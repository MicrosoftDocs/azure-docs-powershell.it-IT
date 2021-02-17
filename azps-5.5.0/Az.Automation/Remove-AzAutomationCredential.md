---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B53B765F-5CFC-4BF8-A48A-E638A73E1FC5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationCredential.md
ms.openlocfilehash: 2f5aef61ad89bc7ac4879c3a40880522a52020e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205507"
---
# <span data-ttu-id="5af78-101">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5af78-101">Remove-AzAutomationCredential</span></span>

## <span data-ttu-id="5af78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5af78-102">SYNOPSIS</span></span>
<span data-ttu-id="5af78-103">Rimuove le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="5af78-103">Removes an Automation credential.</span></span>

## <span data-ttu-id="5af78-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5af78-104">SYNTAX</span></span>

```
Remove-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af78-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5af78-105">DESCRIPTION</span></span>
<span data-ttu-id="5af78-106">Il cmdlet **Remove-AzAutomationCredential** rimuove una credenziali dall'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5af78-106">The **Remove-AzAutomationCredential** cmdlet removes a credential from Azure Automation.</span></span>

## <span data-ttu-id="5af78-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5af78-107">EXAMPLES</span></span>

### <span data-ttu-id="5af78-108">Esempio 1: Rimuovere le credenziali</span><span class="sxs-lookup"><span data-stu-id="5af78-108">Example 1: Remove a credential</span></span>
```
PS C:\>Remove-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5af78-109">Questo comando rimuove una credenziali denominata ContosoCredential nell'account di automazione di Azure denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5af78-109">This command removes a credential named ContosoCredential in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5af78-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5af78-110">PARAMETERS</span></span>

### <span data-ttu-id="5af78-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5af78-111">-AutomationAccountName</span></span>
<span data-ttu-id="5af78-112">Specifica il nome dell'account di automazione da cui questo cmdlet rimuove le credenziali.</span><span class="sxs-lookup"><span data-stu-id="5af78-112">Specifies the name of the Automation account from which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="5af78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af78-113">-DefaultProfile</span></span>
<span data-ttu-id="5af78-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5af78-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5af78-115">-Name</span><span class="sxs-lookup"><span data-stu-id="5af78-115">-Name</span></span>
<span data-ttu-id="5af78-116">Specifica il nome delle credenziali rimosse dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5af78-116">Specifies the name of the credential that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5af78-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af78-117">-ResourceGroupName</span></span>
<span data-ttu-id="5af78-118">Specifica il nome del gruppo di risorse per cui questo cmdlet rimuove le credenziali.</span><span class="sxs-lookup"><span data-stu-id="5af78-118">Specifies the name of the resource group for which this cmdlet removes a credential.</span></span>

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

### <span data-ttu-id="5af78-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5af78-119">-Confirm</span></span>
<span data-ttu-id="5af78-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5af78-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af78-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af78-121">-WhatIf</span></span>
<span data-ttu-id="5af78-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5af78-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af78-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5af78-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af78-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af78-124">CommonParameters</span></span>
<span data-ttu-id="5af78-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af78-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af78-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5af78-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af78-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="5af78-127">INPUTS</span></span>

### <span data-ttu-id="5af78-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5af78-128">System.String</span></span>

## <span data-ttu-id="5af78-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5af78-129">OUTPUTS</span></span>

### <span data-ttu-id="5af78-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="5af78-130">System.Void</span></span>

## <span data-ttu-id="5af78-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="5af78-131">NOTES</span></span>

## <span data-ttu-id="5af78-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5af78-132">RELATED LINKS</span></span>

[<span data-ttu-id="5af78-133">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5af78-133">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="5af78-134">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5af78-134">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="5af78-135">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="5af78-135">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


