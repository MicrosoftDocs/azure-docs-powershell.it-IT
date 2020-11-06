---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunHistory.md
ms.openlocfilehash: 60c58d6e5cd395d60818c7d7777fe561259feb15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508116"
---
# <span data-ttu-id="6d52c-101">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="6d52c-101">Get-AzureRmLogicAppRunHistory</span></span>

## <span data-ttu-id="6d52c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d52c-102">SYNOPSIS</span></span>
<span data-ttu-id="6d52c-103">Ottiene la cronologia di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="6d52c-103">Gets the run history of a logic app.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d52c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d52c-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d52c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d52c-105">DESCRIPTION</span></span>
<span data-ttu-id="6d52c-106">Il cmdlet **Get-AzureRmLogicAppRunHistory** ottiene la cronologia di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="6d52c-106">The **Get-AzureRmLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="6d52c-107">Questo cmdlet restituisce una raccolta di oggetti **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="6d52c-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="6d52c-108">Specifica il gruppo delle app e delle risorse logiche.</span><span class="sxs-lookup"><span data-stu-id="6d52c-108">Specify the logic app and resource group.</span></span>

<span data-ttu-id="6d52c-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="6d52c-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6d52c-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="6d52c-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6d52c-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="6d52c-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6d52c-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="6d52c-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6d52c-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d52c-113">EXAMPLES</span></span>

### <span data-ttu-id="6d52c-114">Esempio 1: ottenere la cronologia di esecuzione di un'app logica</span><span class="sxs-lookup"><span data-stu-id="6d52c-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952540

CorrelationId    : d3ddc917-9aaa-47b3-8814-c621c2ae530b
EndTime          : 1/13/2016 2:42:56 PM
Error            : {code, message}
Name             : 08587489107100664541
Outputs          : {}
StartTime        : 1/13/2016 2:42:55 PM
Status           : Failed
TriggerName      : httpTrigger
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="6d52c-115">Questo comando consente di ottenere la cronologia di esecuzione di un'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="6d52c-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="6d52c-116">Esempio 2: ottenere un'app logica in esecuzione</span><span class="sxs-lookup"><span data-stu-id="6d52c-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
CorrelationId    : 55830326-9042-404d-a4c3-fab198106a57
EndTime          : 1/13/2016 2:46:55 PM
Error            : {code, message}
Name             : 08587489104702792076
Outputs          : {}
StartTime        : 1/13/2016 2:46:55 PM
Status           : Failed
TriggerName      : 
LogicAppName     : LogicApp03
LogicAppVersion  : 08587489107859952120
```

<span data-ttu-id="6d52c-117">Questo comando consente di ottenere un'app logica specifica eseguita per l'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="6d52c-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="6d52c-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d52c-118">PARAMETERS</span></span>

### <span data-ttu-id="6d52c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d52c-119">-DefaultProfile</span></span>
<span data-ttu-id="6d52c-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6d52c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d52c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d52c-121">-Name</span></span>
<span data-ttu-id="6d52c-122">Specifica il nome dell'app logica per cui questo cmdlet ottiene la cronologia di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6d52c-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d52c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d52c-123">-ResourceGroupName</span></span>
<span data-ttu-id="6d52c-124">Specifica il nome di un gruppo di risorse che contiene l'app logica.</span><span class="sxs-lookup"><span data-stu-id="6d52c-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="6d52c-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="6d52c-125">-RunName</span></span>
<span data-ttu-id="6d52c-126">Specifica il nome di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="6d52c-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="6d52c-127">Questo cmdlet ottiene l'esecuzione del flusso di lavoro specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d52c-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="6d52c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d52c-128">CommonParameters</span></span>
<span data-ttu-id="6d52c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d52c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d52c-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d52c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d52c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d52c-131">INPUTS</span></span>

### <span data-ttu-id="6d52c-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6d52c-132">None</span></span>
<span data-ttu-id="6d52c-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6d52c-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d52c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d52c-134">OUTPUTS</span></span>

### <span data-ttu-id="6d52c-135">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="6d52c-135">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="6d52c-136">Note</span><span class="sxs-lookup"><span data-stu-id="6d52c-136">NOTES</span></span>

## <span data-ttu-id="6d52c-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d52c-137">RELATED LINKS</span></span>

[<span data-ttu-id="6d52c-138">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="6d52c-138">Get-AzureRmLogicAppRunAction</span></span>](./Get-AzureRmLogicAppRunAction.md)

[<span data-ttu-id="6d52c-139">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="6d52c-139">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

[<span data-ttu-id="6d52c-140">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="6d52c-140">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)

