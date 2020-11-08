---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: de1c40dc7c9f8fefb1a275394b066e8af96de211
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201172"
---
# <span data-ttu-id="6585a-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="6585a-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="6585a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6585a-102">SYNOPSIS</span></span>
<span data-ttu-id="6585a-103">Ottiene la cronologia di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="6585a-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="6585a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6585a-104">SYNTAX</span></span>

```
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6585a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6585a-105">DESCRIPTION</span></span>
<span data-ttu-id="6585a-106">Il cmdlet **Get-AzLogicAppRunHistory** ottiene la cronologia di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="6585a-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="6585a-107">Questo cmdlet restituisce una raccolta di oggetti **WorkflowRun** .</span><span class="sxs-lookup"><span data-stu-id="6585a-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="6585a-108">Specifica il gruppo delle app e delle risorse logiche.</span><span class="sxs-lookup"><span data-stu-id="6585a-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="6585a-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="6585a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6585a-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="6585a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6585a-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="6585a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6585a-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="6585a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6585a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6585a-113">EXAMPLES</span></span>

### <span data-ttu-id="6585a-114">Esempio 1: ottenere la cronologia di esecuzione di un'app logica</span><span class="sxs-lookup"><span data-stu-id="6585a-114">Example 1: Get the run history of a logic app</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03"
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

<span data-ttu-id="6585a-115">Questo comando consente di ottenere la cronologia di esecuzione di un'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="6585a-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="6585a-116">Esempio 2: ottenere un'app logica in esecuzione</span><span class="sxs-lookup"><span data-stu-id="6585a-116">Example 2: Get a logic app run</span></span>
```powershell
PS C:\>Get-AzLogicAppRunHistory -ResourceGroupName "Resourcegroup11" -Name "LogicApp03" -RunName "08587489104702792076"
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

<span data-ttu-id="6585a-117">Questo comando consente di ottenere un'app logica specifica eseguita per l'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="6585a-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="6585a-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="6585a-118">Example 3</span></span>

<span data-ttu-id="6585a-119">Questo comando consente di ottenere la cronologia di esecuzione di un'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="6585a-119">This command gets the run history of a logic app named LogicApp03.</span></span> <span data-ttu-id="6585a-120">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="6585a-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunHistory -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="6585a-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6585a-121">PARAMETERS</span></span>

### <span data-ttu-id="6585a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6585a-122">-DefaultProfile</span></span>
<span data-ttu-id="6585a-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6585a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6585a-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="6585a-124">-Name</span></span>
<span data-ttu-id="6585a-125">Specifica il nome dell'app logica per cui questo cmdlet ottiene la cronologia di esecuzione.</span><span class="sxs-lookup"><span data-stu-id="6585a-125">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="6585a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6585a-126">-ResourceGroupName</span></span>
<span data-ttu-id="6585a-127">Specifica il nome di un gruppo di risorse che contiene l'app logica.</span><span class="sxs-lookup"><span data-stu-id="6585a-127">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="6585a-128">-RunName</span><span class="sxs-lookup"><span data-stu-id="6585a-128">-RunName</span></span>
<span data-ttu-id="6585a-129">Specifica il nome di esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="6585a-129">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="6585a-130">Questo cmdlet ottiene l'esecuzione del flusso di lavoro specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6585a-130">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="6585a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6585a-131">CommonParameters</span></span>
<span data-ttu-id="6585a-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6585a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6585a-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6585a-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6585a-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6585a-134">INPUTS</span></span>

### <span data-ttu-id="6585a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6585a-135">System.String</span></span>

## <span data-ttu-id="6585a-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6585a-136">OUTPUTS</span></span>

### <span data-ttu-id="6585a-137">Microsoft. Azure. Management. Logic. Models. WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="6585a-137">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="6585a-138">Note</span><span class="sxs-lookup"><span data-stu-id="6585a-138">NOTES</span></span>

## <span data-ttu-id="6585a-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6585a-139">RELATED LINKS</span></span>

[<span data-ttu-id="6585a-140">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="6585a-140">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="6585a-141">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="6585a-141">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="6585a-142">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="6585a-142">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


