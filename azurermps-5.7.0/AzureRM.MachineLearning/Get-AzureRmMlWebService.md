---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 802a3be7aca857b798f1e853bec499c5397b6e65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512539"
---
# <span data-ttu-id="f37bf-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="f37bf-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="f37bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f37bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f37bf-103">Recupera le informazioni di riepilogo per uno o più servizi Web.</span><span class="sxs-lookup"><span data-stu-id="f37bf-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f37bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f37bf-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f37bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f37bf-105">DESCRIPTION</span></span>
<span data-ttu-id="f37bf-106">Recupera le informazioni di definizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="f37bf-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="f37bf-107">A seconda dei paramenti passati, il cmdlet restituisce il definizione per un servizio Web specifico, una raccolta di defintions per i servizi Web per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di defintions per i servizi Web all'interno della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f37bf-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="f37bf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f37bf-108">EXAMPLES</span></span>

### <span data-ttu-id="f37bf-109">--------------------------Esempio 1: ottenere i dettagli di un servizio Web specifico--------------------------</span><span class="sxs-lookup"><span data-stu-id="f37bf-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="f37bf-110">--------------------------Esempio 2: ottenere tutte le risorse del servizio Web nell'abbonamento corrente--------------------------</span><span class="sxs-lookup"><span data-stu-id="f37bf-110">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
```
Get-AzureRmMlWebService
```

### <span data-ttu-id="f37bf-111">--------------------------Esempio 3: ottenere tutti i servizi Web nell'abbonamento corrente e nel gruppo di risorse specifico--------------------------</span><span class="sxs-lookup"><span data-stu-id="f37bf-111">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="f37bf-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f37bf-112">PARAMETERS</span></span>

### <span data-ttu-id="f37bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f37bf-113">-DefaultProfile</span></span>
<span data-ttu-id="f37bf-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f37bf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f37bf-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="f37bf-115">-Name</span></span>
<span data-ttu-id="f37bf-116">Nome del servizio Web per cui vengono recuperati i dettagli.</span><span class="sxs-lookup"><span data-stu-id="f37bf-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37bf-117">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="f37bf-117">-Region</span></span>
<span data-ttu-id="f37bf-118">Nome Regio</span><span class="sxs-lookup"><span data-stu-id="f37bf-118">The name of regio</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37bf-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f37bf-119">-ResourceGroupName</span></span>
<span data-ttu-id="f37bf-120">Gruppo di risorse da cui vengono recuperati i dettagli per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="f37bf-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f37bf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f37bf-121">CommonParameters</span></span>
<span data-ttu-id="f37bf-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f37bf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f37bf-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f37bf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f37bf-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f37bf-124">INPUTS</span></span>

### <span data-ttu-id="f37bf-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f37bf-125">None</span></span>
<span data-ttu-id="f37bf-126">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f37bf-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f37bf-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f37bf-127">OUTPUTS</span></span>

### <span data-ttu-id="f37bf-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f37bf-128">None</span></span>

## <span data-ttu-id="f37bf-129">Note</span><span class="sxs-lookup"><span data-stu-id="f37bf-129">NOTES</span></span>
<span data-ttu-id="f37bf-130">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="f37bf-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f37bf-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f37bf-131">RELATED LINKS</span></span>

