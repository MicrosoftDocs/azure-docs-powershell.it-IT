---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 01bba193f763eff784bdd5f3f67118d84c6235a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008942"
---
# <span data-ttu-id="0ec5a-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="0ec5a-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="0ec5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ec5a-102">SYNOPSIS</span></span>

<span data-ttu-id="0ec5a-103">Ottiene la cronologia di esecuzione di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="0ec5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ec5a-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ec5a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0ec5a-105">DESCRIPTION</span></span>

<span data-ttu-id="0ec5a-106">Il cmdlet **Get-AzLogicAppRunHistory** ottiene la cronologia di esecuzione di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="0ec5a-107">Questo cmdlet restituisce una raccolta di oggetti **WorkflowRun.**</span><span class="sxs-lookup"><span data-stu-id="0ec5a-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="0ec5a-108">Specificare l'app logica e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="0ec5a-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0ec5a-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0ec5a-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0ec5a-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0ec5a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ec5a-113">EXAMPLES</span></span>

### <span data-ttu-id="0ec5a-114">Esempio 1: Ottenere la cronologia di esecuzione di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="0ec5a-114">Example 1: Get the run history of a logic app</span></span>

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

<span data-ttu-id="0ec5a-115">Questo comando ottiene la cronologia di esecuzione di un'app per la logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="0ec5a-116">Esempio 2: Eseguire un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="0ec5a-116">Example 2: Get a logic app run</span></span>

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

<span data-ttu-id="0ec5a-117">Questo comando ottiene una specifica app per la logica eseguita per l'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="0ec5a-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0ec5a-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="0ec5a-119">Questo comando ottiene l'intera cronologia di esecuzione di un'app per la logica denominata LogicApp03 seguendo NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="0ec5a-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="0ec5a-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="0ec5a-121">Questo comando ottiene le prime due pagine della cronologia di esecuzione di un'app per la logica denominata LogicApp03, seguendo NextPageLink e limitando le dimensioni dei risultati a due pagine.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="0ec5a-122">Ogni pagina contiene trenta risultati.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="0ec5a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ec5a-123">PARAMETERS</span></span>

### <span data-ttu-id="0ec5a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec5a-124">-DefaultProfile</span></span>

<span data-ttu-id="0ec5a-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0ec5a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ec5a-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="0ec5a-126">-FollowNextPageLink</span></span>

<span data-ttu-id="0ec5a-127">Indica che il cmdlet deve seguire i collegamenti alla pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="0ec5a-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="0ec5a-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="0ec5a-129">Specifica quante volte seguire i collegamenti alle pagine successivi se si usa FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="0ec5a-130">-Name</span><span class="sxs-lookup"><span data-stu-id="0ec5a-130">-Name</span></span>

<span data-ttu-id="0ec5a-131">Specifica il nome dell'app per la logica per cui viene eseguita la cronologia di esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="0ec5a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ec5a-132">-ResourceGroupName</span></span>

<span data-ttu-id="0ec5a-133">Specifica il nome di un gruppo di risorse che contiene l'app logica.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="0ec5a-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="0ec5a-134">-RunName</span></span>

<span data-ttu-id="0ec5a-135">Specifica il nome eseguito di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="0ec5a-136">Questo cmdlet ottiene l'esecuzione del flusso di lavoro specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="0ec5a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec5a-137">CommonParameters</span></span>

<span data-ttu-id="0ec5a-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec5a-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0ec5a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec5a-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="0ec5a-140">INPUTS</span></span>

### <span data-ttu-id="0ec5a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0ec5a-141">System.String</span></span>

## <span data-ttu-id="0ec5a-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ec5a-142">OUTPUTS</span></span>

### <span data-ttu-id="0ec5a-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="0ec5a-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="0ec5a-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="0ec5a-144">NOTES</span></span>

## <span data-ttu-id="0ec5a-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ec5a-145">RELATED LINKS</span></span>

[<span data-ttu-id="0ec5a-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="0ec5a-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="0ec5a-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="0ec5a-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="0ec5a-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="0ec5a-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
