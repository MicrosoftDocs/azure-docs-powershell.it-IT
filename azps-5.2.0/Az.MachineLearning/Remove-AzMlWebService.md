---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 4a59508cc816f3301d76b1d982f52108247b50a3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346216"
---
# <span data-ttu-id="c88b1-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="c88b1-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="c88b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c88b1-102">SYNOPSIS</span></span>
<span data-ttu-id="c88b1-103">Elimina un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="c88b1-103">Deletes a web service.</span></span>

## <span data-ttu-id="c88b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c88b1-104">SYNTAX</span></span>

### <span data-ttu-id="c88b1-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c88b1-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c88b1-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="c88b1-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c88b1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c88b1-107">DESCRIPTION</span></span>
<span data-ttu-id="c88b1-108">Elimina un servizio Web di apprendimento di Azure machine a cui fa riferimento il nome e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c88b1-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="c88b1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c88b1-109">EXAMPLES</span></span>

### <span data-ttu-id="c88b1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c88b1-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="c88b1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c88b1-111">PARAMETERS</span></span>

### <span data-ttu-id="c88b1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c88b1-112">-DefaultProfile</span></span>
<span data-ttu-id="c88b1-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c88b1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c88b1-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c88b1-114">-Force</span></span>
<span data-ttu-id="c88b1-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="c88b1-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c88b1-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="c88b1-116">-MlWebService</span></span>
<span data-ttu-id="c88b1-117">Il servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c88b1-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="c88b1-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c88b1-118">-Name</span></span>
<span data-ttu-id="c88b1-119">Nome del servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c88b1-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="c88b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c88b1-120">-ResourceGroupName</span></span>
<span data-ttu-id="c88b1-121">Gruppo risorse del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="c88b1-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="c88b1-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c88b1-122">-Confirm</span></span>
<span data-ttu-id="c88b1-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c88b1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c88b1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c88b1-124">-WhatIf</span></span>
<span data-ttu-id="c88b1-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c88b1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c88b1-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c88b1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c88b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c88b1-127">CommonParameters</span></span>
<span data-ttu-id="c88b1-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c88b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c88b1-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c88b1-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c88b1-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c88b1-130">INPUTS</span></span>

### <span data-ttu-id="c88b1-131">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="c88b1-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="c88b1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c88b1-132">OUTPUTS</span></span>

### <span data-ttu-id="c88b1-133">System. void</span><span class="sxs-lookup"><span data-stu-id="c88b1-133">System.Void</span></span>

## <span data-ttu-id="c88b1-134">Note</span><span class="sxs-lookup"><span data-stu-id="c88b1-134">NOTES</span></span>
<span data-ttu-id="c88b1-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="c88b1-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c88b1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c88b1-136">RELATED LINKS</span></span>
