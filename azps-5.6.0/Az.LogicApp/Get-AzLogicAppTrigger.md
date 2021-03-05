---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTrigger.md
ms.openlocfilehash: 28a7cd76f03dd3b6d2fc79e5d0b8d4d963a7f55c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008926"
---
# <span data-ttu-id="8d24d-101">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="8d24d-101">Get-AzLogicAppTrigger</span></span>

## <span data-ttu-id="8d24d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d24d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d24d-103">Ottiene i trigger di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="8d24d-103">Gets the triggers of a logic app.</span></span>

## <span data-ttu-id="8d24d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8d24d-104">SYNTAX</span></span>

```
Get-AzLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d24d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8d24d-105">DESCRIPTION</span></span>
<span data-ttu-id="8d24d-106">Il cmdlet **Get-AzLogicAppTrigger** ottiene i trigger da un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="8d24d-106">The **Get-AzLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="8d24d-107">Questo cmdlet restituisce un **oggetto WorkflowTrigger.**</span><span class="sxs-lookup"><span data-stu-id="8d24d-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="8d24d-108">Specificare il flusso di lavoro, il gruppo di risorse e il trigger.</span><span class="sxs-lookup"><span data-stu-id="8d24d-108">Specify the workflow, resource group, and trigger.</span></span>
<span data-ttu-id="8d24d-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="8d24d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8d24d-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="8d24d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8d24d-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="8d24d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8d24d-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="8d24d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8d24d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8d24d-113">EXAMPLES</span></span>

### <span data-ttu-id="8d24d-114">Esempio 1: Ottenere un trigger di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="8d24d-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger01
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp05
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="8d24d-115">Questo comando recupera il trigger denominato Trigger01 dall'app logica denominata LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="8d24d-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="8d24d-116">Esempio 2: Ottenere tutti i trigger di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="8d24d-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
ChangedTime         : 1/14/2016 11:45:07 AM
CreatedTime         : 1/13/2016 2:42:26 PM
LastExecutionTime   : 1/14/2016 11:45:07 AM
Name                : Trigger02
NextExecutionTime   : 1/14/2016 12:45:07 PM
RecurrenceFrequency : Minute
RecurrenceInterval  : 60
Status              : Waiting
Type                : Microsoft.Logic/workflows/triggers
LogicAppName        : LogicApp07
LogicAppVersion     : 08587489107406290826
```

<span data-ttu-id="8d24d-117">Questo comando recupera i trigger dell'app logica denominata LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="8d24d-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="8d24d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d24d-118">PARAMETERS</span></span>

### <span data-ttu-id="8d24d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d24d-119">-DefaultProfile</span></span>
<span data-ttu-id="8d24d-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8d24d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d24d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8d24d-121">-Name</span></span>
<span data-ttu-id="8d24d-122">Specifica il nome dell'app per la logica da cui il cmdlet riceve un trigger.</span><span class="sxs-lookup"><span data-stu-id="8d24d-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d24d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d24d-123">-ResourceGroupName</span></span>
<span data-ttu-id="8d24d-124">Specifica il nome di un gruppo di risorse in cui viene attivato questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d24d-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d24d-125">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="8d24d-125">-TriggerName</span></span>
<span data-ttu-id="8d24d-126">Specifica il nome del trigger che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d24d-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d24d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d24d-127">CommonParameters</span></span>
<span data-ttu-id="8d24d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d24d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d24d-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d24d-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d24d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="8d24d-130">INPUTS</span></span>

### <span data-ttu-id="8d24d-131">System.String</span><span class="sxs-lookup"><span data-stu-id="8d24d-131">System.String</span></span>

## <span data-ttu-id="8d24d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8d24d-132">OUTPUTS</span></span>

### <span data-ttu-id="8d24d-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="8d24d-133">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="8d24d-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="8d24d-134">NOTES</span></span>

## <span data-ttu-id="8d24d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8d24d-135">RELATED LINKS</span></span>

[<span data-ttu-id="8d24d-136">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="8d24d-136">Get-AzLogicAppTriggerHistory</span></span>](./Get-AzLogicAppTriggerHistory.md)

[<span data-ttu-id="8d24d-137">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="8d24d-137">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


