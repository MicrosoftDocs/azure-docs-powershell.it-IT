---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubValidSku.md
ms.openlocfilehash: 904fb627be4460fbbca0dc6dae9a68fc0dd468ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521231"
---
# <span data-ttu-id="4d770-101">Get-AzureRmIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="4d770-101">Get-AzureRmIotHubValidSku</span></span>

## <span data-ttu-id="4d770-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d770-102">SYNOPSIS</span></span>
<span data-ttu-id="4d770-103">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="4d770-103">Gets all valid skus that this IotHub can transition to.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d770-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d770-104">SYNTAX</span></span>

```
Get-AzureRmIotHubValidSku [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d770-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d770-105">DESCRIPTION</span></span>
<span data-ttu-id="4d770-106">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="4d770-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="4d770-107">Un IotHub non può eseguire la transizione tra le SKU gratuite e quelle a pagamento e viceversa.</span><span class="sxs-lookup"><span data-stu-id="4d770-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="4d770-108">Sarà necessario eliminare e ricreare il iothub se si vuole ottenere questo risultato.</span><span class="sxs-lookup"><span data-stu-id="4d770-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="4d770-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d770-109">EXAMPLES</span></span>

### <span data-ttu-id="4d770-110">Esempio 1 ottenere gli SKU validi</span><span class="sxs-lookup"><span data-stu-id="4d770-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzureRmIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="4d770-111">Ottiene un elenco di tutte le SKU per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="4d770-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="4d770-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d770-112">PARAMETERS</span></span>

### <span data-ttu-id="4d770-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d770-113">-Name</span></span>
<span data-ttu-id="4d770-114">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="4d770-114">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="4d770-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d770-115">-ResourceGroupName</span></span>
<span data-ttu-id="4d770-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="4d770-116">Resource Group Name</span></span>

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

### <span data-ttu-id="4d770-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d770-117">-DefaultProfile</span></span>
<span data-ttu-id="4d770-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d770-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d770-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d770-119">CommonParameters</span></span>
<span data-ttu-id="4d770-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d770-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d770-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d770-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d770-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d770-122">INPUTS</span></span>

### <span data-ttu-id="4d770-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4d770-123">System.String</span></span>

## <span data-ttu-id="4d770-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d770-124">OUTPUTS</span></span>

### <span data-ttu-id="4d770-125">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription, Microsoft. Azure. Commands. IotHub, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4d770-125">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription, Microsoft.Azure.Commands.IotHub, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4d770-126">Note</span><span class="sxs-lookup"><span data-stu-id="4d770-126">NOTES</span></span>

## <span data-ttu-id="4d770-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d770-127">RELATED LINKS</span></span>

