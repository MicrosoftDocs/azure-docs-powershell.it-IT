---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: C1F6BBF9-0DB5-46FD-B8A8-9029B0AB6166
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptriggerhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTriggerHistory.md
ms.openlocfilehash: 9c27fd1e46d17722f843a09babab31338e88e2ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687832"
---
# <span data-ttu-id="7ea67-101">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="7ea67-101">Get-AzureRmLogicAppTriggerHistory</span></span>

## <span data-ttu-id="7ea67-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ea67-102">SYNOPSIS</span></span>
<span data-ttu-id="7ea67-103">Ottiene la cronologia dei trigger in un'app logica.</span><span class="sxs-lookup"><span data-stu-id="7ea67-103">Gets the history of triggers in a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ea67-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ea67-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTriggerHistory -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-HistoryName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ea67-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ea67-105">DESCRIPTION</span></span>
<span data-ttu-id="7ea67-106">Il cmdlet **Get-AzureRmLogicAppTriggerHistory** ottiene la cronologia dei trigger in un'app logica nella caratteristica delle app logiche.</span><span class="sxs-lookup"><span data-stu-id="7ea67-106">The **Get-AzureRmLogicAppTriggerHistory** cmdlet gets the history of triggers in a logic app in the Logic Apps feature.</span></span>
<span data-ttu-id="7ea67-107">Questo cmdlet restituisce un oggetto **WorkflowTriggerHistory** .</span><span class="sxs-lookup"><span data-stu-id="7ea67-107">This cmdlet returns a **WorkflowTriggerHistory** object.</span></span>
<span data-ttu-id="7ea67-108">Specifica l'app logica, il gruppo di risorse e il trigger.</span><span class="sxs-lookup"><span data-stu-id="7ea67-108">Specify the logic app, resource group, and trigger.</span></span>
<span data-ttu-id="7ea67-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="7ea67-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="7ea67-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="7ea67-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="7ea67-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="7ea67-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="7ea67-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="7ea67-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="7ea67-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ea67-113">EXAMPLES</span></span>

### <span data-ttu-id="7ea67-114">Esempio 1: ottenere una cronologia dei trigger di un'app logica</span><span class="sxs-lookup"><span data-stu-id="7ea67-114">Example 1: Get a trigger history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -TriggerName "Trigger01" -HistoryName "08587489107387695768"
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

<span data-ttu-id="7ea67-115">Questo comando consente di ottenere una cronologia di trigger dell'app logica specifica per un trigger nell'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="7ea67-115">This command gets a specific logic app trigger history for a trigger in the logic app named LogicApp03.</span></span>

### <span data-ttu-id="7ea67-116">Esempio 2: ottenere le cronologie dei trigger di un'app logica</span><span class="sxs-lookup"><span data-stu-id="7ea67-116">Example 2: Get trigger histories of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTriggerHistory -ResourceGroupName "ResourceGroup11" -Name "LogicApp07" -TriggerName "Trigger01"
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

<span data-ttu-id="7ea67-117">Questo comando consente di ottenere le cronologie dei trigger del flusso di lavoro per un trigger nell'app logica denominata LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="7ea67-117">This command gets the workflow trigger histories for a trigger in the logic app named LogicApp07.</span></span>

## <span data-ttu-id="7ea67-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ea67-118">PARAMETERS</span></span>

### <span data-ttu-id="7ea67-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ea67-119">-DefaultProfile</span></span>
<span data-ttu-id="7ea67-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7ea67-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ea67-121">-Historyname</span><span class="sxs-lookup"><span data-stu-id="7ea67-121">-HistoryName</span></span>
<span data-ttu-id="7ea67-122">Specifica il nome della cronologia ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ea67-122">Specifies the name of the history that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7ea67-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ea67-123">-Name</span></span>
<span data-ttu-id="7ea67-124">Specifica il nome dell'app logica per cui questo cmdlet ottiene la cronologia dei trigger.</span><span class="sxs-lookup"><span data-stu-id="7ea67-124">Specifies the name of the logic app for which this cmdlet gets trigger history.</span></span>

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

### <span data-ttu-id="7ea67-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ea67-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ea67-126">Specifica il nome del gruppo di risorse in cui questo cmdlet ottiene la cronologia.</span><span class="sxs-lookup"><span data-stu-id="7ea67-126">Specifies the name of the resource group in which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="7ea67-127">-Triggername</span><span class="sxs-lookup"><span data-stu-id="7ea67-127">-TriggerName</span></span>
<span data-ttu-id="7ea67-128">Specifica il nome del trigger per cui questo cmdlet ottiene la cronologia.</span><span class="sxs-lookup"><span data-stu-id="7ea67-128">Specifies the name of the trigger for which this cmdlet gets history.</span></span>

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

### <span data-ttu-id="7ea67-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ea67-129">CommonParameters</span></span>
<span data-ttu-id="7ea67-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ea67-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ea67-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ea67-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ea67-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ea67-132">INPUTS</span></span>

### <span data-ttu-id="7ea67-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7ea67-133">System.String</span></span>

## <span data-ttu-id="7ea67-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ea67-134">OUTPUTS</span></span>

### <span data-ttu-id="7ea67-135">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="7ea67-135">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerHistory</span></span>

## <span data-ttu-id="7ea67-136">Note</span><span class="sxs-lookup"><span data-stu-id="7ea67-136">NOTES</span></span>

## <span data-ttu-id="7ea67-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ea67-137">RELATED LINKS</span></span>

[<span data-ttu-id="7ea67-138">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="7ea67-138">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="7ea67-139">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="7ea67-139">Get-AzureRmLogicAppTrigger</span></span>](./Get-AzureRmLogicAppTrigger.md)

[<span data-ttu-id="7ea67-140">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="7ea67-140">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


