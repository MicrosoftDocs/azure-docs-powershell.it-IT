---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2EA28B90-4BAE-45DF-BD2E-60C74F53FB7B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicAppRunAction.md
ms.openlocfilehash: 49968330f56fe0891adb9c5a62a1264700f53224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520509"
---
# <span data-ttu-id="a24e0-101">Get-AzureRmLogicAppRunAction</span><span class="sxs-lookup"><span data-stu-id="a24e0-101">Get-AzureRmLogicAppRunAction</span></span>

## <span data-ttu-id="a24e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a24e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a24e0-103">Ottiene un'azione da un'app logica in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a24e0-103">Gets an action from a logic app run.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a24e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a24e0-104">SYNTAX</span></span>

```
Get-AzureRmLogicAppRunAction -ResourceGroupName <String> -Name <String> -RunName <String>
 [-ActionName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a24e0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a24e0-105">DESCRIPTION</span></span>
<span data-ttu-id="a24e0-106">Il cmdlet **Get-AzureRmLogicAppRunAction** ottiene un'azione da un'app logica in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a24e0-106">The **Get-AzureRmLogicAppRunAction** cmdlet gets an action from a logic app run.</span></span>
<span data-ttu-id="a24e0-107">Questo cmdlet restituisce un oggetto **WorkflowRunAction** .</span><span class="sxs-lookup"><span data-stu-id="a24e0-107">This cmdlet returns a **WorkflowRunAction** objects.</span></span>
<span data-ttu-id="a24e0-108">Specifica l'app logica, il gruppo di risorse ed Esegui.</span><span class="sxs-lookup"><span data-stu-id="a24e0-108">Specify the logic app, resource group, and run.</span></span>

<span data-ttu-id="a24e0-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="a24e0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="a24e0-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="a24e0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="a24e0-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="a24e0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="a24e0-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="a24e0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="a24e0-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a24e0-113">EXAMPLES</span></span>

### <span data-ttu-id="a24e0-114">Esempio 1: ottenere un'azione da un'app logica in esecuzione</span><span class="sxs-lookup"><span data-stu-id="a24e0-114">Example 1: Get an action from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56" -ActionName "LogicAppAction01"
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

<span data-ttu-id="a24e0-115">Questo comando consente di ottenere un'azione specifica dell'app logica dall'app logica denominata LogicApp05 per l'esecuzione denominata LogicAppRun56.</span><span class="sxs-lookup"><span data-stu-id="a24e0-115">This command gets a specific Logic App action from the logic app named LogicApp05 for the run named LogicAppRun56.</span></span>

### <span data-ttu-id="a24e0-116">Esempio 2: ottenere tutte le azioni da un'app logica eseguita</span><span class="sxs-lookup"><span data-stu-id="a24e0-116">Example 2: Get all the actions from a Logic App run</span></span>
```
PS C:\>Get-AzureRmLogicAppActionRun -ResourceGroupName "ResourceGroup11" -Name "LogicApp05" -RunName "LogicAppRun56"
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

<span data-ttu-id="a24e0-117">Questo comando consente di ottenere tutte le azioni delle app logiche da un'esecuzione denominata LogicAppRun56 di un'app logica denominata LogicApp05.</span><span class="sxs-lookup"><span data-stu-id="a24e0-117">This command gets all Logic App actions from a run named LogicAppRun56 of a logic app named LogicApp05.</span></span>

## <span data-ttu-id="a24e0-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a24e0-118">PARAMETERS</span></span>

### <span data-ttu-id="a24e0-119">-ActionName</span><span class="sxs-lookup"><span data-stu-id="a24e0-119">-ActionName</span></span>
<span data-ttu-id="a24e0-120">Specifica il nome di un'azione in un'app logica in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a24e0-120">Specifies the name of an action in a logic app run.</span></span>
<span data-ttu-id="a24e0-121">Questo cmdlet ottiene l'azione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a24e0-121">This cmdlet gets the action that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24e0-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="a24e0-122">-Name</span></span>
<span data-ttu-id="a24e0-123">Specifica il nome di un'app logica per cui questo cmdlet riceve un'azione.</span><span class="sxs-lookup"><span data-stu-id="a24e0-123">Specifies the name of a logic app for which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="a24e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a24e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="a24e0-125">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene un'azione.</span><span class="sxs-lookup"><span data-stu-id="a24e0-125">Specifies the name of a resource group in which this cmdlet gets an action.</span></span>

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

### <span data-ttu-id="a24e0-126">-RunName</span><span class="sxs-lookup"><span data-stu-id="a24e0-126">-RunName</span></span>
<span data-ttu-id="a24e0-127">Specifica il nome di un'esecuzione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="a24e0-127">Specifies the name of a run of a logic app.</span></span>
<span data-ttu-id="a24e0-128">Questo cmdlet ottiene un'azione per l'esecuzione specificata da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="a24e0-128">This cmdlet gets an action for the run that this parameter specifies.</span></span>

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

### <span data-ttu-id="a24e0-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a24e0-129">-DefaultProfile</span></span>
<span data-ttu-id="a24e0-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a24e0-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a24e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a24e0-131">CommonParameters</span></span>
<span data-ttu-id="a24e0-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a24e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a24e0-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a24e0-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a24e0-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a24e0-134">INPUTS</span></span>

## <span data-ttu-id="a24e0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a24e0-135">OUTPUTS</span></span>

### <span data-ttu-id="a24e0-136">Microsoft. Azure. Management. Logic. Models. WorkflowRunAction</span><span class="sxs-lookup"><span data-stu-id="a24e0-136">Microsoft.Azure.Management.Logic.Models.WorkflowRunAction</span></span>

## <span data-ttu-id="a24e0-137">Note</span><span class="sxs-lookup"><span data-stu-id="a24e0-137">NOTES</span></span>

## <span data-ttu-id="a24e0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a24e0-138">RELATED LINKS</span></span>

[<span data-ttu-id="a24e0-139">Get-AzureRmLogicAppRunHistory</span><span class="sxs-lookup"><span data-stu-id="a24e0-139">Get-AzureRmLogicAppRunHistory</span></span>](./Get-AzureRmLogicAppRunHistory.md)

[<span data-ttu-id="a24e0-140">Stop-AzureRmLogicAppRun</span><span class="sxs-lookup"><span data-stu-id="a24e0-140">Stop-AzureRmLogicAppRun</span></span>](./Stop-AzureRmLogicAppRun.md)


