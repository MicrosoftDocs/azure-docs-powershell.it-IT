---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: ed243f822817c223576fd3bbe0293a8cf18d7a51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510032"
---
# <span data-ttu-id="7f5af-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="7f5af-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="7f5af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f5af-102">SYNOPSIS</span></span>
<span data-ttu-id="7f5af-103">Ottiene le SKU disponibili per un account.</span><span class="sxs-lookup"><span data-stu-id="7f5af-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f5af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f5af-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f5af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f5af-105">DESCRIPTION</span></span>
<span data-ttu-id="7f5af-106">Il cmdlet **Get-AzureRmCognitiveServicesAccountSkus** ottiene gli SKU disponibili per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7f5af-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="7f5af-107">L'USK è il piano di livello per un account.</span><span class="sxs-lookup"><span data-stu-id="7f5af-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="7f5af-108">Definisce il prezzo, il limite di chiamata e il tasso per l'account.</span><span class="sxs-lookup"><span data-stu-id="7f5af-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="7f5af-109">La SKU F0 è un livello gratuito.</span><span class="sxs-lookup"><span data-stu-id="7f5af-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="7f5af-110">I livelli a pagamento includono S0, S1, S2 e così via.</span><span class="sxs-lookup"><span data-stu-id="7f5af-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="7f5af-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f5af-111">EXAMPLES</span></span>

## <span data-ttu-id="7f5af-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f5af-112">PARAMETERS</span></span>

### <span data-ttu-id="7f5af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f5af-113">-DefaultProfile</span></span>
<span data-ttu-id="7f5af-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7f5af-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7f5af-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="7f5af-115">-Name</span></span>
<span data-ttu-id="7f5af-116">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="7f5af-116">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5af-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f5af-117">-ResourceGroupName</span></span>
<span data-ttu-id="7f5af-118">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="7f5af-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f5af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f5af-119">CommonParameters</span></span>
<span data-ttu-id="7f5af-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f5af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f5af-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f5af-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f5af-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f5af-122">INPUTS</span></span>

### <span data-ttu-id="7f5af-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7f5af-123">None</span></span>
<span data-ttu-id="7f5af-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="7f5af-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f5af-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f5af-125">OUTPUTS</span></span>

### <span data-ttu-id="7f5af-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="7f5af-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="7f5af-127">Note</span><span class="sxs-lookup"><span data-stu-id="7f5af-127">NOTES</span></span>

## <span data-ttu-id="7f5af-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f5af-128">RELATED LINKS</span></span>

