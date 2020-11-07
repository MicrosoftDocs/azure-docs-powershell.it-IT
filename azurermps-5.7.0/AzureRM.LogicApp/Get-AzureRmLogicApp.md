---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 7BFCD982-EC80-418B-BB52-C9941D028F76
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermlogicapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmLogicApp.md
ms.openlocfilehash: 3faa9ce82806da0e2f058f3d1bcaeba3862c27c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686729"
---
# <span data-ttu-id="39603-101">Get-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="39603-101">Get-AzureRmLogicApp</span></span>

## <span data-ttu-id="39603-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39603-102">SYNOPSIS</span></span>
<span data-ttu-id="39603-103">Ottiene un'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39603-103">Gets a logic app from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39603-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39603-104">SYNTAX</span></span>

```
Get-AzureRmLogicApp -ResourceGroupName <String> -Name <String> [-Version <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39603-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39603-105">DESCRIPTION</span></span>
<span data-ttu-id="39603-106">Il cmdlet **Get-AzureRmLogicApp** ottiene un'app logica.</span><span class="sxs-lookup"><span data-stu-id="39603-106">The **Get-AzureRmLogicApp** cmdlet gets a logic app.</span></span>
<span data-ttu-id="39603-107">Questo cmdlet restituisce un oggetto **flusso di lavoro** .</span><span class="sxs-lookup"><span data-stu-id="39603-107">This cmdlet returns a **Workflow** object.</span></span>

<span data-ttu-id="39603-108">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="39603-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="39603-109">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="39603-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="39603-110">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="39603-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="39603-111">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="39603-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="39603-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39603-112">EXAMPLES</span></span>

### <span data-ttu-id="39603-113">Esempio 1: ottenere un'app logica da un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="39603-113">Example 1: Get a logic app from a resource group</span></span>
```
PS C:\>Get-AzureRmLogicApp -ResourceGroupName "ResourceGroup11" -Name "LogicApp03"
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

<span data-ttu-id="39603-114">Questo comando consente di ottenere un'app logica dal gruppo di risorse denominato ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="39603-114">This command gets a logic app from the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="39603-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39603-115">PARAMETERS</span></span>

### <span data-ttu-id="39603-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39603-116">-DefaultProfile</span></span>
<span data-ttu-id="39603-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="39603-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39603-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="39603-118">-Name</span></span>
<span data-ttu-id="39603-119">Specifica il nome dell'app logica ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39603-119">Specifies the name of the logic app that this cmdlet gets.</span></span>

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

### <span data-ttu-id="39603-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39603-120">-ResourceGroupName</span></span>
<span data-ttu-id="39603-121">Specifica il nome di un gruppo di risorse in cui questo cmdlet ottiene un'app logica.</span><span class="sxs-lookup"><span data-stu-id="39603-121">Specifies the name for a resource group in which this cmdlet gets a logic app.</span></span>

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

### <span data-ttu-id="39603-122">-Versione</span><span class="sxs-lookup"><span data-stu-id="39603-122">-Version</span></span>
<span data-ttu-id="39603-123">Specifica la versione di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="39603-123">Specifies the version of a logic app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39603-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39603-124">CommonParameters</span></span>
<span data-ttu-id="39603-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39603-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39603-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39603-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39603-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39603-127">INPUTS</span></span>

### <span data-ttu-id="39603-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="39603-128">None</span></span>
<span data-ttu-id="39603-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="39603-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="39603-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39603-130">OUTPUTS</span></span>

### <span data-ttu-id="39603-131">Microsoft. Azure. Management. Logic. Models. Workflow</span><span class="sxs-lookup"><span data-stu-id="39603-131">Microsoft.Azure.Management.Logic.Models.Workflow</span></span>

## <span data-ttu-id="39603-132">Note</span><span class="sxs-lookup"><span data-stu-id="39603-132">NOTES</span></span>

## <span data-ttu-id="39603-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39603-133">RELATED LINKS</span></span>

[<span data-ttu-id="39603-134">New-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="39603-134">New-AzureRmLogicApp</span></span>](./New-AzureRmLogicApp.md)

[<span data-ttu-id="39603-135">Remove-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="39603-135">Remove-AzureRmLogicApp</span></span>](./Remove-AzureRmLogicApp.md)

[<span data-ttu-id="39603-136">Set-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="39603-136">Set-AzureRmLogicApp</span></span>](./Set-AzureRmLogicApp.md)

[<span data-ttu-id="39603-137">Start-AzureRmLogicApp</span><span class="sxs-lookup"><span data-stu-id="39603-137">Start-AzureRmLogicApp</span></span>](./Start-AzureRmLogicApp.md)

