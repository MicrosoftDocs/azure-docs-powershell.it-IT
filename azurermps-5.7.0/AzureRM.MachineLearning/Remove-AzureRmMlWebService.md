---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: 4d7365a2a7a8d11fc1032f182409bd462931be3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515659"
---
# <span data-ttu-id="34d26-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="34d26-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="34d26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="34d26-102">SYNOPSIS</span></span>
<span data-ttu-id="34d26-103">Elimina un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="34d26-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34d26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34d26-104">SYNTAX</span></span>

### <span data-ttu-id="34d26-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="34d26-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34d26-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="34d26-106">RemoveByObject</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34d26-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34d26-107">DESCRIPTION</span></span>
<span data-ttu-id="34d26-108">Elimina un servizio Web di apprendimento di Azure machine a cui fa riferimento il nome e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="34d26-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="34d26-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34d26-109">EXAMPLES</span></span>

### <span data-ttu-id="34d26-110">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="34d26-110">--------------------------  Example 1  --------------------------</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="34d26-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="34d26-111">PARAMETERS</span></span>

### <span data-ttu-id="34d26-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d26-112">-DefaultProfile</span></span>
<span data-ttu-id="34d26-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34d26-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d26-114">-Force</span><span class="sxs-lookup"><span data-stu-id="34d26-114">-Force</span></span>
<span data-ttu-id="34d26-115">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="34d26-115">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d26-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="34d26-116">-MlWebService</span></span>
<span data-ttu-id="34d26-117">Il servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="34d26-117">The web service to be removed.</span></span>

```yaml
Type: WebService
Parameter Sets: RemoveByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34d26-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="34d26-118">-Name</span></span>
<span data-ttu-id="34d26-119">Nome del servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="34d26-119">The name of the web service to be removed.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d26-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34d26-120">-ResourceGroupName</span></span>
<span data-ttu-id="34d26-121">Gruppo risorse del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="34d26-121">The resource group of the web service.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d26-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="34d26-122">-Confirm</span></span>
<span data-ttu-id="34d26-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34d26-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d26-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d26-124">-WhatIf</span></span>
<span data-ttu-id="34d26-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34d26-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d26-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34d26-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d26-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d26-127">CommonParameters</span></span>
<span data-ttu-id="34d26-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34d26-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d26-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34d26-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d26-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="34d26-130">INPUTS</span></span>

### <span data-ttu-id="34d26-131">Servizio</span><span class="sxs-lookup"><span data-stu-id="34d26-131">WebService</span></span>
<span data-ttu-id="34d26-132">Il parametro ' MlWebService ' accetta il valore di tipo ' WebService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="34d26-132">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="34d26-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34d26-133">OUTPUTS</span></span>

### <span data-ttu-id="34d26-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="34d26-134">None</span></span>

## <span data-ttu-id="34d26-135">Note</span><span class="sxs-lookup"><span data-stu-id="34d26-135">NOTES</span></span>
<span data-ttu-id="34d26-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="34d26-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="34d26-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34d26-137">RELATED LINKS</span></span>

