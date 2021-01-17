---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubvalidsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubValidSku.md
ms.openlocfilehash: e0f178c10fa74d8fa230472397d7bcc835f98bf4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371097"
---
# <span data-ttu-id="cbe04-101">Get-AzIotHubValidSku</span><span class="sxs-lookup"><span data-stu-id="cbe04-101">Get-AzIotHubValidSku</span></span>

## <span data-ttu-id="cbe04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbe04-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe04-103">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="cbe04-103">Gets all valid skus that this IotHub can transition to.</span></span>

## <span data-ttu-id="cbe04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbe04-104">SYNTAX</span></span>

```
Get-AzIotHubValidSku [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbe04-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbe04-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe04-106">Ottiene tutti gli SKU validi a cui questo IotHub può eseguire la transizione.</span><span class="sxs-lookup"><span data-stu-id="cbe04-106">Gets all the valid skus that this IotHub can transition to.</span></span>
<span data-ttu-id="cbe04-107">Un IotHub non può eseguire la transizione tra le SKU gratuite e quelle a pagamento e viceversa.</span><span class="sxs-lookup"><span data-stu-id="cbe04-107">An IotHub cannot transition between free and the paid skus and vice versa.</span></span> <span data-ttu-id="cbe04-108">Sarà necessario eliminare e ricreare il iothub se si vuole ottenere questo risultato.</span><span class="sxs-lookup"><span data-stu-id="cbe04-108">You will have to delete and recreate the iothub if you want to achieve this.</span></span>

## <span data-ttu-id="cbe04-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbe04-109">EXAMPLES</span></span>

### <span data-ttu-id="cbe04-110">Esempio 1 ottenere gli SKU validi</span><span class="sxs-lookup"><span data-stu-id="cbe04-110">Example 1 Get the valid skus</span></span>
```
PS C:\> Get-AzIotHubValidSku -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="cbe04-111">Ottiene un elenco di tutte le SKU per la IotHub denominata "myiothub"</span><span class="sxs-lookup"><span data-stu-id="cbe04-111">Gets a list of all skus for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="cbe04-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbe04-112">PARAMETERS</span></span>

### <span data-ttu-id="cbe04-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbe04-113">-DefaultProfile</span></span>
<span data-ttu-id="cbe04-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cbe04-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cbe04-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbe04-115">-Name</span></span>
<span data-ttu-id="cbe04-116">Nome dell'hub molto.</span><span class="sxs-lookup"><span data-stu-id="cbe04-116">Name of the IoT hub.</span></span> 

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

### <span data-ttu-id="cbe04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbe04-117">-ResourceGroupName</span></span>
<span data-ttu-id="cbe04-118">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="cbe04-118">Resource Group Name</span></span>

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

### <span data-ttu-id="cbe04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe04-119">CommonParameters</span></span>
<span data-ttu-id="cbe04-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbe04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe04-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe04-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe04-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbe04-122">INPUTS</span></span>

### <span data-ttu-id="cbe04-123">System. String</span><span class="sxs-lookup"><span data-stu-id="cbe04-123">System.String</span></span>

## <span data-ttu-id="cbe04-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbe04-124">OUTPUTS</span></span>

### <span data-ttu-id="cbe04-125">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHubSkuDescription</span><span class="sxs-lookup"><span data-stu-id="cbe04-125">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSkuDescription</span></span>

## <span data-ttu-id="cbe04-126">Note</span><span class="sxs-lookup"><span data-stu-id="cbe04-126">NOTES</span></span>

## <span data-ttu-id="cbe04-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbe04-127">RELATED LINKS</span></span>
