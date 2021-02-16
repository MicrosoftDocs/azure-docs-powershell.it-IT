---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/add-azmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Add-AzMlWebServiceRegionalProperty.md
ms.openlocfilehash: c9d7f205da9adbe199f2c8e33685612fd547feb7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190303"
---
# <span data-ttu-id="d1d0a-101">Add-AzMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="d1d0a-101">Add-AzMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="d1d0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d0a-103">Crea proprietà del servizio Web locale.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-103">Creates regional web service properties.</span></span>

## <span data-ttu-id="d1d0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1d0a-104">SYNTAX</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1d0a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d1d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="d1d0a-106">Crea le proprietà locali di Azure Machine Learning per un servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="d1d0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="d1d0a-108">Esempio 1: Aggiungere nuove proprietà internazionali per gli Stati Uniti centro ovest</span><span class="sxs-lookup"><span data-stu-id="d1d0a-108">Example 1: Add new regional properties for West Central US</span></span>

```
Add-AzMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="d1d0a-109">Questo comando di esempio crea una proprietà regionale per un servizio Web nell'area "Stati Uniti centro occidentale".</span><span class="sxs-lookup"><span data-stu-id="d1d0a-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="d1d0a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1d0a-110">PARAMETERS</span></span>

### <span data-ttu-id="d1d0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d0a-111">-DefaultProfile</span></span>
<span data-ttu-id="d1d0a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d1d0a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1d0a-113">-Force</span><span class="sxs-lookup"><span data-stu-id="d1d0a-113">-Force</span></span>
<span data-ttu-id="d1d0a-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-114">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d0a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d1d0a-115">-Name</span></span>
<span data-ttu-id="d1d0a-116">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-116">The name for the web service.</span></span>

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

### <span data-ttu-id="d1d0a-117">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="d1d0a-117">-Region</span></span>
<span data-ttu-id="d1d0a-118">Area in cui creare le proprietà del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-118">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1d0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1d0a-120">Gruppo di risorse a cui appartiene il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-120">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="d1d0a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1d0a-121">-Confirm</span></span>
<span data-ttu-id="d1d0a-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d0a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1d0a-123">-WhatIf</span></span>
<span data-ttu-id="d1d0a-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1d0a-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1d0a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d0a-126">CommonParameters</span></span>
<span data-ttu-id="d1d0a-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1d0a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d0a-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1d0a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d0a-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="d1d0a-129">INPUTS</span></span>

### <span data-ttu-id="d1d0a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d1d0a-130">System.String</span></span>

## <span data-ttu-id="d1d0a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1d0a-131">OUTPUTS</span></span>

### <span data-ttu-id="d1d0a-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="d1d0a-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="d1d0a-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="d1d0a-133">NOTES</span></span>
<span data-ttu-id="d1d0a-134">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="d1d0a-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="d1d0a-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1d0a-135">RELATED LINKS</span></span>
