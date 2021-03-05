---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerHistory.md
ms.openlocfilehash: 7c0d34ad56021e2fb4f74aef1bed41ca38c918c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008878"
---
# <span data-ttu-id="1a901-101">Get-AzLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="1a901-101">Get-AzLogicAppTriggerHistory</span></span>

## <span data-ttu-id="1a901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a901-102">SYNOPSIS</span></span>

<span data-ttu-id="1a901-103">Recupera la cronologia dei trigger in un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="1a901-103">Gets the history of triggers in a logic app.</span></span>

## <span data-ttu-id="1a901-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a901-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a901-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a901-105">DESCRIPTION</span></span>

<span data-ttu-id="1a901-106">Il cmdlet **Get-AzLogicAppTriggerHistory** ottiene la cronologia dei trigger in un'app per la logica nella funzionalità App per la logica.</span><span class="sxs-lookup"><span data-stu-id="1a901-106">The **Get-AzLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="1a901-107">Questo cmdlet restituisce un **oggetto WorkflowTriggerHistory.**</span><span class="sxs-lookup"><span data-stu-id="1a901-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="1a901-108">Specificare l'app per la logica, il gruppo di risorse e il trigger.</span><span class="sxs-lookup"><span data-stu-id="1a901-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="1a901-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="1a901-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="1a901-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="1a901-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="1a901-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="1a901-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="1a901-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="1a901-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="1a901-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a901-113">EXAMPLES</span></span>

### <span data-ttu-id="1a901-114">Esempio 1: Ottenere la cronologia dei trigger di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="1a901-114">Example 1: Get a trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A15%3A16Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="1a901-115">Questo comando ottiene la cronologia di trigger di una specifica app per logica per un trigger nell'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="1a901-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="1a901-116">Esempio 2: Ottenere la cronologia dei trigger di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="1a901-116">Example 2: Get trigger histories of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
Code        : BadRequest
EndTime     : 1/13/2016 2:43:33 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/CAB46_60e2ad0f0e1947e8b5798716914c5d
              b6_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489106716457817
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:43:33 PM
Status      : Failed
TrackingId  : c91a63f1-48b4-4eae-91eb-8f6dbfa9fe06
Type        : Microsoft.Logic/workflows/triggers/histories

Code        : BadRequest
EndTime     : 1/13/2016 2:42:26 PM
Error       : {code, message}
Fired       : False
InputsLink  : https://flowprodcu02by01.blob.core.windows.net/flow3ea9ffd11c684c9f9f258b1a6ea5cb6020160113t000000zcontent/A7392_d1e831de68ac4ef89d19a40f05e663
              cb_httpTrigger:5Finputs:2Ejson?sv=2014-02-14&sr=b&sig=&se=2016-01-14T16%3A18%3A27Z&sp=r
Name        : 08587489107387695768
OutputsLink : 
Run         : 
StartTime   : 1/13/2016 2:42:26 PM
Status      : Failed
TrackingId  : f88a499b-f80f-4a28-9bbf-c4cc0d129700
Type        : Microsoft.Logic/workflows/triggers/histories
```

<span data-ttu-id="1a901-117">Questo comando recupera le cronologie dei trigger del flusso di lavoro per un trigger nell'app logica denominata LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="1a901-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

### <span data-ttu-id="1a901-118">Esempio 3: Ottenere l'intera cronologia dei trigger di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="1a901-118">Example 3: Get entire trigger history of a logic app</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink
```

<span data-ttu-id="1a901-119">Questo comando recupera l'intera cronologia dei trigger del flusso di lavoro per un trigger nell'app per la logica denominata LogicApp08 seguendo NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="1a901-119">This command gets the entire workflow trigger history for a trigger in the logic app named LogicApp08 by following the NextPageLink.</span></span>

### <span data-ttu-id="1a901-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="1a901-120">Example 4</span></span>

```powershell
PS C:\>Get-AzLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp08" -TriggerName "Trigger01" -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="1a901-121">Questo comando recupera le prime due pagine della cronologia dei trigger del flusso di lavoro per un trigger nell'app per la logica denominata LogicApp09, seguendo NextPageLink e limitando le dimensioni dei risultati a due pagine.</span><span class="sxs-lookup"><span data-stu-id="1a901-121">This command gets the first two pages of workflow trigger history for a trigger in the logic app named LogicApp09 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="1a901-122">Ogni pagina contiene trenta risultati.</span><span class="sxs-lookup"><span data-stu-id="1a901-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="1a901-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a901-123">PARAMETERS</span></span>

### <span data-ttu-id="1a901-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a901-124">-DefaultProfile</span></span>

<span data-ttu-id="1a901-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1a901-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a901-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="1a901-126">-FollowNextPageLink</span></span>

<span data-ttu-id="1a901-127">Indica che il cmdlet deve seguire i collegamenti alla pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="1a901-127">Indicates the cmdlet should follow next page links.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: FL

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a901-128">-HistoryName</span><span class="sxs-lookup"><span data-stu-id="1a901-128">-HistoryName</span></span>

<span data-ttu-id="1a901-129">Specifica il nome della cronologia che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a901-129">Specifies the name of the history that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a901-130">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="1a901-130">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="1a901-131">Specifica quante volte seguire i collegamenti alle pagine successivi se si usa FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="1a901-131">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ML

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a901-132">-Name</span><span class="sxs-lookup"><span data-stu-id="1a901-132">-Name</span></span>

<span data-ttu-id="1a901-133">Specifica il nome dell'app per la logica per cui il cmdlet ottiene la cronologia dei trigger.</span><span class="sxs-lookup"><span data-stu-id="1a901-133">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="1a901-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a901-134">-ResourceGroupName</span></span>

<span data-ttu-id="1a901-135">Specifica il nome del gruppo di risorse in cui il cmdlet ottiene la cronologia.</span><span class="sxs-lookup"><span data-stu-id="1a901-135">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="1a901-136">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="1a901-136">-TriggerName</span></span>

<span data-ttu-id="1a901-137">Specifica il nome del trigger per cui il cmdlet ottiene la cronologia.</span><span class="sxs-lookup"><span data-stu-id="1a901-137">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="1a901-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a901-138">CommonParameters</span></span>

<span data-ttu-id="1a901-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a901-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a901-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a901-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a901-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a901-141">INPUTS</span></span>

### <span data-ttu-id="1a901-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1a901-142">System.String</span></span>

## <span data-ttu-id="1a901-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a901-143">OUTPUTS</span></span>

### <span data-ttu-id="1a901-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="1a901-144">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="1a901-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a901-145">NOTES</span></span>

## <span data-ttu-id="1a901-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a901-146">RELATED LINKS</span></span>

[<span data-ttu-id="1a901-147">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="1a901-147">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="1a901-148">Get-AzLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="1a901-148">Get-AzLogicAppTrigger</span></span>](./Get-AzLogicAppTrigger.md)

[<span data-ttu-id="1a901-149">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="1a901-149">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)
