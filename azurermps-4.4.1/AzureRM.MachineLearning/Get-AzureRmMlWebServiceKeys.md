---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebServiceKeys.md
ms.openlocfilehash: 694ac928d78cf64f500730c57e394a8e3a425456
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521613"
---
# <span data-ttu-id="dd20f-101">Get-AzureRmMlWebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="dd20f-101">Get-AzureRmMlWebServiceKeys</span></span>

## <span data-ttu-id="dd20f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dd20f-102">SYNOPSIS</span></span>
<span data-ttu-id="dd20f-103">Recupera le chiavi del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="dd20f-103">Retrieves the web service's keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dd20f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd20f-104">SYNTAX</span></span>

### <span data-ttu-id="dd20f-105">Ottenere i tasti di scelta di un servizio Web Azure ML in base al nome e al gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd20f-105">Get an Azure ML web service's access keys given its name and resource group.</span></span>
```
Get-AzureRmMlWebServiceKeys -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dd20f-106">Ottenere il Kesy di Access per l'istanza del servizio Web specificata.</span><span class="sxs-lookup"><span data-stu-id="dd20f-106">Get the access kesy for the given web service instance.</span></span>
```
Get-AzureRmMlWebServiceKeys -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd20f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dd20f-107">DESCRIPTION</span></span>
<span data-ttu-id="dd20f-108">Ottiene i tasti di scelta per le API di runtime del servizio Web di Azure computer Learning.</span><span class="sxs-lookup"><span data-stu-id="dd20f-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="dd20f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd20f-109">EXAMPLES</span></span>

### <span data-ttu-id="dd20f-110">--------------------------Esempio 1: ottenere le chiavi per un servizio Web specificato dal gruppo di risorse e dal nome--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd20f-110">--------------------------  Example 1 - Get the keys for a web service specified by resource group and name  --------------------------</span></span>
<span data-ttu-id="dd20f-111">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd20f-111">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="dd20f-112">--------------------------Esempio 2-Get Keys per l'istanza del servizio Web--------------------------</span><span class="sxs-lookup"><span data-stu-id="dd20f-112">--------------------------  Example 2 - Get keys for web service instance  --------------------------</span></span>
<span data-ttu-id="dd20f-113">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="dd20f-113">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebServiceKeys -MlWebService $mlService
```

<span data-ttu-id="dd20f-114">$mlService è un oggetto di tipo Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService.</span><span class="sxs-lookup"><span data-stu-id="dd20f-114">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="dd20f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dd20f-115">PARAMETERS</span></span>

### <span data-ttu-id="dd20f-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="dd20f-116">-MlWebService</span></span>
<span data-ttu-id="dd20f-117">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="dd20f-117">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService
Parameter Sets: Get the access kesy for the given web service instance.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd20f-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="dd20f-118">-Name</span></span>
<span data-ttu-id="dd20f-119">Nome del servizio Web per cui vengono recuperati i tasti di scelta.</span><span class="sxs-lookup"><span data-stu-id="dd20f-119">The name of the web service for which the access keys are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd20f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd20f-120">-ResourceGroupName</span></span>
<span data-ttu-id="dd20f-121">Gruppo di risorse per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="dd20f-121">The resource group for the web service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get an Azure ML web service's access keys given its name and resource group.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd20f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd20f-122">-DefaultProfile</span></span>
<span data-ttu-id="dd20f-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dd20f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd20f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd20f-124">CommonParameters</span></span>
<span data-ttu-id="dd20f-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd20f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd20f-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd20f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd20f-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dd20f-127">INPUTS</span></span>

### <span data-ttu-id="dd20f-128">Servizio</span><span class="sxs-lookup"><span data-stu-id="dd20f-128">WebService</span></span>
<span data-ttu-id="dd20f-129">Il parametro ' MlWebService ' accetta il valore di tipo ' WebService ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="dd20f-129">Parameter 'MlWebService' accepts value of type 'WebService' from the pipeline</span></span>

## <span data-ttu-id="dd20f-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd20f-130">OUTPUTS</span></span>

### <span data-ttu-id="dd20f-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="dd20f-131">None</span></span>

## <span data-ttu-id="dd20f-132">Note</span><span class="sxs-lookup"><span data-stu-id="dd20f-132">NOTES</span></span>
<span data-ttu-id="dd20f-133">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="dd20f-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="dd20f-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd20f-134">RELATED LINKS</span></span>

