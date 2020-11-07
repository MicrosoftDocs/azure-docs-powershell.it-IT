---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: f81419f43defdf2c66d2d8f1768c63fc09ff0d35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835864"
---
# <span data-ttu-id="5fcf8-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="5fcf8-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="5fcf8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fcf8-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcf8-103">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="5fcf8-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="5fcf8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fcf8-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fcf8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fcf8-105">DESCRIPTION</span></span>
<span data-ttu-id="5fcf8-106">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="5fcf8-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="5fcf8-107">Un IotHub non può eseguire la transizione tra le SKU gratuite e quelle a pagamento e viceversa.</span><span class="sxs-lookup"><span data-stu-id="5fcf8-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="5fcf8-108">Sarà necessario eliminare e ricreare il iothub se si vuole ottenere questo risultato.</span><span class="sxs-lookup"><span data-stu-id="5fcf8-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="5fcf8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fcf8-109">EXAMPLES</span></span>

### <span data-ttu-id="5fcf8-110">Esempio 1 ottenere gli SKU validi</span><span class="sxs-lookup"><span data-stu-id="5fcf8-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="5fcf8-111">Ottiene un elenco di tutte le SKU per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="5fcf8-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="5fcf8-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fcf8-112">PARAMETERS</span></span>

### <span data-ttu-id="5fcf8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcf8-113">-DefaultProfile</span></span>
<span data-ttu-id="5fcf8-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5fcf8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fcf8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fcf8-115">-Name</span></span>
<span data-ttu-id="5fcf8-116">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="5fcf8-116">Name of the IoT hub.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fcf8-117">-ResourceGroupName</span></span>
<span data-ttu-id="5fcf8-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="5fcf8-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fcf8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcf8-119">CommonParameters</span></span>
<span data-ttu-id="5fcf8-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fcf8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcf8-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcf8-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcf8-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fcf8-122">INPUTS</span></span>

### <span data-ttu-id="5fcf8-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5fcf8-123">System.String</span></span>

## <span data-ttu-id="5fcf8-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fcf8-124">OUTPUTS</span></span>

### <span data-ttu-id="5fcf8-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="5fcf8-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="5fcf8-126">Note</span><span class="sxs-lookup"><span data-stu-id="5fcf8-126">NOTES</span></span>

## <span data-ttu-id="5fcf8-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fcf8-127">RELATED LINKS</span></span>
