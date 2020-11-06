---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/add-azurermmlwebserviceregionalproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 8b2f881b57639a83227c2f590ffd260b78509a54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521033"
---
# <span data-ttu-id="113ce-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="113ce-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="113ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="113ce-102">SYNOPSIS</span></span>
<span data-ttu-id="113ce-103">Crea proprietà del servizio Web regionali.</span><span class="sxs-lookup"><span data-stu-id="113ce-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="113ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="113ce-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="113ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="113ce-105">DESCRIPTION</span></span>
<span data-ttu-id="113ce-106">Crea le proprietà locali di Azure Machine Learning per un servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="113ce-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="113ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="113ce-107">EXAMPLES</span></span>

### <span data-ttu-id="113ce-108">--------------------------Esempio 1: aggiungere nuove proprietà internazionali per gli Stati Uniti di West Central--------------------------</span><span class="sxs-lookup"><span data-stu-id="113ce-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="113ce-109">Questo comando di esempio crea una proprietà Region per un servizio Web nell'area "West Central US".</span><span class="sxs-lookup"><span data-stu-id="113ce-109">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="113ce-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="113ce-110">PARAMETERS</span></span>

### <span data-ttu-id="113ce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="113ce-111">-DefaultProfile</span></span>
<span data-ttu-id="113ce-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="113ce-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="113ce-113">-Force</span><span class="sxs-lookup"><span data-stu-id="113ce-113">-Force</span></span>
<span data-ttu-id="113ce-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="113ce-114">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="113ce-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="113ce-115">-Name</span></span>
<span data-ttu-id="113ce-116">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="113ce-116">The name for the web service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="113ce-117">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="113ce-117">-Region</span></span>
<span data-ttu-id="113ce-118">Area geografica in cui creare le proprietà del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="113ce-118">The region in which to create the web service properties.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="113ce-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="113ce-119">-ResourceGroupName</span></span>
<span data-ttu-id="113ce-120">Gruppo di risorse in cui appartiene il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="113ce-120">The resource group in which the web service belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="113ce-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="113ce-121">-Confirm</span></span>
<span data-ttu-id="113ce-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="113ce-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="113ce-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="113ce-123">-WhatIf</span></span>
<span data-ttu-id="113ce-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="113ce-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="113ce-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="113ce-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="113ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="113ce-126">CommonParameters</span></span>
<span data-ttu-id="113ce-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="113ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="113ce-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="113ce-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="113ce-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="113ce-129">INPUTS</span></span>

### <span data-ttu-id="113ce-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="113ce-130">None</span></span>
<span data-ttu-id="113ce-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="113ce-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="113ce-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="113ce-132">OUTPUTS</span></span>

### <span data-ttu-id="113ce-133">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="113ce-133">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="113ce-134">Descrizione di riepilogo del servizio Web di Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="113ce-134">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="113ce-135">Note</span><span class="sxs-lookup"><span data-stu-id="113ce-135">NOTES</span></span>
<span data-ttu-id="113ce-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="113ce-136">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="113ce-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="113ce-137">RELATED LINKS</span></span>

