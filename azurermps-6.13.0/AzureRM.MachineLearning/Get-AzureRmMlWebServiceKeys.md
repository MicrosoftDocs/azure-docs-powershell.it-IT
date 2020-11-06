---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 7d0df70118f50274ccecfd730e752efabcf52519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515156"
---
# <span data-ttu-id="6fc0a-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="6fc0a-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="6fc0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc0a-103">Recupera le chiavi del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="6fc0a-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fc0a-104">SYNTAX</span></span>

### <span data-ttu-id="6fc0a-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6fc0a-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fc0a-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="6fc0a-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fc0a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fc0a-107">DESCRIPTION</span></span>
<span data-ttu-id="6fc0a-108">Ottiene i tasti di scelta per le API di runtime del servizio Web di Azure computer Learning.</span><span class="sxs-lookup"><span data-stu-id="6fc0a-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="6fc0a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fc0a-109">EXAMPLES</span></span>

### <span data-ttu-id="6fc0a-110">Esempio 1-ottenere le chiavi per un servizio Web specificato dal gruppo di risorse e dal nome</span><span class="sxs-lookup"><span data-stu-id="6fc0a-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="6fc0a-111">Esempio 2-Get Keys per l'istanza del servizio Web</span><span class="sxs-lookup"><span data-stu-id="6fc0a-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="6fc0a-112">$mlService è un oggetto di tipo Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="6fc0a-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="6fc0a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fc0a-113">PARAMETERS</span></span>

### <span data-ttu-id="6fc0a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc0a-114">-DefaultProfile</span></span>
<span data-ttu-id="6fc0a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6fc0a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fc0a-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="6fc0a-116">-MlWebService</span></span>
<span data-ttu-id="6fc0a-117">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="6fc0a-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: GetByInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc0a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fc0a-118">-Name</span></span>
<span data-ttu-id="6fc0a-119">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="6fc0a-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc0a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fc0a-120">-ResourceGroupName</span></span>
<span data-ttu-id="6fc0a-121">Gruppo di risorse per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="6fc0a-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc0a-122">CommonParameters</span></span>
<span data-ttu-id="6fc0a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc0a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc0a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc0a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fc0a-125">INPUTS</span></span>

### <span data-ttu-id="6fc0a-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="6fc0a-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="6fc0a-127">Parametri: MlWebService (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6fc0a-127">Parameters: MlWebService (ByValue)</span></span>

## <span data-ttu-id="6fc0a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fc0a-128">OUTPUTS</span></span>

### <span data-ttu-id="6fc0a-129">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="6fc0a-129">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="6fc0a-130">Note</span><span class="sxs-lookup"><span data-stu-id="6fc0a-130">NOTES</span></span>
<span data-ttu-id="6fc0a-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="6fc0a-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6fc0a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fc0a-132">RELATED LINKS</span></span>
