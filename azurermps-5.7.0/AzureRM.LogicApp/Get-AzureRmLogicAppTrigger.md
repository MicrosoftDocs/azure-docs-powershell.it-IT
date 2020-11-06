---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5307F1F1-E84C-4949-A557-99EF0012C3DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapptrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppTrigger.md
ms.openlocfilehash: f9f21689a894e46a9cd8d53d591d1cb17099fad8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511159"
---
# <span data-ttu-id="c37b0-101">Get-AzureRmLogicAppTrigger</span><span class="sxs-lookup"><span data-stu-id="c37b0-101">Get-AzureRmLogicAppTrigger</span></span>

## <span data-ttu-id="c37b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c37b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c37b0-103">Ottiene i trigger di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="c37b0-103">Gets the triggers of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c37b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c37b0-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppTrigger -ResourceGroupName <String> -Name <String> [-TriggerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c37b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c37b0-105">DESCRIPTION</span></span>
<span data-ttu-id="c37b0-106">Il cmdlet **Get-AzureRmLogicAppTrigger** ottiene trigger da un'app logica.</span><span class="sxs-lookup"><span data-stu-id="c37b0-106">The **Get-AzureRmLogicAppTrigger** cmdlet gets triggers from a logic app.</span></span>
<span data-ttu-id="c37b0-107">Questo cmdlet restituisce un oggetto **WorkflowTrigger** .</span><span class="sxs-lookup"><span data-stu-id="c37b0-107">This cmdlet returns a **WorkflowTrigger** object.</span></span>
<span data-ttu-id="c37b0-108">Specificare il flusso di lavoro, il gruppo di risorse e il trigger.</span><span class="sxs-lookup"><span data-stu-id="c37b0-108">Specify the workflow, resource group, and trigger.</span></span>

<span data-ttu-id="c37b0-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="c37b0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="c37b0-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="c37b0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="c37b0-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="c37b0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="c37b0-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="c37b0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="c37b0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c37b0-113">EXAMPLES</span></span>

### <span data-ttu-id="c37b0-114">Esempio 1: ottenere un trigger di un'app logica</span><span class="sxs-lookup"><span data-stu-id="c37b0-114">Example 1: Get a trigger of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -TriggerName "Trigger01"
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

<span data-ttu-id="c37b0-115">Questo comando ottiene il trigger denominato Trigger01 dall'app logica denominata LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="c37b0-115">This command gets the trigger named Trigger01 from the logic app named LogicApp05.</span></span>

### <span data-ttu-id="c37b0-116">Esempio 2: ottenere tutti i trigger di un'app logica</span><span class="sxs-lookup"><span data-stu-id="c37b0-116">Example 2: Get all triggers of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppTrigger -ResourceGroupName "ResourceGroup11" -Name "LogicApp07"
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

<span data-ttu-id="c37b0-117">Questo comando consente di ottenere i trigger dell'app logica denominata LogicApp07.</span><span class="sxs-lookup"><span data-stu-id="c37b0-117">This command gets the triggers of the logic app named LogicApp07.</span></span>

## <span data-ttu-id="c37b0-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c37b0-118">PARAMETERS</span></span>

### <span data-ttu-id="c37b0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37b0-119">-DefaultProfile</span></span>
<span data-ttu-id="c37b0-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c37b0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c37b0-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="c37b0-121">-Name</span></span>
<span data-ttu-id="c37b0-122">Specifica il nome dell'app logica da cui questo cmdlet ottiene un trigger.</span><span class="sxs-lookup"><span data-stu-id="c37b0-122">Specifies the name of the logic app from which this cmdlet gets a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c37b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="c37b0-124">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene un trigger.</span><span class="sxs-lookup"><span data-stu-id="c37b0-124">Specifies the name of a resource group in which this cmdlet gets a trigger.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37b0-125">-Triggername</span><span class="sxs-lookup"><span data-stu-id="c37b0-125">-TriggerName</span></span>
<span data-ttu-id="c37b0-126">Specifica il nome del trigger ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c37b0-126">Specifies the name of the trigger that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c37b0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37b0-127">CommonParameters</span></span>
<span data-ttu-id="c37b0-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c37b0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37b0-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c37b0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37b0-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c37b0-130">INPUTS</span></span>

### <span data-ttu-id="c37b0-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c37b0-131">None</span></span>
<span data-ttu-id="c37b0-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c37b0-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c37b0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c37b0-133">OUTPUTS</span></span>

### <span data-ttu-id="c37b0-134">Microsoft. Azure. Management. Logic. Models. WorkflowTrigger</span><span class="sxs-lookup"><span data-stu-id="c37b0-134">Microsoft.Azure.Management.Logic.Models.WorkflowTrigger</span></span>

## <span data-ttu-id="c37b0-135">Note</span><span class="sxs-lookup"><span data-stu-id="c37b0-135">NOTES</span></span>

## <span data-ttu-id="c37b0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c37b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="c37b0-137">Get-AzureRmLogicAppTriggerHistory</span><span class="sxs-lookup"><span data-stu-id="c37b0-137">Get-AzureRmLogicAppTriggerHistory</span></span>](./Get-AzureRmLogicAppTriggerHistory.md)

[<span data-ttu-id="c37b0-138">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="c37b0-138">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)


