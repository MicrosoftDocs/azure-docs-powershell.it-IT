---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 7164c1f37c3205e3bc2d71f2b820290217aff432
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403103"
---
# <span data-ttu-id="84e90-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="84e90-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="84e90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e90-102">SYNOPSIS</span></span>
<span data-ttu-id="84e90-103">Ottiene le regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="84e90-103">Gets alert rules.</span></span>

## <span data-ttu-id="84e90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="84e90-104">SYNTAX</span></span>

### <span data-ttu-id="84e90-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="84e90-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="84e90-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="84e90-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84e90-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="84e90-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84e90-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="84e90-108">DESCRIPTION</span></span>
<span data-ttu-id="84e90-109">Il cmdlet **Get-AzAlertRule** ottiene una regola di avviso in base al nome o all'URI oppure a tutte le regole di avviso da un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="84e90-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="84e90-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="84e90-110">EXAMPLES</span></span>

### <span data-ttu-id="84e90-111">Esempio 1: Ottenere regole di avviso per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="84e90-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="84e90-112">Questo comando recupera tutte le regole di avviso per il gruppo di risorse denominato Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="84e90-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="84e90-113">L'output non contiene dettagli sulle regole perché non è specificato il parametro *DetailedOutput.*</span><span class="sxs-lookup"><span data-stu-id="84e90-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="84e90-114">Esempio 2: Ottenere una regola di avviso in base al nome</span><span class="sxs-lookup"><span data-stu-id="84e90-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="84e90-115">Questo comando ottiene la regola di avviso denominata myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="84e90-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="84e90-116">Poiché il *parametro DetailedOutput* non è specificato, l'output contiene solo informazioni di base sulla regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="84e90-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="84e90-117">Esempio 3: Ottenere una regola di avviso per nome con output dettagliato</span><span class="sxs-lookup"><span data-stu-id="84e90-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="84e90-118">Questo comando ottiene la regola di avviso denominata myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="84e90-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="84e90-119">Il *parametro DetailedOutput* è specificato, quindi l'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="84e90-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="84e90-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84e90-120">PARAMETERS</span></span>

### <span data-ttu-id="84e90-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e90-121">-DefaultProfile</span></span>
<span data-ttu-id="84e90-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="84e90-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84e90-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="84e90-123">-DetailedOutput</span></span>
<span data-ttu-id="84e90-124">Visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="84e90-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="84e90-125">-Name</span><span class="sxs-lookup"><span data-stu-id="84e90-125">-Name</span></span>
<span data-ttu-id="84e90-126">Specifica il nome della regola di avviso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="84e90-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="84e90-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84e90-127">-ResourceGroupName</span></span>
<span data-ttu-id="84e90-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="84e90-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="84e90-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="84e90-129">-TargetResourceId</span></span>
<span data-ttu-id="84e90-130">Specifica l'ID della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="84e90-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="84e90-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e90-131">CommonParameters</span></span>
<span data-ttu-id="84e90-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e90-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e90-133">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e90-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e90-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="84e90-134">INPUTS</span></span>

### <span data-ttu-id="84e90-135">System.String</span><span class="sxs-lookup"><span data-stu-id="84e90-135">System.String</span></span>

### <span data-ttu-id="84e90-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="84e90-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="84e90-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="84e90-137">OUTPUTS</span></span>

### <span data-ttu-id="84e90-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="84e90-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="84e90-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="84e90-139">NOTES</span></span>

## <span data-ttu-id="84e90-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="84e90-140">RELATED LINKS</span></span>


[<span data-ttu-id="84e90-141">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="84e90-141">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="84e90-142">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="84e90-142">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="84e90-143">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="84e90-143">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="84e90-144">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="84e90-144">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


