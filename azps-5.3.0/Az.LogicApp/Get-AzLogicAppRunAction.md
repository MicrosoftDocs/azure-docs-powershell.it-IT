---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapprunaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppRunAction.md
ms.openlocfilehash: c382b4bb9a02150beaa6880fd88d8f7b376b7c34
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386256"
---
# <span data-ttu-id="bbdd1-101">Get-AzLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="bbdd1-101">Get-AzLogicAppRunAction</span></span>

## <span data-ttu-id="bbdd1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bbdd1-102">SYNOPSIS</span></span>
<span data-ttu-id="bbdd1-103">Ottiene un'azione da un'app logica in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-103">Gets an action from a logic app run.</span></span>

## <span data-ttu-id="bbdd1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bbdd1-104">SYNTAX</span></span>

```
Get-AzLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String> [-ActionName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbdd1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbdd1-105">DESCRIPTION</span></span>
<span data-ttu-id="bbdd1-106">Il cmdlet **Get-AzLogicAppRunAction** ottiene un'azione da un'app logica in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-106">The **Get-AzLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="bbdd1-107">Questo cmdlet restituisce un oggetto **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="bbdd1-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="bbdd1-108">Specifica l'app logica, il gruppo di risorse ed Esegui.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-108">Specify the logic app, resource group, and run.</span></span>
<span data-ttu-id="bbdd1-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bbdd1-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bbdd1-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bbdd1-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bbdd1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bbdd1-113">EXAMPLES</span></span>

### <span data-ttu-id="bbdd1-114">Esempio 1: ottenere un'azione da un'app logica in esecuzione</span><span class="sxs-lookup"><span data-stu-id="bbdd1-114">Example 1: Get an action from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="bbdd1-115">Questo comando consente di ottenere un'azione specifica dell'app logica dall'app logica denominata LogicApp05 per l'esecuzione denominata LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="bbdd1-116">Esempio 2: ottenere tutte le azioni da un'app logica eseguita</span><span class="sxs-lookup"><span data-stu-id="bbdd1-116">Example 2: Get all the actions from a Logic App run</span></span>
```powershell
PS C:\>Get-AzLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
Code        : NotFound
EndTime     : 1/13/2016 2:42:56 PM
Error       : 
InputsLink  : Microsoft.Azure.Management.Logic.Models.ContentLink
Name        : LogicAppAction1
OutputsLink : Microsoft.Azure.Management.Logic.Models.ContentLink
StartTime   : 1/13/2016 2:42:55 PM
Status      : Failed
TrackingId  : 
Type        :
```

<span data-ttu-id="bbdd1-117">Questo comando consente di ottenere tutte le azioni delle app logiche da un'esecuzione denominata LogicAppRun56 di un'app logica denominata LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

### <span data-ttu-id="bbdd1-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="bbdd1-118">Example 3</span></span>

<span data-ttu-id="bbdd1-119">Questo comando consente di ottenere tutte le azioni delle app logiche da un'esecuzione denominata LogicAppRun56 di un'app logica denominata LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-119">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span> <span data-ttu-id="bbdd1-120">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="bbdd1-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzLogicAppRunAction -Name 'IntegrationAccount31' -ResourceGroupName MyResourceGroup -RunName '08587489104702792076'
```

## <span data-ttu-id="bbdd1-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bbdd1-121">PARAMETERS</span></span>

### <span data-ttu-id="bbdd1-122">-ActionName</span><span class="sxs-lookup"><span data-stu-id="bbdd1-122">-ActionName</span></span>
<span data-ttu-id="bbdd1-123">Specifica il nome di un'azione in un'app logica in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-123">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="bbdd1-124">Questo cmdlet ottiene l'azione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-124">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbdd1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbdd1-125">-DefaultProfile</span></span>
<span data-ttu-id="bbdd1-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bbdd1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbdd1-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="bbdd1-127">-Name</span></span>
<span data-ttu-id="bbdd1-128">Specifica il nome di un'app logica per cui questo cmdlet riceve un'azione.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-128">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="bbdd1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbdd1-129">-ResourceGroupName</span></span>
<span data-ttu-id="bbdd1-130">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene un'azione.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-130">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="bbdd1-131">-RunName</span><span class="sxs-lookup"><span data-stu-id="bbdd1-131">-RunName</span></span>
<span data-ttu-id="bbdd1-132">Specifica il nome di un'esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-132">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="bbdd1-133">Questo cmdlet ottiene un'azione per l'esecuzione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-133">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="bbdd1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbdd1-134">CommonParameters</span></span>
<span data-ttu-id="bbdd1-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bbdd1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbdd1-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbdd1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbdd1-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bbdd1-137">INPUTS</span></span>

### <span data-ttu-id="bbdd1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bbdd1-138">System.String</span></span>

## <span data-ttu-id="bbdd1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bbdd1-139">OUTPUTS</span></span>

### <span data-ttu-id="bbdd1-140">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="bbdd1-140">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="bbdd1-141">Note</span><span class="sxs-lookup"><span data-stu-id="bbdd1-141">NOTES</span></span>

## <span data-ttu-id="bbdd1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bbdd1-142">RELATED LINKS</span></span>

[<span data-ttu-id="bbdd1-143">Get-AzLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="bbdd1-143">Get-AzLogicAppRunHistory</span></span>](./Get-AzLogicAppRunHistory.md)

[<span data-ttu-id="bbdd1-144">Stop-AzLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="bbdd1-144">Stop-AzLogicAppRun</span></span>](./Stop-AzLogicAppRun.md)


