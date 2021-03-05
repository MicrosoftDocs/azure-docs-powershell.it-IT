---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlwebservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebServiceKey.md
ms.openlocfilehash: 05adf2476c922fdea17a69bd33f74570309349ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961885"
---
# <span data-ttu-id="93f71-101">Get-AzMlWebServiceKey</span><span class="sxs-lookup"><span data-stu-id="93f71-101">Get-AzMlWebServiceKey</span></span>

## <span data-ttu-id="93f71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f71-102">SYNOPSIS</span></span>
<span data-ttu-id="93f71-103">Recupera le chiavi del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="93f71-103">Retrieves the web service's keys.</span></span>

## <span data-ttu-id="93f71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93f71-104">SYNTAX</span></span>

### <span data-ttu-id="93f71-105">GetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="93f71-105">GetByNameAndResourceGroup</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93f71-106">GetByInstance</span><span class="sxs-lookup"><span data-stu-id="93f71-106">GetByInstance</span></span>
```
Get-AzMlWebServiceKey -MlWebService <WebService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93f71-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93f71-107">DESCRIPTION</span></span>
<span data-ttu-id="93f71-108">Ottiene le chiavi di accesso per le API di runtime del servizio Web Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="93f71-108">Gets the access keys for the Azure Machine Learning web service's runtime APIs.</span></span>

## <span data-ttu-id="93f71-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93f71-109">EXAMPLES</span></span>

### <span data-ttu-id="93f71-110">Esempio 1 - Ottenere le chiavi per un servizio Web specificato dal nome e dal gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="93f71-110">Example 1 - Get the keys for a web service specified by resource group and name</span></span>
```
Get-AzMlWebServiceKey -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="93f71-111">Esempio 2 - Ottenere le chiavi per l'istanza del servizio Web</span><span class="sxs-lookup"><span data-stu-id="93f71-111">Example 2 - Get keys for web service instance</span></span>
```
Get-AzMlWebServiceKey -MlWebService $mlService
```

<span data-ttu-id="93f71-112">$mlService è un oggetto di tipo Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span><span class="sxs-lookup"><span data-stu-id="93f71-112">$mlService is an object of type Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService.</span></span>

## <span data-ttu-id="93f71-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f71-113">PARAMETERS</span></span>

### <span data-ttu-id="93f71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f71-114">-DefaultProfile</span></span>
<span data-ttu-id="93f71-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93f71-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93f71-116">-MlWebService</span><span class="sxs-lookup"><span data-stu-id="93f71-116">-MlWebService</span></span>
<span data-ttu-id="93f71-117">Nome del servizio Web per cui vengono recuperate le chiavi di accesso.</span><span class="sxs-lookup"><span data-stu-id="93f71-117">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="93f71-118">-Name</span><span class="sxs-lookup"><span data-stu-id="93f71-118">-Name</span></span>
<span data-ttu-id="93f71-119">Nome del servizio Web per cui vengono recuperate le chiavi di accesso.</span><span class="sxs-lookup"><span data-stu-id="93f71-119">The name of the web service for which the access keys are retrieved.</span></span>

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

### <span data-ttu-id="93f71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f71-120">-ResourceGroupName</span></span>
<span data-ttu-id="93f71-121">Gruppo di risorse per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="93f71-121">The resource group for the web service.</span></span>

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

### <span data-ttu-id="93f71-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f71-122">CommonParameters</span></span>
<span data-ttu-id="93f71-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f71-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f71-124">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93f71-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f71-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="93f71-125">INPUTS</span></span>

### <span data-ttu-id="93f71-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span><span class="sxs-lookup"><span data-stu-id="93f71-126">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="93f71-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93f71-127">OUTPUTS</span></span>

### <span data-ttu-id="93f71-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span><span class="sxs-lookup"><span data-stu-id="93f71-128">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebServiceKeys</span></span>

## <span data-ttu-id="93f71-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="93f71-129">NOTES</span></span>
<span data-ttu-id="93f71-130">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, computer, apprendimento automatico, azureml</span><span class="sxs-lookup"><span data-stu-id="93f71-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="93f71-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93f71-131">RELATED LINKS</span></span>
