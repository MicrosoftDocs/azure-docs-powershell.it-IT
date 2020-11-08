---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022884"
---
# <span data-ttu-id="eb19e-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="eb19e-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="eb19e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eb19e-102">SYNOPSIS</span></span>
<span data-ttu-id="eb19e-103">Rimuove il gruppo di lavoratori ibridi dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="eb19e-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="eb19e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eb19e-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb19e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eb19e-105">DESCRIPTION</span></span>
<span data-ttu-id="eb19e-106">Il cmdlet Remove-AzAutomationHybridWorkerGroup rimuove un gruppo di lavoro ibrido dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="eb19e-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="eb19e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eb19e-107">EXAMPLES</span></span>

### <span data-ttu-id="eb19e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="eb19e-108">Example 1</span></span>
<span data-ttu-id="eb19e-109">Questo comando rimuove un lavoratore ibrido per nome.</span><span class="sxs-lookup"><span data-stu-id="eb19e-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="eb19e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eb19e-110">PARAMETERS</span></span>

### <span data-ttu-id="eb19e-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="eb19e-111">-AutomationAccountName</span></span>
<span data-ttu-id="eb19e-112">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="eb19e-112">The automation account name.</span></span>

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

### <span data-ttu-id="eb19e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb19e-113">-DefaultProfile</span></span>
<span data-ttu-id="eb19e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eb19e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb19e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb19e-115">-Name</span></span>
<span data-ttu-id="eb19e-116">Nome del gruppo di lavoratori ibridi.</span><span class="sxs-lookup"><span data-stu-id="eb19e-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="eb19e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb19e-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb19e-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eb19e-118">The resource group name.</span></span>

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

### <span data-ttu-id="eb19e-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eb19e-119">-Confirm</span></span>
<span data-ttu-id="eb19e-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb19e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb19e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb19e-121">-WhatIf</span></span>
<span data-ttu-id="eb19e-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb19e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb19e-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eb19e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb19e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb19e-124">CommonParameters</span></span>
<span data-ttu-id="eb19e-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb19e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb19e-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb19e-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb19e-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eb19e-127">INPUTS</span></span>

### <span data-ttu-id="eb19e-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb19e-128">System.String</span></span>

## <span data-ttu-id="eb19e-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eb19e-129">OUTPUTS</span></span>

### <span data-ttu-id="eb19e-130">System. void</span><span class="sxs-lookup"><span data-stu-id="eb19e-130">System.Void</span></span>

## <span data-ttu-id="eb19e-131">Note</span><span class="sxs-lookup"><span data-stu-id="eb19e-131">NOTES</span></span>

## <span data-ttu-id="eb19e-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eb19e-132">RELATED LINKS</span></span>
