---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867100"
---
# <span data-ttu-id="7bbc9-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7bbc9-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="7bbc9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7bbc9-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbc9-103">Ottiene le regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7bbc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bbc9-104">SYNTAX</span></span>

### <span data-ttu-id="7bbc9-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7bbc9-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7bbc9-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="7bbc9-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7bbc9-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="7bbc9-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7bbc9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bbc9-108">DESCRIPTION</span></span>
<span data-ttu-id="7bbc9-109">Il cmdlet **Get-AzureRmAlertRule** ottiene una regola di avviso in base al nome o all'URI o a tutte le regole di avviso di un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="7bbc9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bbc9-110">EXAMPLES</span></span>

### <span data-ttu-id="7bbc9-111">Esempio 1: ottenere regole di avviso per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7bbc9-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="7bbc9-112">Questo comando consente di ottenere tutte le regole di avviso per il gruppo di risorse denominato Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="7bbc9-113">L'output non contiene dettagli sulle regole perché il parametro *DetailedOutput* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="7bbc9-114">Esempio 2: ottenere una regola di avviso per nome</span><span class="sxs-lookup"><span data-stu-id="7bbc9-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="7bbc9-115">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="7bbc9-116">Dato che il parametro *DetailedOutput* non è specificato, l'output contiene solo informazioni di base sulla regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="7bbc9-117">Esempio 3: ottenere una regola di avviso per nome con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="7bbc9-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="7bbc9-118">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="7bbc9-119">Il parametro *DetailedOutput* è specificato, quindi l'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="7bbc9-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7bbc9-120">PARAMETERS</span></span>

### <span data-ttu-id="7bbc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbc9-121">-DefaultProfile</span></span>
<span data-ttu-id="7bbc9-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7bbc9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bbc9-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="7bbc9-123">-DetailedOutput</span></span>
<span data-ttu-id="7bbc9-124">Visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="7bbc9-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="7bbc9-125">-Name</span></span>
<span data-ttu-id="7bbc9-126">Specifica il nome della regola di avviso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="7bbc9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bbc9-127">-ResourceGroupName</span></span>
<span data-ttu-id="7bbc9-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="7bbc9-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="7bbc9-129">-TargetResourceId</span></span>
<span data-ttu-id="7bbc9-130">Specifica l'ID della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="7bbc9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbc9-131">CommonParameters</span></span>
<span data-ttu-id="7bbc9-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bbc9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbc9-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bbc9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbc9-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7bbc9-134">INPUTS</span></span>

### <span data-ttu-id="7bbc9-135">System. String</span><span class="sxs-lookup"><span data-stu-id="7bbc9-135">System.String</span></span>

### <span data-ttu-id="7bbc9-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7bbc9-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7bbc9-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bbc9-137">OUTPUTS</span></span>

### <span data-ttu-id="7bbc9-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="7bbc9-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="7bbc9-139">Note</span><span class="sxs-lookup"><span data-stu-id="7bbc9-139">NOTES</span></span>

## <span data-ttu-id="7bbc9-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bbc9-140">RELATED LINKS</span></span>



[<span data-ttu-id="7bbc9-141">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7bbc9-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7bbc9-142">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7bbc9-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7bbc9-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7bbc9-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="7bbc9-144">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7bbc9-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


