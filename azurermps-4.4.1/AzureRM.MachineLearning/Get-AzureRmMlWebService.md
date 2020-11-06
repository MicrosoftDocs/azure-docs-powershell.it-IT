---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521617"
---
# <span data-ttu-id="79f94-101">Get-AzureRmMlWebService</span><span class="sxs-lookup"><span data-stu-id="79f94-101">Get-AzureRmMlWebService</span></span>

## <span data-ttu-id="79f94-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="79f94-102">SYNOPSIS</span></span>
<span data-ttu-id="79f94-103">Recupera le informazioni di riepilogo per uno o più servizi Web.</span><span class="sxs-lookup"><span data-stu-id="79f94-103">Retrieves the summary information for one or more web services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79f94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79f94-104">SYNTAX</span></span>

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79f94-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79f94-105">DESCRIPTION</span></span>
<span data-ttu-id="79f94-106">Recupera le informazioni di definizione del servizio Web.</span><span class="sxs-lookup"><span data-stu-id="79f94-106">Retrieves web service defintion information.</span></span>
<span data-ttu-id="79f94-107">A seconda dei paramenti passati, il cmdlet restituisce il definizione per un servizio Web specifico, una raccolta di defintions per i servizi Web per un gruppo di risorse specificato nell'abbonamento corrente o una raccolta di defintions per i servizi Web all'interno della sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="79f94-107">Depending on the paramenters passed, the cmdlet returns the defintion for a specific web service, a collection of defintions for the web services for a specified resource group within the current subscription, or a collection of defintions for the web services within the current subscription.</span></span>

## <span data-ttu-id="79f94-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79f94-108">EXAMPLES</span></span>

### <span data-ttu-id="79f94-109">--------------------------Esempio 1: ottenere i dettagli di un servizio Web specifico--------------------------</span><span class="sxs-lookup"><span data-stu-id="79f94-109">--------------------------  Example 1: Get details of specific web service  --------------------------</span></span>
<span data-ttu-id="79f94-110">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="79f94-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### <span data-ttu-id="79f94-111">--------------------------Esempio 2: ottenere tutte le risorse del servizio Web nell'abbonamento corrente--------------------------</span><span class="sxs-lookup"><span data-stu-id="79f94-111">--------------------------  Example 2: Get all web service resources in current subscription  --------------------------</span></span>
<span data-ttu-id="79f94-112">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="79f94-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService
```

### <span data-ttu-id="79f94-113">--------------------------Esempio 3: ottenere tutti i servizi Web nell'abbonamento corrente e nel gruppo di risorse specifico--------------------------</span><span class="sxs-lookup"><span data-stu-id="79f94-113">--------------------------  Example 3: Get all web services in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="79f94-114">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="79f94-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## <span data-ttu-id="79f94-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="79f94-115">PARAMETERS</span></span>

### <span data-ttu-id="79f94-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="79f94-116">-Name</span></span>
<span data-ttu-id="79f94-117">Nome del servizio Web per cui vengono recuperati i dettagli.</span><span class="sxs-lookup"><span data-stu-id="79f94-117">The name of the web service for which the details are retrieved.</span></span>

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

### <span data-ttu-id="79f94-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f94-118">-ResourceGroupName</span></span>
<span data-ttu-id="79f94-119">Gruppo di risorse da cui vengono recuperati i dettagli per il servizio Web.</span><span class="sxs-lookup"><span data-stu-id="79f94-119">The resource group from which the details for the web service are retrieved.</span></span>

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

### <span data-ttu-id="79f94-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f94-120">-DefaultProfile</span></span>
<span data-ttu-id="79f94-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79f94-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79f94-122">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="79f94-122">-Region</span></span>
<span data-ttu-id="79f94-123">Nome dell'area geografica</span><span class="sxs-lookup"><span data-stu-id="79f94-123">The name of region</span></span>

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

### <span data-ttu-id="79f94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f94-124">CommonParameters</span></span>
<span data-ttu-id="79f94-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79f94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f94-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f94-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f94-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="79f94-127">INPUTS</span></span>

## <span data-ttu-id="79f94-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79f94-128">OUTPUTS</span></span>

### <span data-ttu-id="79f94-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="79f94-129">None</span></span>

## <span data-ttu-id="79f94-130">Note</span><span class="sxs-lookup"><span data-stu-id="79f94-130">NOTES</span></span>
<span data-ttu-id="79f94-131">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Machine, computer Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="79f94-131">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="79f94-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79f94-132">RELATED LINKS</span></span>

