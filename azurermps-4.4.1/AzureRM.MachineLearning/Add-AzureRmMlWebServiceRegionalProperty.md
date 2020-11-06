---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 24f12a0e95ab7c233a08ec1ad0f4dc330583dd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522112"
---
# <span data-ttu-id="6d1eb-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="6d1eb-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="6d1eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d1eb-102">SYNOPSIS</span></span>
<span data-ttu-id="6d1eb-103">Crea proprietà del servizio Web regionali.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d1eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d1eb-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d1eb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d1eb-105">DESCRIPTION</span></span>
<span data-ttu-id="6d1eb-106">Crea le proprietà locali di Azure Machine Learning per un servizio Web esistente.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="6d1eb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d1eb-107">EXAMPLES</span></span>

### <span data-ttu-id="6d1eb-108">--------------------------Esempio 1: aggiungere nuove proprietà internazionali per gli Stati Uniti di West Central--------------------------</span><span class="sxs-lookup"><span data-stu-id="6d1eb-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>
<span data-ttu-id="6d1eb-109">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="6d1eb-109">@{paragraph=PS C:\\\>}</span></span>



```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="6d1eb-110">Questo comando di esempio crea una proprietà Region per un servizio Web nell'area "West Central US".</span><span class="sxs-lookup"><span data-stu-id="6d1eb-110">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="6d1eb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d1eb-111">PARAMETERS</span></span>

### <span data-ttu-id="6d1eb-112">-Force</span><span class="sxs-lookup"><span data-stu-id="6d1eb-112">-Force</span></span>
<span data-ttu-id="6d1eb-113">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-113">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6d1eb-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="6d1eb-114">-Name</span></span>
<span data-ttu-id="6d1eb-115">Nome del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-115">The name for the web service.</span></span>

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

### <span data-ttu-id="6d1eb-116">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="6d1eb-116">-Region</span></span>
<span data-ttu-id="6d1eb-117">Area geografica in cui creare le proprietà del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-117">The region in which to create the web service properties.</span></span>

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

### <span data-ttu-id="6d1eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d1eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="6d1eb-119">Gruppo di risorse in cui appartiene il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-119">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="6d1eb-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6d1eb-120">-Confirm</span></span>
<span data-ttu-id="6d1eb-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d1eb-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d1eb-122">-WhatIf</span></span>
<span data-ttu-id="6d1eb-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d1eb-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d1eb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d1eb-125">-DefaultProfile</span></span>
<span data-ttu-id="6d1eb-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d1eb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d1eb-127">CommonParameters</span></span>
<span data-ttu-id="6d1eb-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d1eb-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d1eb-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d1eb-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d1eb-130">INPUTS</span></span>

## <span data-ttu-id="6d1eb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d1eb-131">OUTPUTS</span></span>

### <span data-ttu-id="6d1eb-132">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="6d1eb-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="6d1eb-133">Descrizione di riepilogo del servizio Web di Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="6d1eb-133">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="6d1eb-134">Note</span><span class="sxs-lookup"><span data-stu-id="6d1eb-134">NOTES</span></span>
<span data-ttu-id="6d1eb-135">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6d1eb-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6d1eb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d1eb-136">RELATED LINKS</span></span>

