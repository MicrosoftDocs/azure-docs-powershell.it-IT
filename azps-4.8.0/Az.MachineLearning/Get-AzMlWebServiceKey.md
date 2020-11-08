---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: e6da366738bf6b1d56c9500ddd6064c6505a5936
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189619"
---
# <span data-ttu-id="21e41-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="21e41-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="21e41-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21e41-102">SYNOPSIS</span></span>
<span data-ttu-id="21e41-103">Recupera le chiavi del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="21e41-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="21e41-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21e41-104">SYNTAX</span></span>

### <span data-ttu-id="21e41-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="21e41-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21e41-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="21e41-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="21e41-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21e41-107">DESCRIPTION</span></span>
<span data-ttu-id="21e41-108">Ottiene i tasti di scelta per le API di runtime del servizio Web di Azure computer Learning.</span><span class="sxs-lookup"><span data-stu-id="21e41-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="21e41-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21e41-109">EXAMPLES</span></span>

### <span data-ttu-id="21e41-110">Esempio 1-ottenere le chiavi per un servizio Web specificato dal gruppo di risorse e dal nome</span><span class="sxs-lookup"><span data-stu-id="21e41-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="21e41-111">Esempio 2-Get Keys per l'istanza del servizio Web</span><span class="sxs-lookup"><span data-stu-id="21e41-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="21e41-112">$mlService è un oggetto di tipo Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="21e41-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="21e41-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21e41-113">PARAMETERS</span></span>

### <span data-ttu-id="21e41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21e41-114">-DefaultProfile</span></span>
<span data-ttu-id="21e41-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="21e41-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21e41-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="21e41-116">-MlWebService</span></span>
<span data-ttu-id="21e41-117">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="21e41-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="21e41-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="21e41-118">-Name</span></span>
<span data-ttu-id="21e41-119">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="21e41-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="21e41-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21e41-120">-ResourceGroupName</span></span>
<span data-ttu-id="21e41-121">Gruppo di risorse per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="21e41-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="21e41-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21e41-122">CommonParameters</span></span>
<span data-ttu-id="21e41-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21e41-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21e41-124">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21e41-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21e41-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21e41-125">INPUTS</span></span>

### <span data-ttu-id="21e41-126">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="21e41-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="21e41-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21e41-127">OUTPUTS</span></span>

### <span data-ttu-id="21e41-128">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="21e41-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="21e41-129">Note</span><span class="sxs-lookup"><span data-stu-id="21e41-129">NOTES</span></span>
<span data-ttu-id="21e41-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="21e41-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="21e41-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21e41-131">RELATED LINKS</span></span>