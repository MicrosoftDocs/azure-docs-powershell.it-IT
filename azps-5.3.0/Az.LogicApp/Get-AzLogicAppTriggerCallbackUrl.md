---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F523CFA0-427B-41AF-9C2D-EB54EC96C04B
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azlogicapptriggercallbackurl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzLogicAppTriggerCallbackUrl.md
ms.openlocfilehash: 8f45141fc937710a5369ebfac208705ca1ee3ba3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386217"
---
# <span data-ttu-id="b5cc3-101">Get-AzLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b5cc3-101">Get-AzLogicAppTriggerCallbackUrl</span></span>

## <span data-ttu-id="b5cc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b5cc3-102">SYNOPSIS</span></span>
<span data-ttu-id="b5cc3-103">Ottiene un URL di callback del trigger dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-103">Gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="b5cc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b5cc3-104">SYNTAX</span></span>

```
Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName <String> -Name <String> -TriggerName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5cc3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b5cc3-105">DESCRIPTION</span></span>
<span data-ttu-id="b5cc3-106">Il cmdlet **Get-AzLogicAppTriggerCallbackUrl** ottiene un URL di callback del trigger dell'app logica da un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-106">The **Get-AzLogicAppTriggerCallbackUrl** cmdlet gets a Logic App trigger callback URL from a resource group.</span></span>
<span data-ttu-id="b5cc3-107">Questo cmdlet restituisce un oggetto **WorkflowTriggerCallbackUrl** che rappresenta l'URL di callback.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-107">This cmdlet returns a **WorkflowTriggerCallbackUrl** object that represents the callback URL.</span></span>
<span data-ttu-id="b5cc3-108">Specificare il nome del gruppo di risorse, il nome dell'app logica e il nome del trigger.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-108">Specify the resource group name, logic app name, and trigger name.</span></span>
<span data-ttu-id="b5cc3-109">Questo modulo supporta i parametri dinamici.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b5cc3-110">Per usare un parametro dinamico, digitarlo nel comando.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b5cc3-111">Per individuare i nomi dei parametri dinamici, digitare un segno meno (-) dopo il nome del cmdlet e quindi premere ripetutamente TAB per spostarsi tra i parametri disponibili.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b5cc3-112">Se si omette un parametro di modello obbligatorio, il cmdlet richiede il valore.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b5cc3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b5cc3-113">EXAMPLES</span></span>

### <span data-ttu-id="b5cc3-114">Esempio 1: ottenere un URL di callback del trigger dell'app logica</span><span class="sxs-lookup"><span data-stu-id="b5cc3-114">Example 1: Get a Logic App trigger callback URL</span></span>
```
PS C:\>Get-AzLogicAppTriggerCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "LogicApp1" -TriggerName "manual"
Value                                                                                                                                                                                                               
-----                                                                                                                                                                                                               
https://prod-03.westus.logic.azure.com:443/workflows/c4ed9335bc864140a11f4508d19acea3/triggers/manual/run?api-version=2016-06-01&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=<value>
```

<span data-ttu-id="b5cc3-115">Questo comando consente di ottenere un URL di callback dell'app logica.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-115">This command gets a Logic App trigger callback URL.</span></span>

## <span data-ttu-id="b5cc3-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b5cc3-116">PARAMETERS</span></span>

### <span data-ttu-id="b5cc3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5cc3-117">-DefaultProfile</span></span>
<span data-ttu-id="b5cc3-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b5cc3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5cc3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5cc3-119">-Name</span></span>
<span data-ttu-id="b5cc3-120">Specifica il nome di un'app logica.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-120">Specifies the name of a logic app.</span></span>

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

### <span data-ttu-id="b5cc3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5cc3-121">-ResourceGroupName</span></span>
<span data-ttu-id="b5cc3-122">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b5cc3-123">-Triggername</span><span class="sxs-lookup"><span data-stu-id="b5cc3-123">-TriggerName</span></span>
<span data-ttu-id="b5cc3-124">Specifica il nome di un trigger.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-124">Specifies the name of a trigger.</span></span>

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

### <span data-ttu-id="b5cc3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5cc3-125">CommonParameters</span></span>
<span data-ttu-id="b5cc3-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5cc3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5cc3-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5cc3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5cc3-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b5cc3-128">INPUTS</span></span>

### <span data-ttu-id="b5cc3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b5cc3-129">System.String</span></span>

## <span data-ttu-id="b5cc3-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b5cc3-130">OUTPUTS</span></span>

### <span data-ttu-id="b5cc3-131">Microsoft. Azure. Management. Logic. Models. WorkflowTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b5cc3-131">Microsoft.Azure.Management.Logic.Models.WorkflowTriggerCallbackUrl</span></span>

## <span data-ttu-id="b5cc3-132">Note</span><span class="sxs-lookup"><span data-stu-id="b5cc3-132">NOTES</span></span>

## <span data-ttu-id="b5cc3-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b5cc3-133">RELATED LINKS</span></span>

[<span data-ttu-id="b5cc3-134">Get-AzIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="b5cc3-134">Get-AzIntegrationAccountCallbackUrl</span></span>](./Get-AzIntegrationAccountCallbackUrl.md)


