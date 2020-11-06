---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 672ab7a3c802ae8165b29c69ffb6c3f63310cc89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516611"
---
# <span data-ttu-id="eef81-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="eef81-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="eef81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eef81-102">SYNOPSIS</span></span>
<span data-ttu-id="eef81-103">Ottiene le regole di avviso.</span><span class="sxs-lookup"><span data-stu-id="eef81-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eef81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eef81-104">SYNTAX</span></span>

### <span data-ttu-id="eef81-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="eef81-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eef81-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="eef81-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eef81-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="eef81-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eef81-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eef81-108">DESCRIPTION</span></span>
<span data-ttu-id="eef81-109">Il cmdlet **Get-AzureRmAlertRule** ottiene una regola di avviso in base al nome o all'URI o a tutte le regole di avviso di un gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="eef81-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="eef81-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eef81-110">EXAMPLES</span></span>

### <span data-ttu-id="eef81-111">Esempio 1: ottenere regole di avviso per un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="eef81-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="eef81-112">Questo comando consente di ottenere tutte le regole di avviso per il gruppo di risorse denominato Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="eef81-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="eef81-113">L'output non contiene dettagli sulle regole perché il parametro *DetailedOutput* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="eef81-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="eef81-114">Esempio 2: ottenere una regola di avviso per nome</span><span class="sxs-lookup"><span data-stu-id="eef81-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="eef81-115">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="eef81-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="eef81-116">Dato che il parametro *DetailedOutput* non è specificato, l'output contiene solo informazioni di base sulla regola di avviso.</span><span class="sxs-lookup"><span data-stu-id="eef81-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="eef81-117">Esempio 3: ottenere una regola di avviso per nome con l'output dettagliato</span><span class="sxs-lookup"><span data-stu-id="eef81-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="eef81-118">Questo comando consente di ottenere la regola di avviso denominata avviso-7da64548-214d-42CA-B12B-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="eef81-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="eef81-119">Il parametro *DetailedOutput* è specificato, quindi l'output è dettagliato.</span><span class="sxs-lookup"><span data-stu-id="eef81-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="eef81-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eef81-120">PARAMETERS</span></span>

### <span data-ttu-id="eef81-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eef81-121">-DefaultProfile</span></span>
<span data-ttu-id="eef81-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eef81-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eef81-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="eef81-123">-DetailedOutput</span></span>
<span data-ttu-id="eef81-124">Visualizza tutti i dettagli nell'output.</span><span class="sxs-lookup"><span data-stu-id="eef81-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="eef81-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="eef81-125">-Name</span></span>
<span data-ttu-id="eef81-126">Specifica il nome della regola di avviso da ottenere.</span><span class="sxs-lookup"><span data-stu-id="eef81-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="eef81-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eef81-127">-ResourceGroupName</span></span>
<span data-ttu-id="eef81-128">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="eef81-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="eef81-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="eef81-129">-TargetResourceId</span></span>
<span data-ttu-id="eef81-130">Specifica l'ID della risorsa di destinazione.</span><span class="sxs-lookup"><span data-stu-id="eef81-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="eef81-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eef81-131">CommonParameters</span></span>
<span data-ttu-id="eef81-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eef81-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eef81-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eef81-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eef81-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eef81-134">INPUTS</span></span>

### <span data-ttu-id="eef81-135">System. String</span><span class="sxs-lookup"><span data-stu-id="eef81-135">System.String</span></span>

### <span data-ttu-id="eef81-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="eef81-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="eef81-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eef81-137">OUTPUTS</span></span>

### <span data-ttu-id="eef81-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="eef81-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="eef81-139">Note</span><span class="sxs-lookup"><span data-stu-id="eef81-139">NOTES</span></span>

## <span data-ttu-id="eef81-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eef81-140">RELATED LINKS</span></span>

[<span data-ttu-id="eef81-141">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="eef81-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="eef81-142">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="eef81-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="eef81-143">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="eef81-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="eef81-144">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="eef81-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="eef81-145">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="eef81-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)

