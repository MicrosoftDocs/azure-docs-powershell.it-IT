---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F271BCB1-6D43-48E5-BB51-00288F57BFFB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunhistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunHistory.md
ms.openlocfilehash: 855cab84e4ab9de2cd7afae2a25dbc867a192e96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187622"
---
# <span data-ttu-id="9d684-101">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="9d684-101">Get-AzLogicAppRunHistory</span></span>

## <span data-ttu-id="9d684-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d684-102">SYNOPSIS</span></span>

<span data-ttu-id="9d684-103">Ottiene la cronologia di esecuzione di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="9d684-103">Gets the run history of a logic app.</span></span>

## <span data-ttu-id="9d684-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d684-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunHistory -ResourceGroupName <String> -Name <String> [-RunName <String>] [-FollowNextPageLink]
 [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d684-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d684-105">DESCRIPTION</span></span>

<span data-ttu-id="9d684-106">Il cmdlet **Get-AzLogicAppRunHistory** ottiene la cronologia di esecuzione di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="9d684-106">The **Get-AzLogicAppRunHistory** cmdlet gets the run history of a logic app.</span></span>
<span data-ttu-id="9d684-107">Questo cmdlet restituisce una raccolta di oggetti **WorkflowRun.**</span><span class="sxs-lookup"><span data-stu-id="9d684-107">This cmdlet returns a collection of **WorkflowRun** objects.</span></span>
<span data-ttu-id="9d684-108">Specificare l'app logica e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9d684-108">Specify the logic app and resource group.</span></span>
<span data-ttu-id="9d684-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="9d684-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="9d684-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="9d684-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="9d684-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="9d684-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="9d684-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="9d684-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="9d684-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d684-113">EXAMPLES</span></span>

### <span data-ttu-id="9d684-114">Esempio 1: Ottenere la cronologia di esecuzione di un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="9d684-114">Example 1: Get the run history of a logic app</span></span>

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

<span data-ttu-id="9d684-115">Questo comando ottiene la cronologia di esecuzione di un'app per la logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="9d684-115">This command gets the run history of a logic app named LogicApp03.</span></span>

### <span data-ttu-id="9d684-116">Esempio 2: Eseguire un'app per la logica</span><span class="sxs-lookup"><span data-stu-id="9d684-116">Example 2: Get a logic app run</span></span>

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

<span data-ttu-id="9d684-117">Questo comando ottiene una specifica app per la logica eseguita per l'app logica denominata LogicApp03.</span><span class="sxs-lookup"><span data-stu-id="9d684-117">This command gets a specific logic app run for the logic app named LogicApp03.</span></span>

### <span data-ttu-id="9d684-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9d684-118">Example 3</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink
```

<span data-ttu-id="9d684-119">Questo comando recupera l'intera cronologia di esecuzione di un'app per la logica denominata LogicApp03 seguendo NextPageLink.</span><span class="sxs-lookup"><span data-stu-id="9d684-119">This command gets the entire run history of a logic app named LogicApp03 by following the NextPageLink.</span></span>

### <span data-ttu-id="9d684-120">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9d684-120">Example 4</span></span>

```powershell
Get-AzLogicAppRunHistory -Name 'LogicApp03' -ResourceGroupName MyResourceGroup -FollowNextPageLink -MaximumFollowNextPageLink 1
```

<span data-ttu-id="9d684-121">Questo comando ottiene le prime due pagine della cronologia di esecuzione di un'app per la logica denominata LogicApp03, seguendo NextPageLink e limitando le dimensioni dei risultati a due pagine.</span><span class="sxs-lookup"><span data-stu-id="9d684-121">This command gets the first two pages of run history of a logic app named LogicApp03 by following the NextPageLink and limiting the result size to two pages.</span></span>
<span data-ttu-id="9d684-122">Ogni pagina contiene trenta risultati.</span><span class="sxs-lookup"><span data-stu-id="9d684-122">Each page contains thirty results.</span></span>

## <span data-ttu-id="9d684-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d684-123">PARAMETERS</span></span>

### <span data-ttu-id="9d684-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d684-124">-DefaultProfile</span></span>

<span data-ttu-id="9d684-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="9d684-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d684-126">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="9d684-126">-FollowNextPageLink</span></span>

<span data-ttu-id="9d684-127">Indica che il cmdlet deve seguire i collegamenti alla pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="9d684-127">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="9d684-128">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="9d684-128">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="9d684-129">Specifica quante volte seguire i collegamenti alle pagine successivi se si usa FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="9d684-129">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="9d684-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9d684-130">-Name</span></span>

<span data-ttu-id="9d684-131">Specifica il nome dell'app per la logica per cui viene eseguita la cronologia di esecuzione del cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d684-131">Specifies the name of the logic app for which this cmdlet gets run history.</span></span>

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

### <span data-ttu-id="9d684-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d684-132">-ResourceGroupName</span></span>

<span data-ttu-id="9d684-133">Specifica il nome di un gruppo di risorse che contiene l'app logica.</span><span class="sxs-lookup"><span data-stu-id="9d684-133">Specifies the name of a resource group that contains the logic app.</span></span>

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

### <span data-ttu-id="9d684-134">-RunName</span><span class="sxs-lookup"><span data-stu-id="9d684-134">-RunName</span></span>

<span data-ttu-id="9d684-135">Specifica il nome eseguito di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="9d684-135">Specifies the run name of a logic app.</span></span>
<span data-ttu-id="9d684-136">Questo cmdlet ottiene l'esecuzione del flusso di lavoro specificata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d684-136">This cmdlet gets the workflow run that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="9d684-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d684-137">CommonParameters</span></span>

<span data-ttu-id="9d684-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d684-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d684-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d684-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d684-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d684-140">INPUTS</span></span>

### <span data-ttu-id="9d684-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9d684-141">System.String</span></span>

## <span data-ttu-id="9d684-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d684-142">OUTPUTS</span></span>

### <span data-ttu-id="9d684-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span><span class="sxs-lookup"><span data-stu-id="9d684-143">Microsoft.Azure.Management.Logic.Models.WorkflowRun</span></span>

## <span data-ttu-id="9d684-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d684-144">NOTES</span></span>

## <span data-ttu-id="9d684-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d684-145">RELATED LINKS</span></span>

[<span data-ttu-id="9d684-146">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="9d684-146">Get-AzLogicAppRunAction</span></span>](./Get-AzLogicAppRunAction.md)

[<span data-ttu-id="9d684-147">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="9d684-147">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)

[<span data-ttu-id="9d684-148">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="9d684-148">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
