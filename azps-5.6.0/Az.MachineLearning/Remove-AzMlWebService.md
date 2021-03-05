---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/remove-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlWebService.md
ms.openlocfilehash: 46e9ae8f4b6b4bb954bca158adb82c0d821d67eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006701"
---
# <span data-ttu-id="0041a-101">Remove-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="0041a-101">Remove-AzMlWebService</span></span>

## <span data-ttu-id="0041a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0041a-102">SYNOPSIS</span></span>
<span data-ttu-id="0041a-103">Elimina un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="0041a-103">Deletes a web service.</span></span>

## <span data-ttu-id="0041a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0041a-104">SYNTAX</span></span>

### <span data-ttu-id="0041a-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="0041a-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0041a-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="0041a-106">RemoveByObject</span></span>
```
Remove-AzMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0041a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0041a-107">DESCRIPTION</span></span>
<span data-ttu-id="0041a-108">Elimina un servizio Web Azure Machine Learning a cui fa riferimento il gruppo di risorse e il nome.</span><span class="sxs-lookup"><span data-stu-id="0041a-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="0041a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0041a-109">EXAMPLES</span></span>

### <span data-ttu-id="0041a-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0041a-110">Example 1</span></span>
```
Remove-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="0041a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0041a-111">PARAMETERS</span></span>

### <span data-ttu-id="0041a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0041a-112">-DefaultProfile</span></span>
<span data-ttu-id="0041a-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0041a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0041a-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0041a-114">-Force</span></span>
<span data-ttu-id="0041a-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="0041a-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0041a-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="0041a-116">-MlWebService</span></span>
<span data-ttu-id="0041a-117">Il servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0041a-117">The web service to be removed.</span></span>

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

### <span data-ttu-id="0041a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0041a-118">-Name</span></span>
<span data-ttu-id="0041a-119">Nome del servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0041a-119">The name of the web service to be removed.</span></span>

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

### <span data-ttu-id="0041a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0041a-120">-ResourceGroupName</span></span>
<span data-ttu-id="0041a-121">Gruppo di risorse del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="0041a-121">The resource group of the web service.</span></span>

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

### <span data-ttu-id="0041a-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0041a-122">-Confirm</span></span>
<span data-ttu-id="0041a-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0041a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0041a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0041a-124">-WhatIf</span></span>
<span data-ttu-id="0041a-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0041a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0041a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0041a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0041a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0041a-127">CommonParameters</span></span>
<span data-ttu-id="0041a-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0041a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0041a-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0041a-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0041a-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="0041a-130">INPUTS</span></span>

### <span data-ttu-id="0041a-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="0041a-131">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="0041a-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0041a-132">OUTPUTS</span></span>

### <span data-ttu-id="0041a-133">System.Void</span><span class="sxs-lookup"><span data-stu-id="0041a-133">System.Void</span></span>

## <span data-ttu-id="0041a-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="0041a-134">NOTES</span></span>
<span data-ttu-id="0041a-135">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="0041a-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="0041a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0041a-136">RELATED LINKS</span></span>
