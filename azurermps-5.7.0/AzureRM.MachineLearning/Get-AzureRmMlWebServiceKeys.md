---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: a0019b418fbf71a9b8010b4256a062a943244a9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516764"
---
# <span data-ttu-id="62450-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="62450-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="62450-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62450-102">SYNOPSIS</span></span>
<span data-ttu-id="62450-103">Recupera le chiavi del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="62450-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62450-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62450-104">SYNTAX</span></span>

### <span data-ttu-id="62450-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="62450-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62450-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="62450-106">GetByInstance</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62450-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62450-107">DESCRIPTION</span></span>
<span data-ttu-id="62450-108">Ottiene i tasti di scelta per le API di runtime del servizio Web di Azure computer Learning.</span><span class="sxs-lookup"><span data-stu-id="62450-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="62450-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62450-109">EXAMPLES</span></span>

### <span data-ttu-id="62450-110">--------------------------Esempio 1: ottenere le chiavi per un servizio Web specificato dal gruppo di risorse e dal nome--------------------------</span><span class="sxs-lookup"><span data-stu-id="62450-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="62450-111">--------------------------Esempio 2-Get Keys per l'istanza del servizio Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="62450-111">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="62450-112">$mlService è un oggetto di tipo Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="62450-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="62450-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62450-113">PARAMETERS</span></span>

### <span data-ttu-id="62450-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62450-114">-DefaultProfile</span></span>
<span data-ttu-id="62450-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62450-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62450-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="62450-116">-MlWebService</span></span>
<span data-ttu-id="62450-117">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="62450-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: WebService
Parameter Sets: GetByInstance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62450-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="62450-118">-Name</span></span>
<span data-ttu-id="62450-119">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="62450-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62450-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62450-120">-ResourceGroupName</span></span>
<span data-ttu-id="62450-121">Gruppo di risorse per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="62450-121">The resource group for the web service.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62450-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62450-122">CommonParameters</span></span>
<span data-ttu-id="62450-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62450-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62450-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62450-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62450-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62450-125">INPUTS</span></span>

### <span data-ttu-id="62450-126">Servizio</span><span class="sxs-lookup"><span data-stu-id="62450-126">WebService</span></span>
<span data-ttu-id="62450-127">Il parametro ' MlWebService ' accetta il valore di tipo ' WebService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="62450-127">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="62450-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62450-128">OUTPUTS</span></span>

### <span data-ttu-id="62450-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="62450-129">None</span></span>

## <span data-ttu-id="62450-130">Note</span><span class="sxs-lookup"><span data-stu-id="62450-130">NOTES</span></span>
<span data-ttu-id="62450-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="62450-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="62450-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62450-132">RELATED LINKS</span></span>

