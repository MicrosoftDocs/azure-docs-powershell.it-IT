---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlwebservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlWebService.md
ms.openlocfilehash: be34a81e28f2a11ed604afe922694872fedb5f0a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203572"
---
# <span data-ttu-id="4acfb-101">Get-AzMlWebService</span><span class="sxs-lookup"><span data-stu-id="4acfb-101">Get-AzMlWebService</span></span>

## <span data-ttu-id="4acfb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4acfb-102">SYNOPSIS</span></span>
<span data-ttu-id="4acfb-103">Recupera le informazioni di riepilogo per uno o più servizi Web.</span><span class="sxs-lookup"><span data-stu-id="4acfb-103">Retrieves the summary information for one or more web services.</span></span>

## <span data-ttu-id="4acfb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4acfb-104">SYNTAX</span></span>

```
Get-AzMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4acfb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4acfb-105">DESCRIPTION</span></span>
<span data-ttu-id="4acfb-106">Recupera le informazioni sulla definizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="4acfb-106">Retrieves web service definition information.</span></span>
<span data-ttu-id="4acfb-107">A seconda dei parametri passati, il cmdlet restituisce la definizione per un servizio Web specifico, una raccolta di definizioni per i servizi Web per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di definizioni per i servizi Web all'interno della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="4acfb-107">Depending on the parameters passed, the cmdlet returns the definition for a specific web service, a collection of definitions for the web services for a specified resource group within the current subscription, or a collection of definitions for the web services within the current subscription.</span></span>

## <span data-ttu-id="4acfb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4acfb-108">EXAMPLES</span></span>

### <span data-ttu-id="4acfb-109">Esempio 1: ottenere i dettagli di un servizio Web specifico</span><span class="sxs-lookup"><span data-stu-id="4acfb-109">Example 1: Get details of specific web service</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="4acfb-110">Esempio 2: ottenere tutte le risorse del servizio Web nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4acfb-110">Example 2: Get all web service resources in current subscription</span></span>
```
Get-AzMlWebService
```

### <span data-ttu-id="4acfb-111">Esempio 3: ottenere tutti i servizi Web nell'abbonamento corrente e nel gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="4acfb-111">Example 3: Get all web services in the current subscription and given resource group</span></span>
```
Get-AzMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="4acfb-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4acfb-112">PARAMETERS</span></span>

### <span data-ttu-id="4acfb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4acfb-113">-DefaultProfile</span></span>
<span data-ttu-id="4acfb-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4acfb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4acfb-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4acfb-115">-Name</span></span>
<span data-ttu-id="4acfb-116">Nome del servizio Web per cui vengono recuperati i dettagli.</span><span class="sxs-lookup"><span data-stu-id="4acfb-116">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="4acfb-117">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="4acfb-117">-Region</span></span>
<span data-ttu-id="4acfb-118">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="4acfb-118">The name of region</span></span>

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

### <span data-ttu-id="4acfb-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4acfb-119">-ResourceGroupName</span></span>
<span data-ttu-id="4acfb-120">Gruppo di risorse da cui vengono recuperati i dettagli per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="4acfb-120">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="4acfb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4acfb-121">CommonParameters</span></span>
<span data-ttu-id="4acfb-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4acfb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4acfb-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4acfb-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4acfb-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4acfb-124">INPUTS</span></span>

### <span data-ttu-id="4acfb-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="4acfb-125">None</span></span>

## <span data-ttu-id="4acfb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4acfb-126">OUTPUTS</span></span>

### <span data-ttu-id="4acfb-127">Microsoft. Azure. Management. MachineLearning. WebServices. Models. WebService</span><span class="sxs-lookup"><span data-stu-id="4acfb-127">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>

## <span data-ttu-id="4acfb-128">Note</span><span class="sxs-lookup"><span data-stu-id="4acfb-128">NOTES</span></span>
<span data-ttu-id="4acfb-129">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="4acfb-129">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="4acfb-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4acfb-130">RELATED LINKS</span></span>
