---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521628"
---
# <span data-ttu-id="b30c3-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b30c3-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="b30c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b30c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b30c3-103">Ottiene le regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="b30c3-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b30c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b30c3-104">SYNTAX</span></span>

### <span data-ttu-id="b30c3-105">Parametri per il cmdlet Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b30c3-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b30c3-106">Parametri per Get-AzureRmAlertRule cmdlet con nome</span><span class="sxs-lookup"><span data-stu-id="b30c3-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b30c3-107">Parametri per Get-AzureRmAlertRule cmdlet con URI della risorsa di destinazione</span><span class="sxs-lookup"><span data-stu-id="b30c3-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b30c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b30c3-108">DESCRIPTION</span></span>
<span data-ttu-id="b30c3-109">Il cmdlet **Get-AzureRmAlertRule** ottiene una regola di avviso in base al nome o all'URI o a tutte le regole di avviso di un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="b30c3-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="b30c3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b30c3-110">EXAMPLES</span></span>

### <span data-ttu-id="b30c3-111">Esempio 1: ottenere regole di avviso per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b30c3-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="b30c3-112">Questo comando consente di ottenere tutte le regole di avviso per il gruppo di risorse denominato Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="b30c3-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="b30c3-113">L'output non contiene dettagli sulle regole perché il parametro *DetailedOutput* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="b30c3-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="b30c3-114">Esempio 2: ottenere una regola di avviso per nome</span><span class="sxs-lookup"><span data-stu-id="b30c3-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="b30c3-115">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="b30c3-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b30c3-116">Dato che il parametro *DetailedOutput* non è specificato, l'output contiene solo informazioni di base sulla regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="b30c3-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="b30c3-117">Esempio 3: ottenere una regola di avviso per nome con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="b30c3-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="b30c3-118">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="b30c3-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="b30c3-119">Il parametro *DetailedOutput* è specificato, quindi l'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="b30c3-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="b30c3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b30c3-120">PARAMETERS</span></span>

### <span data-ttu-id="b30c3-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="b30c3-121">-DetailedOutput</span></span>
<span data-ttu-id="b30c3-122">Visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="b30c3-122">Displays full details in the output.</span></span>

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

### <span data-ttu-id="b30c3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="b30c3-123">-Name</span></span>
<span data-ttu-id="b30c3-124">Specifica il nome della regola di avviso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b30c3-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b30c3-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b30c3-125">-ResourceGroup</span></span>
<span data-ttu-id="b30c3-126">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b30c3-126">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b30c3-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b30c3-127">-TargetResourceId</span></span>
<span data-ttu-id="b30c3-128">Specifica l'ID della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b30c3-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b30c3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b30c3-129">-DefaultProfile</span></span>
<span data-ttu-id="b30c3-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b30c3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b30c3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30c3-131">CommonParameters</span></span>
<span data-ttu-id="b30c3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b30c3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30c3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30c3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30c3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b30c3-134">INPUTS</span></span>

## <span data-ttu-id="b30c3-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b30c3-135">OUTPUTS</span></span>

### <span data-ttu-id="b30c3-136">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSManagementItemDescriptor]</span><span class="sxs-lookup"><span data-stu-id="b30c3-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="b30c3-137">Note</span><span class="sxs-lookup"><span data-stu-id="b30c3-137">NOTES</span></span>

## <span data-ttu-id="b30c3-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b30c3-138">RELATED LINKS</span></span>

[<span data-ttu-id="b30c3-139">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b30c3-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="b30c3-140">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b30c3-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b30c3-141">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b30c3-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b30c3-142">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b30c3-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b30c3-143">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="b30c3-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


