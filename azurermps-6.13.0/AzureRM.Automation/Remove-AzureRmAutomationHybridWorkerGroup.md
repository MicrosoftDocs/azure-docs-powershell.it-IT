---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRmAutomationHybridWorkerGroup.md
ms.openlocfilehash: b6f15bc55c2e9f9a05e60e7e6f2c139ddbb70454
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685786"
---
# <span data-ttu-id="74782-101">Remove-AzureRmAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="74782-101">Remove-AzureRmAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="74782-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74782-102">SYNOPSIS</span></span>
<span data-ttu-id="74782-103">Rimuove il gruppo di lavoratori ibridi dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="74782-103">Removes hybrid worker group from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74782-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74782-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74782-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74782-105">DESCRIPTION</span></span>
<span data-ttu-id="74782-106">Il cmdlet Remove-AzureRmAutomationHybridWorkerGroup rimuove un gruppo di lavoro ibrido dall'automazione.</span><span class="sxs-lookup"><span data-stu-id="74782-106">The Remove-AzureRmAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="74782-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74782-107">EXAMPLES</span></span>

### <span data-ttu-id="74782-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="74782-108">Example 1</span></span>
<span data-ttu-id="74782-109">Questo comando rimuove un lavoratore ibrido per nome.</span><span class="sxs-lookup"><span data-stu-id="74782-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzureRmAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="74782-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74782-110">PARAMETERS</span></span>

### <span data-ttu-id="74782-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="74782-111">-AutomationAccountName</span></span>
<span data-ttu-id="74782-112">Nome dell'account di automazione.</span><span class="sxs-lookup"><span data-stu-id="74782-112">The automation account name.</span></span>

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

### <span data-ttu-id="74782-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74782-113">-DefaultProfile</span></span>
<span data-ttu-id="74782-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="74782-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74782-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="74782-115">-Name</span></span>
<span data-ttu-id="74782-116">Nome del gruppo di lavoratori ibridi.</span><span class="sxs-lookup"><span data-stu-id="74782-116">The hybrid worker group name.</span></span>

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

### <span data-ttu-id="74782-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74782-117">-ResourceGroupName</span></span>
<span data-ttu-id="74782-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="74782-118">The resource group name.</span></span>

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

### <span data-ttu-id="74782-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74782-119">-Confirm</span></span>
<span data-ttu-id="74782-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74782-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74782-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74782-121">-WhatIf</span></span>
<span data-ttu-id="74782-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74782-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74782-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74782-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74782-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74782-124">CommonParameters</span></span>
<span data-ttu-id="74782-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74782-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74782-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74782-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74782-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74782-127">INPUTS</span></span>

### <span data-ttu-id="74782-128">System. String</span><span class="sxs-lookup"><span data-stu-id="74782-128">System.String</span></span>

## <span data-ttu-id="74782-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74782-129">OUTPUTS</span></span>

### <span data-ttu-id="74782-130">System. void</span><span class="sxs-lookup"><span data-stu-id="74782-130">System.Void</span></span>

## <span data-ttu-id="74782-131">Note</span><span class="sxs-lookup"><span data-stu-id="74782-131">NOTES</span></span>

## <span data-ttu-id="74782-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74782-132">RELATED LINKS</span></span>
