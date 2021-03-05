---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 35ef4a5629726b33a8d9099da78134e6a0bac8b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009934"
---
# <span data-ttu-id="4ca90-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="4ca90-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="4ca90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ca90-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca90-103">Rimuove il gruppo di utenti ibridi dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="4ca90-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="4ca90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ca90-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ca90-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4ca90-105">DESCRIPTION</span></span>
<span data-ttu-id="4ca90-106">Il cmdlet Remove-AzAutomationHybridWorkerGroup rimuove un gruppo di utenti ibridi dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="4ca90-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="4ca90-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ca90-107">EXAMPLES</span></span>

### <span data-ttu-id="4ca90-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ca90-108">Example 1</span></span>
<span data-ttu-id="4ca90-109">Questo comando rimuove un utente ibrido in base al nome.</span><span class="sxs-lookup"><span data-stu-id="4ca90-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="4ca90-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ca90-110">PARAMETERS</span></span>

### <span data-ttu-id="4ca90-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ca90-111">-AutomationAccountName</span></span>
<span data-ttu-id="4ca90-112">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="4ca90-112">The automation account name.</span></span>

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

### <span data-ttu-id="4ca90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca90-113">-DefaultProfile</span></span>
<span data-ttu-id="4ca90-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca90-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca90-115">-Name</span><span class="sxs-lookup"><span data-stu-id="4ca90-115">-Name</span></span>
<span data-ttu-id="4ca90-116">Nome del gruppo di utenti ibridi.</span><span class="sxs-lookup"><span data-stu-id="4ca90-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ca90-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ca90-117">-ResourceGroupName</span></span>
<span data-ttu-id="4ca90-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4ca90-118">The resource group name.</span></span>

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

### <span data-ttu-id="4ca90-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ca90-119">-Confirm</span></span>
<span data-ttu-id="4ca90-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ca90-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca90-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ca90-121">-WhatIf</span></span>
<span data-ttu-id="4ca90-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ca90-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ca90-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ca90-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ca90-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca90-124">CommonParameters</span></span>
<span data-ttu-id="4ca90-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca90-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ca90-126">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca90-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca90-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="4ca90-127">INPUTS</span></span>

### <span data-ttu-id="4ca90-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4ca90-128">System.String</span></span>

## <span data-ttu-id="4ca90-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ca90-129">OUTPUTS</span></span>

### <span data-ttu-id="4ca90-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="4ca90-130">System.Void</span></span>

## <span data-ttu-id="4ca90-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="4ca90-131">NOTES</span></span>

## <span data-ttu-id="4ca90-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ca90-132">RELATED LINKS</span></span>
