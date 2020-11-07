---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: d1c52cef6548f8762f972789a1fd9d47e8cc92aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687848"
---
# <span data-ttu-id="819f0-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="819f0-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="819f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="819f0-102">SYNOPSIS</span></span>
<span data-ttu-id="819f0-103">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="819f0-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="819f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="819f0-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="819f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="819f0-105">DESCRIPTION</span></span>
<span data-ttu-id="819f0-106">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="819f0-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="819f0-107">Un IotHub non può eseguire la transizione tra le SKU gratuite e quelle a pagamento e viceversa.</span><span class="sxs-lookup"><span data-stu-id="819f0-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="819f0-108">Sarà necessario eliminare e ricreare il iothub se si vuole ottenere questo risultato.</span><span class="sxs-lookup"><span data-stu-id="819f0-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="819f0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="819f0-109">EXAMPLES</span></span>

### <span data-ttu-id="819f0-110">Esempio 1 ottenere gli SKU validi</span><span class="sxs-lookup"><span data-stu-id="819f0-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="819f0-111">Ottiene un elenco di tutte le SKU per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="819f0-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="819f0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="819f0-112">PARAMETERS</span></span>

### <span data-ttu-id="819f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819f0-113">-DefaultProfile</span></span>
<span data-ttu-id="819f0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="819f0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="819f0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="819f0-115">-Name</span></span>
<span data-ttu-id="819f0-116">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="819f0-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="819f0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="819f0-117">-ResourceGroupName</span></span>
<span data-ttu-id="819f0-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="819f0-118">Resource Group Name</span></span>

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

### <span data-ttu-id="819f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819f0-119">CommonParameters</span></span>
<span data-ttu-id="819f0-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="819f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819f0-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819f0-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819f0-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="819f0-122">INPUTS</span></span>

### <span data-ttu-id="819f0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="819f0-123">System.String</span></span>

## <span data-ttu-id="819f0-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="819f0-124">OUTPUTS</span></span>

### <span data-ttu-id="819f0-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="819f0-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="819f0-126">Note</span><span class="sxs-lookup"><span data-stu-id="819f0-126">NOTES</span></span>

## <span data-ttu-id="819f0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="819f0-127">RELATED LINKS</span></span>