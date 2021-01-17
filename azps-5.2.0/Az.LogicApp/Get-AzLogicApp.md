---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicApp.md
ms.openlocfilehash: ca0871dae696425c7f19ac1924aa0b725d0dac6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332572"
---
# <span data-ttu-id="117c6-101">Get-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="117c6-101">Get-AzLogicApp</span></span>

## <span data-ttu-id="117c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="117c6-102">SYNOPSIS</span></span>
<span data-ttu-id="117c6-103">Ottiene un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="117c6-103">Gets a logic app from a resource group.</span></span>

## <span data-ttu-id="117c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="117c6-104">SYNTAX</span></span>

### <span data-ttu-id="117c6-105">ListWorkflows (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="117c6-105">ListWorkflows (Default)</span></span>
```
Get-AzLogicApp [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="117c6-106">GetByVersion</span><span class="sxs-lookup"><span data-stu-id="117c6-106">GetByVersion</span></span>
```
Get-AzLogicApp -ResourceGroupName <String> -Name <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="117c6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="117c6-107">DESCRIPTION</span></span>
<span data-ttu-id="117c6-108">Il cmdlet **Get-AzLogicApp** ottiene un'app logica.</span><span class="sxs-lookup"><span data-stu-id="117c6-108">The **Get-AzLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="117c6-109">Questo cmdlet restituisce un oggetto **flusso di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="117c6-109">This cmdlet returns a **Workflow** object.</span></span>
<span data-ttu-id="117c6-110">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="117c6-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="117c6-111">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="117c6-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="117c6-112">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="117c6-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="117c6-113">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="117c6-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="117c6-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="117c6-114">EXAMPLES</span></span>

### <span data-ttu-id="117c6-115">Esempio 1: ottenere un'app logica da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="117c6-115">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
Id                           : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/LogicAppCmdletTest/providers/Microsoft.Logic/workflows/LogicApp03
Name                         : LogicApp03
Type                         : Microsoft.Logic/workflows
Location                     : westus
ChangedTime                  : 1/13/2016 2:41:39 PM
CreatedTime                  : 1/13/2016 2:41:39 PM
AccessEndpoint               : https://westus.logic.azure.com:443/subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourcegroups/ResourceGroup11/providers/Microsoft.Logic/workflows/LogicApp03
State                        : Enabled
DefinitionLinkUri            : 
DefinitionLinkContentVersion : 
Definition                   : {$schema, contentVersion, parameters, triggers...} 
ParametersLinkUri            : 
ParametersLinkContentVersion : 
Parameters                   : {[destinationUri, Microsoft.Azure.Management.Logic.Models.WorkflowParameter]} 
SkuName                      : Standard
PlanName                     : StandardServicePlan
PlanType                     : Microsoft.Web/ServerFarms
PlanId                       : /subscriptions/57b7034d-72d4-433d-ace2-a7460aed6a99/resourceGroups/ResourceGroup11/providers/Microsoft.Web/serverfarms/StandardServicePlan
Version                      : 08587489107859952120
```

<span data-ttu-id="117c6-116">Questo comando consente di ottenere un'app logica dal gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="117c6-116">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="117c6-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="117c6-117">PARAMETERS</span></span>

### <span data-ttu-id="117c6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="117c6-118">-DefaultProfile</span></span>
<span data-ttu-id="117c6-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="117c6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="117c6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="117c6-120">-Name</span></span>
<span data-ttu-id="117c6-121">Specifica il nome dell'app logica ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="117c6-121">Specifies the name of the logic app that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="117c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="117c6-123">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene un'app logica.</span><span class="sxs-lookup"><span data-stu-id="117c6-123">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWorkflows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="117c6-124">-Versione</span><span class="sxs-lookup"><span data-stu-id="117c6-124">-Version</span></span>
<span data-ttu-id="117c6-125">Specifica la versione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="117c6-125">Specifies the version of a logic app.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="117c6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="117c6-126">CommonParameters</span></span>
<span data-ttu-id="117c6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="117c6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="117c6-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="117c6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="117c6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="117c6-129">INPUTS</span></span>

### <span data-ttu-id="117c6-130">System. String</span><span class="sxs-lookup"><span data-stu-id="117c6-130">System.String</span></span>

## <span data-ttu-id="117c6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="117c6-131">OUTPUTS</span></span>

### <span data-ttu-id="117c6-132">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="117c6-132">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

### <span data-ttu-id="117c6-133">Microsoft. Azure. Management. Logic. Models. WorkflowVersion</span><span class="sxs-lookup"><span data-stu-id="117c6-133">Microsoft.Azure.Management.Logic.Models.WorkflowVersion</span></span>

## <span data-ttu-id="117c6-134">Note</span><span class="sxs-lookup"><span data-stu-id="117c6-134">NOTES</span></span>

## <span data-ttu-id="117c6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="117c6-135">RELATED LINKS</span></span>

[<span data-ttu-id="117c6-136">New-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="117c6-136">New-AzLogicApp</span></span>](./New-AzLogicApp.md)

[<span data-ttu-id="117c6-137">Remove-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="117c6-137">Remove-AzLogicApp</span></span>](./Remove-AzLogicApp.md)

[<span data-ttu-id="117c6-138">Set-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="117c6-138">Set-AzLogicApp</span></span>](./Set-AzLogicApp.md)

[<span data-ttu-id="117c6-139">Start-AzLogicApp</span><span class="sxs-lookup"><span data-stu-id="117c6-139">Start-AzLogicApp</span></span>](./Start-AzLogicApp.md)


