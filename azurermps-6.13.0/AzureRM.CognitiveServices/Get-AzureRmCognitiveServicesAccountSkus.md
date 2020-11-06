---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: e1bacc62ca7efc3bd453be93196e83b0b6d67853
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519289"
---
# <span data-ttu-id="f61c9-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="f61c9-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="f61c9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f61c9-102">SYNOPSIS</span></span>
<span data-ttu-id="f61c9-103">Ottiene le SKU disponibili per un account.</span><span class="sxs-lookup"><span data-stu-id="f61c9-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f61c9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f61c9-104">SYNTAX</span></span>

### <span data-ttu-id="f61c9-105">GetSkusWithAccount (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f61c9-105">GetSkusWithAccount (Default)</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f61c9-106">GetSkusWithFilter</span><span class="sxs-lookup"><span data-stu-id="f61c9-106">GetSkusWithFilter</span></span>
```
Get-AzureRmCognitiveServicesAccountSkus [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f61c9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f61c9-107">DESCRIPTION</span></span>
<span data-ttu-id="f61c9-108">Il cmdlet **Get-AzureRmCognitiveServicesAccountSkus** ottiene gli SKU disponibili per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="f61c9-108">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="f61c9-109">L'USK è il piano di livello per un account.</span><span class="sxs-lookup"><span data-stu-id="f61c9-109">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="f61c9-110">Definisce il prezzo, il limite di chiamata e il tasso per l'account.</span><span class="sxs-lookup"><span data-stu-id="f61c9-110">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="f61c9-111">La SKU F0 è un livello gratuito.</span><span class="sxs-lookup"><span data-stu-id="f61c9-111">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="f61c9-112">I livelli a pagamento includono S0, S1, S2 e così via.</span><span class="sxs-lookup"><span data-stu-id="f61c9-112">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="f61c9-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f61c9-113">EXAMPLES</span></span>

### <span data-ttu-id="f61c9-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f61c9-114">Example 1</span></span>
```powershell
PS C:\> (Get-AzureRmCognitiveServicesAccountSkus -ResourceGroupName cognitive-services-resource-group -Name myluis).Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="f61c9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f61c9-115">PARAMETERS</span></span>

### <span data-ttu-id="f61c9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f61c9-116">-DefaultProfile</span></span>
<span data-ttu-id="f61c9-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f61c9-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f61c9-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f61c9-118">-Location</span></span>
<span data-ttu-id="f61c9-119">Posizione dell'account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="f61c9-119">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f61c9-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f61c9-120">-Name</span></span>
<span data-ttu-id="f61c9-121">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="f61c9-121">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f61c9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f61c9-122">-ResourceGroupName</span></span>
<span data-ttu-id="f61c9-123">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="f61c9-123">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithAccount
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f61c9-124">-Digitare</span><span class="sxs-lookup"><span data-stu-id="f61c9-124">-Type</span></span>
<span data-ttu-id="f61c9-125">Tipo di account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="f61c9-125">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: GetSkusWithFilter
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f61c9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61c9-126">CommonParameters</span></span>
<span data-ttu-id="f61c9-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f61c9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61c9-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f61c9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61c9-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f61c9-129">INPUTS</span></span>

### <span data-ttu-id="f61c9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f61c9-130">System.String</span></span>

## <span data-ttu-id="f61c9-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f61c9-131">OUTPUTS</span></span>

### <span data-ttu-id="f61c9-132">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="f61c9-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="f61c9-133">Note</span><span class="sxs-lookup"><span data-stu-id="f61c9-133">NOTES</span></span>

## <span data-ttu-id="f61c9-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f61c9-134">RELATED LINKS</span></span>
