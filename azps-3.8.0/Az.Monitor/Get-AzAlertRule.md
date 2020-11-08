---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022961"
---
# <span data-ttu-id="6c17c-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c17c-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="6c17c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6c17c-102">SYNOPSIS</span></span>
<span data-ttu-id="6c17c-103">Ottiene le regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="6c17c-103">Gets alert rules.</span></span>

## <span data-ttu-id="6c17c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6c17c-104">SYNTAX</span></span>

### <span data-ttu-id="6c17c-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6c17c-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6c17c-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="6c17c-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c17c-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="6c17c-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c17c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6c17c-108">DESCRIPTION</span></span>
<span data-ttu-id="6c17c-109">Il cmdlet **Get-AzAlertRule** ottiene una regola di avviso in base al nome o all'URI o a tutte le regole di avviso di un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="6c17c-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="6c17c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6c17c-110">EXAMPLES</span></span>

### <span data-ttu-id="6c17c-111">Esempio 1: ottenere regole di avviso per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6c17c-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="6c17c-112">Questo comando consente di ottenere tutte le regole di avviso per il gruppo di risorse denominato Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="6c17c-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="6c17c-113">L'output non contiene dettagli sulle regole perché il parametro *DetailedOutput* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="6c17c-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="6c17c-114">Esempio 2: ottenere una regola di avviso per nome</span><span class="sxs-lookup"><span data-stu-id="6c17c-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="6c17c-115">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="6c17c-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="6c17c-116">Dato che il parametro *DetailedOutput* non è specificato, l'output contiene solo informazioni di base sulla regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="6c17c-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="6c17c-117">Esempio 3: ottenere una regola di avviso per nome con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="6c17c-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="6c17c-118">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="6c17c-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="6c17c-119">Il parametro *DetailedOutput* è specificato, quindi l'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="6c17c-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="6c17c-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6c17c-120">PARAMETERS</span></span>

### <span data-ttu-id="6c17c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c17c-121">-DefaultProfile</span></span>
<span data-ttu-id="6c17c-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6c17c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c17c-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="6c17c-123">-DetailedOutput</span></span>
<span data-ttu-id="6c17c-124">Visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="6c17c-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c17c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c17c-125">-Name</span></span>
<span data-ttu-id="6c17c-126">Specifica il nome della regola di avviso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6c17c-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c17c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c17c-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c17c-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6c17c-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c17c-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="6c17c-129">-TargetResourceId</span></span>
<span data-ttu-id="6c17c-130">Specifica l'ID della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="6c17c-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c17c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c17c-131">CommonParameters</span></span>
<span data-ttu-id="6c17c-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c17c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c17c-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c17c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c17c-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6c17c-134">INPUTS</span></span>

### <span data-ttu-id="6c17c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6c17c-135">System.String</span></span>

### <span data-ttu-id="6c17c-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6c17c-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6c17c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6c17c-137">OUTPUTS</span></span>

### <span data-ttu-id="6c17c-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c17c-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="6c17c-139">Note</span><span class="sxs-lookup"><span data-stu-id="6c17c-139">NOTES</span></span>

## <span data-ttu-id="6c17c-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6c17c-140">RELATED LINKS</span></span>

[<span data-ttu-id="6c17c-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c17c-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="6c17c-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c17c-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="6c17c-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c17c-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="6c17c-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6c17c-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="6c17c-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="6c17c-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


