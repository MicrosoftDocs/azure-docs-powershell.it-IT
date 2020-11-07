---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: cff5113c37580b375bbaaea24850d5b55cd110ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835495"
---
# <span data-ttu-id="3ddbf-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="3ddbf-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="3ddbf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ddbf-102">SYNOPSIS</span></span>
<span data-ttu-id="3ddbf-103">Ottiene la cronologia di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="3ddbf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ddbf-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ddbf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ddbf-105">DESCRIPTION</span></span>
<span data-ttu-id="3ddbf-106">Il cmdlet **Get-AzLogicAppRunHistory** ottiene la cronologia di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="3ddbf-107">Questo cmdlet restituisce una raccolta di oggetti **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="3ddbf-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="3ddbf-108">Specifica il gruppo delle app e delle risorse logiche.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="3ddbf-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3ddbf-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3ddbf-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3ddbf-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3ddbf-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ddbf-113">EXAMPLES</span></span>

### <span data-ttu-id="3ddbf-114">Esempio 1: ottenere la cronologia di esecuzione di un'app logica</span><span class="sxs-lookup"><span data-stu-id="3ddbf-114">Example 1: Get the run history of a logic app</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="3ddbf-115">Questo comando consente di ottenere la cronologia di esecuzione di un'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="3ddbf-116">Esempio 2: ottenere un'app logica in esecuzione</span><span class="sxs-lookup"><span data-stu-id="3ddbf-116">Example 2: Get a logic app run</span></span>
```
PS C:\>Get-AzLogicAppActionRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="3ddbf-117">Questo comando consente di ottenere un'app logica specifica eseguita per l'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

## <span data-ttu-id="3ddbf-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ddbf-118">PARAMETERS</span></span>

### <span data-ttu-id="3ddbf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ddbf-119">-DefaultProfile</span></span>
<span data-ttu-id="3ddbf-120">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ddbf-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ddbf-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ddbf-121">-Name</span></span>
<span data-ttu-id="3ddbf-122">Specifica il nome dell'app logica per cui questo cmdlet ottiene la cronologia di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-122">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ddbf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ddbf-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ddbf-124">Specifica il nome di un gruppo di risorse che contiene l'app logica.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-124">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="3ddbf-125">-RunName</span><span class="sxs-lookup"><span data-stu-id="3ddbf-125">-RunName</span></span>
<span data-ttu-id="3ddbf-126">Specifica il nome di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-126">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="3ddbf-127">Questo cmdlet ottiene l'esecuzione del flusso di lavoro specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-127">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="3ddbf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ddbf-128">CommonParameters</span></span>
<span data-ttu-id="3ddbf-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ddbf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ddbf-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ddbf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ddbf-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ddbf-131">INPUTS</span></span>

### <span data-ttu-id="3ddbf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3ddbf-132">System.String</span></span>

## <span data-ttu-id="3ddbf-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ddbf-133">OUTPUTS</span></span>

### <span data-ttu-id="3ddbf-134">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="3ddbf-134">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="3ddbf-135">Note</span><span class="sxs-lookup"><span data-stu-id="3ddbf-135">NOTES</span></span>

## <span data-ttu-id="3ddbf-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ddbf-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ddbf-137">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="3ddbf-137">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="3ddbf-138">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="3ddbf-138">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="3ddbf-139">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="3ddbf-139">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


