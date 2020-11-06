---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlWebService.md
ms.openlocfilehash: f05d4142efab5a95cfef43fbc44cf57d0e1e2cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519159"
---
# <span data-ttu-id="da58e-101">Remove-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="da58e-101">Remove-AzureRmMlWebService</span></span>

## <span data-ttu-id="da58e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="da58e-102">SYNOPSIS</span></span>
<span data-ttu-id="da58e-103">Elimina un servizio Web.</span><span class="sxs-lookup"><span data-stu-id="da58e-103">Deletes a web service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da58e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="da58e-104">SYNTAX</span></span>

### <span data-ttu-id="da58e-105">Rimuovere un servizio Web di Azure ML resouce per nome e gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="da58e-105">Remove an Azure ML web service resouce by name and resource group.</span></span>
```
Remove-AzureRmMlWebService -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="da58e-106">Rimuovere un servizio Web di Azure ML specificato come oggetto.</span><span class="sxs-lookup"><span data-stu-id="da58e-106">Remove an Azure ML web service specified as an object.</span></span>
```
Remove-AzureRmMlWebService -MlWebService <WebService> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da58e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="da58e-107">DESCRIPTION</span></span>
<span data-ttu-id="da58e-108">Elimina un servizio Web di apprendimento di Azure machine a cui fa riferimento il nome e il gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="da58e-108">Deletes a Azure Machine Learning web service referenced by resource group and name.</span></span>

## <span data-ttu-id="da58e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="da58e-109">EXAMPLES</span></span>

### <span data-ttu-id="da58e-110">--------------------------Esempio 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="da58e-110">--------------------------  Example 1  --------------------------</span></span>
<span data-ttu-id="da58e-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="da58e-111">@{paragraph=PS C:\\\>}</span></span>





```
Remove-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

## <span data-ttu-id="da58e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="da58e-112">PARAMETERS</span></span>

### <span data-ttu-id="da58e-113">-Force</span><span class="sxs-lookup"><span data-stu-id="da58e-113">-Force</span></span>
<span data-ttu-id="da58e-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="da58e-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="da58e-115">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="da58e-115">-MlWebService</span></span>
<span data-ttu-id="da58e-116">Il servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="da58e-116">The web service to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Remove an Azure ML web service specified as an object.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da58e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="da58e-117">-Name</span></span>
<span data-ttu-id="da58e-118">Nome del servizio Web da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="da58e-118">The name of the web service to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da58e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da58e-119">-ResourceGroupName</span></span>
<span data-ttu-id="da58e-120">Gruppo risorse del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="da58e-120">The resource group of the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove an Azure ML web service resouce by name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da58e-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="da58e-121">-Confirm</span></span>
<span data-ttu-id="da58e-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da58e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da58e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da58e-123">-WhatIf</span></span>
<span data-ttu-id="da58e-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da58e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da58e-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="da58e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da58e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da58e-126">-DefaultProfile</span></span>
<span data-ttu-id="da58e-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="da58e-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da58e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da58e-128">CommonParameters</span></span>
<span data-ttu-id="da58e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da58e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da58e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da58e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da58e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="da58e-131">INPUTS</span></span>

### <span data-ttu-id="da58e-132">Servizio</span><span class="sxs-lookup"><span data-stu-id="da58e-132">WebService</span></span>
<span data-ttu-id="da58e-133">Il parametro ' MlWebService ' accetta il valore di tipo ' WebService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="da58e-133">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="da58e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="da58e-134">OUTPUTS</span></span>

### <span data-ttu-id="da58e-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="da58e-135">None</span></span>

## <span data-ttu-id="da58e-136">Note</span><span class="sxs-lookup"><span data-stu-id="da58e-136">NOTES</span></span>
<span data-ttu-id="da58e-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="da58e-137">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="da58e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="da58e-138">RELATED LINKS</span></span>

