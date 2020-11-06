---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: c1d6ae6c1396e23398bc1b52f4f32458999072a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516519"
---
# <span data-ttu-id="38388-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="38388-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="38388-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38388-102">SYNOPSIS</span></span>
<span data-ttu-id="38388-103">Elimina un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="38388-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38388-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38388-104">SYNTAX</span></span>

### <span data-ttu-id="38388-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="38388-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38388-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="38388-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38388-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38388-107">DESCRIPTION</span></span>
<span data-ttu-id="38388-108">Elimina un servizio Web di apprendimento di Azure machine a cui fa riferimento il nome e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="38388-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="38388-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38388-109">EXAMPLES</span></span>

### <span data-ttu-id="38388-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38388-110">Example 1</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="38388-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38388-111">PARAMETERS</span></span>

### <span data-ttu-id="38388-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38388-112">-DefaultProfile</span></span>
<span data-ttu-id="38388-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="38388-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38388-114">-Force</span><span class="sxs-lookup"><span data-stu-id="38388-114">-Force</span></span>
<span data-ttu-id="38388-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="38388-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="38388-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="38388-116">-MlWebService</span></span>
<span data-ttu-id="38388-117">Il servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="38388-117">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38388-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="38388-118">-Name</span></span>
<span data-ttu-id="38388-119">Nome del servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="38388-119">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38388-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38388-120">-ResourceGroupName</span></span>
<span data-ttu-id="38388-121">Gruppo risorse del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="38388-121">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38388-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38388-122">-Confirm</span></span>
<span data-ttu-id="38388-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38388-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38388-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38388-124">-WhatIf</span></span>
<span data-ttu-id="38388-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38388-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38388-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38388-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38388-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38388-127">CommonParameters</span></span>
<span data-ttu-id="38388-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38388-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38388-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38388-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38388-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38388-130">INPUTS</span></span>

### <span data-ttu-id="38388-131">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="38388-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="38388-132">Parametri: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38388-132">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="38388-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38388-133">OUTPUTS</span></span>

### <span data-ttu-id="38388-134">System. void</span><span class="sxs-lookup"><span data-stu-id="38388-134">System.Void</span></span>

## <span data-ttu-id="38388-135">Note</span><span class="sxs-lookup"><span data-stu-id="38388-135">NOTES</span></span>
<span data-ttu-id="38388-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="38388-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="38388-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38388-137">RELATED LINKS</span></span>