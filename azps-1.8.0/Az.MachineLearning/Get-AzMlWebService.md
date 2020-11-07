---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: fe304408ee236312c2e6c71324d6a2a34157ff58
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835303"
---
# <span data-ttu-id="7fdbc-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="7fdbc-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="7fdbc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fdbc-102">SYNOPSIS</span></span>
<span data-ttu-id="7fdbc-103">Recupera le informazioni di riepilogo per uno o più servizi Web.</span><span class="sxs-lookup"><span data-stu-id="7fdbc-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="7fdbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fdbc-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fdbc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fdbc-105">DESCRIPTION</span></span>
<span data-ttu-id="7fdbc-106">Recupera le informazioni di definizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="7fdbc-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="7fdbc-107">A seconda dei paramenti passati, il cmdlet restituisce il definizione per un servizio Web specifico, una raccolta di defintions per i servizi Web per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di defintions per i servizi Web all'interno della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="7fdbc-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="7fdbc-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fdbc-108">EXAMPLES</span></span>

### <span data-ttu-id="7fdbc-109">Esempio 1: ottenere i dettagli di un servizio Web specifico</span><span class="sxs-lookup"><span data-stu-id="7fdbc-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="7fdbc-110">Esempio 2: ottenere tutte le risorse del servizio Web nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="7fdbc-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="7fdbc-111">Esempio 3: ottenere tutti i servizi Web nell'abbonamento corrente e nel gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="7fdbc-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="7fdbc-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fdbc-112">PARAMETERS</span></span>

### <span data-ttu-id="7fdbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fdbc-113">-DefaultProfile</span></span>
<span data-ttu-id="7fdbc-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7fdbc-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7fdbc-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fdbc-115">-Name</span></span>
<span data-ttu-id="7fdbc-116">Nome del servizio Web per cui vengono recuperati i dettagli.</span><span class="sxs-lookup"><span data-stu-id="7fdbc-116">The name of the web service for which the details are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdbc-117">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="7fdbc-117">-Region</span></span>
<span data-ttu-id="7fdbc-118">Nome Regio</span><span class="sxs-lookup"><span data-stu-id="7fdbc-118">The name of regio</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdbc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fdbc-119">-ResourceGroupName</span></span>
<span data-ttu-id="7fdbc-120">Gruppo di risorse da cui vengono recuperati i dettagli per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="7fdbc-120">The resource group from which the details for the web service are retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fdbc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fdbc-121">CommonParameters</span></span>
<span data-ttu-id="7fdbc-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fdbc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fdbc-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fdbc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fdbc-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fdbc-124">INPUTS</span></span>

### <span data-ttu-id="7fdbc-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7fdbc-125">None</span></span>

## <span data-ttu-id="7fdbc-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fdbc-126">OUTPUTS</span></span>

### <span data-ttu-id="7fdbc-127">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="7fdbc-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="7fdbc-128">Note</span><span class="sxs-lookup"><span data-stu-id="7fdbc-128">NOTES</span></span>
<span data-ttu-id="7fdbc-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="7fdbc-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7fdbc-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fdbc-130">RELATED LINKS</span></span>
