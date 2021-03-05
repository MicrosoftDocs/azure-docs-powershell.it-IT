---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: 6835fb2ce58e834e9270af293fdc4f0d07fc01aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008973"
---
# <span data-ttu-id="38e8d-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="38e8d-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="38e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38e8d-102">SYNOPSIS</span></span>

<span data-ttu-id="38e8d-103">Recupera un'azione da un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="38e8d-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="38e8d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38e8d-104">SYNTAX</span></span>

```powershell
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-FollowNextPageLink] [-MaximumFollowNextPageLink <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38e8d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38e8d-105">DESCRIPTION</span></span>

<span data-ttu-id="38e8d-106">Il **cmdlet Get-AzLogicAppRunAction** ottiene un'azione da un'app logica eseguita.</span><span class="sxs-lookup"><span data-stu-id="38e8d-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="38e8d-107">Questo cmdlet restituisce un oggetto **WorkflowRunAction.**</span><span class="sxs-lookup"><span data-stu-id="38e8d-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="38e8d-108">Specificare l'app per la logica, il gruppo di risorse ed eseguire.</span><span class="sxs-lookup"><span data-stu-id="38e8d-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="38e8d-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="38e8d-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="38e8d-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="38e8d-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="38e8d-111">Per individuare i nomi dei parametri dinamici, digitare un trattino (-) dopo il nome del cmdlet e quindi premere TAB più volte per scorrere i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="38e8d-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="38e8d-112">Se si omette un parametro di modello obbligatorio, il cmdlet chiede di specificare il valore.</span><span class="sxs-lookup"><span data-stu-id="38e8d-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="38e8d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38e8d-113">EXAMPLES</span></span>

### <span data-ttu-id="38e8d-114">Esempio 1: Ottenere un'azione dall'esecuzione di un'app logica</span><span class="sxs-lookup"><span data-stu-id="38e8d-114">Example 1: Get an action from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -ActionName "LogicAppAction01"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction01
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="38e8d-115">Questo comando ottiene una specifica azione dell'app logica denominata LogicApp05 per l'esecuzione con l'identificatore 08585925184423369718380498702CU26.</span><span class="sxs-lookup"><span data-stu-id="38e8d-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run with identifier 08585925184423369718380498702CU26.</span></span>

### <span data-ttu-id="38e8d-116">Esempio 2: Ottenere tutte le azioni da un'app logica eseguita</span><span class="sxs-lookup"><span data-stu-id="38e8d-116">Example 2: Get all the actions from a Logic App run</span></span>

```powershell
PS C:\>Get-AzLogicAppRunAction -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "08585925184423369718380498702CU26" -FollowNextPageLink
```

<span data-ttu-id="38e8d-117">Questo comando recupera tutte le azioni dell'app logica da un'esecuzione con l'identificatore 08585925184423369718380498702CU26 di un'app logica denominata LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="38e8d-117">This command gets all Logic App actions from a run with identifier 08585925184423369718380498702CU26 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="38e8d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38e8d-118">PARAMETERS</span></span>

### <span data-ttu-id="38e8d-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="38e8d-119">-ActionName</span></span>

<span data-ttu-id="38e8d-120">Specifica il nome di un'azione in esecuzione in un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="38e8d-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="38e8d-121">Questo cmdlet ottiene l'azione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="38e8d-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="38e8d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e8d-122">-DefaultProfile</span></span>

<span data-ttu-id="38e8d-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="38e8d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38e8d-124">-FollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="38e8d-124">-FollowNextPageLink</span></span>

<span data-ttu-id="38e8d-125">Indica che il cmdlet deve seguire i collegamenti alla pagina successiva.</span><span class="sxs-lookup"><span data-stu-id="38e8d-125">Indicates the cmdlet should follow next page links.</span></span>

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

### <span data-ttu-id="38e8d-126">-MaximumFollowNextPageLink</span><span class="sxs-lookup"><span data-stu-id="38e8d-126">-MaximumFollowNextPageLink</span></span>

<span data-ttu-id="38e8d-127">Specifica quante volte seguire i collegamenti alle pagine successivi se si usa FollowNextPageLink.</span><span class="sxs-lookup"><span data-stu-id="38e8d-127">Specifies how many times to follow next page links if FollowNextPageLink is used.</span></span>

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

### <span data-ttu-id="38e8d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="38e8d-128">-Name</span></span>

<span data-ttu-id="38e8d-129">Specifica il nome di un'app per la logica per cui il cmdlet riceve un'azione.</span><span class="sxs-lookup"><span data-stu-id="38e8d-129">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="38e8d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e8d-130">-ResourceGroupName</span></span>

<span data-ttu-id="38e8d-131">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene un'azione.</span><span class="sxs-lookup"><span data-stu-id="38e8d-131">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="38e8d-132">-RunName</span><span class="sxs-lookup"><span data-stu-id="38e8d-132">-RunName</span></span>

<span data-ttu-id="38e8d-133">Specifica il nome di un'esecuzione di un'app per la logica.</span><span class="sxs-lookup"><span data-stu-id="38e8d-133">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="38e8d-134">Questo cmdlet ottiene un'azione per l'esecuzione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="38e8d-134">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="38e8d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e8d-135">CommonParameters</span></span>

<span data-ttu-id="38e8d-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38e8d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e8d-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38e8d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e8d-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="38e8d-138">INPUTS</span></span>

### <span data-ttu-id="38e8d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="38e8d-139">System.String</span></span>

## <span data-ttu-id="38e8d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38e8d-140">OUTPUTS</span></span>

### <span data-ttu-id="38e8d-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="38e8d-141">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="38e8d-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="38e8d-142">NOTES</span></span>

## <span data-ttu-id="38e8d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38e8d-143">RELATED LINKS</span></span>

[<span data-ttu-id="38e8d-144">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="38e8d-144">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="38e8d-145">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="38e8d-145">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)
