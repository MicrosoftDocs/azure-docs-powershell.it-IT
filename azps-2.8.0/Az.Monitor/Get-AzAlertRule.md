---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 9e1a0035a9736ac01963d150f06db9e510e51e17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673817"
---
# <span data-ttu-id="468e3-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="468e3-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="468e3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="468e3-102">SYNOPSIS</span></span>
<span data-ttu-id="468e3-103">Ottiene le regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="468e3-103">Gets alert rules.</span></span>

## <span data-ttu-id="468e3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="468e3-104">SYNTAX</span></span>

### <span data-ttu-id="468e3-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="468e3-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="468e3-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="468e3-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="468e3-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="468e3-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="468e3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="468e3-108">DESCRIPTION</span></span>
<span data-ttu-id="468e3-109">Il cmdlet **Get-AzAlertRule** ottiene una regola di avviso in base al nome o all'URI o a tutte le regole di avviso di un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="468e3-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="468e3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="468e3-110">EXAMPLES</span></span>

### <span data-ttu-id="468e3-111">Esempio 1: ottenere regole di avviso per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="468e3-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="468e3-112">Questo comando consente di ottenere tutte le regole di avviso per il gruppo di risorse denominato Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="468e3-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="468e3-113">L'output non contiene dettagli sulle regole perché il parametro *DetailedOutput* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="468e3-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="468e3-114">Esempio 2: ottenere una regola di avviso per nome</span><span class="sxs-lookup"><span data-stu-id="468e3-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="468e3-115">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="468e3-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="468e3-116">Dato che il parametro *DetailedOutput* non è specificato, l'output contiene solo informazioni di base sulla regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="468e3-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="468e3-117">Esempio 3: ottenere una regola di avviso per nome con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="468e3-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="468e3-118">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="468e3-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="468e3-119">Il parametro *DetailedOutput* è specificato, quindi l'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="468e3-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="468e3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="468e3-120">PARAMETERS</span></span>

### <span data-ttu-id="468e3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="468e3-121">-DefaultProfile</span></span>
<span data-ttu-id="468e3-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="468e3-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="468e3-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="468e3-123">-DetailedOutput</span></span>
<span data-ttu-id="468e3-124">Visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="468e3-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="468e3-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="468e3-125">-Name</span></span>
<span data-ttu-id="468e3-126">Specifica il nome della regola di avviso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="468e3-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="468e3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="468e3-127">-ResourceGroupName</span></span>
<span data-ttu-id="468e3-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="468e3-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="468e3-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="468e3-129">-TargetResourceId</span></span>
<span data-ttu-id="468e3-130">Specifica l'ID della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="468e3-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="468e3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="468e3-131">CommonParameters</span></span>
<span data-ttu-id="468e3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="468e3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="468e3-133">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="468e3-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="468e3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="468e3-134">INPUTS</span></span>

### <span data-ttu-id="468e3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="468e3-135">System.String</span></span>

### <span data-ttu-id="468e3-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="468e3-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="468e3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="468e3-137">OUTPUTS</span></span>

### <span data-ttu-id="468e3-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="468e3-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="468e3-139">Note</span><span class="sxs-lookup"><span data-stu-id="468e3-139">NOTES</span></span>

## <span data-ttu-id="468e3-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="468e3-140">RELATED LINKS</span></span>

[<span data-ttu-id="468e3-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="468e3-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="468e3-142">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="468e3-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="468e3-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="468e3-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="468e3-144">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="468e3-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="468e3-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="468e3-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


