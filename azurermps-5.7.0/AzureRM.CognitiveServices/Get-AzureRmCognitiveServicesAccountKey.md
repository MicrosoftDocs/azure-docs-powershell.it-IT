---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 73B1EB7E-568E-44E8-993A-91678B7D8AEE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountKey.md
ms.openlocfilehash: 230c47e67610cdeea629097f26c73cb2774c5384
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518208"
---
# <span data-ttu-id="31567-101">Get-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="31567-101">Get-AzureRmCognitiveServicesAccountKey</span></span>

## <span data-ttu-id="31567-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31567-102">SYNOPSIS</span></span>
<span data-ttu-id="31567-103">Ottiene le chiavi dell'API per un account.</span><span class="sxs-lookup"><span data-stu-id="31567-103">Gets the API keys for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31567-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31567-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31567-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31567-105">DESCRIPTION</span></span>
<span data-ttu-id="31567-106">Il cmdlet **Get-AzureRmCognitiveServicesAccountKey** ottiene le chiavi API per un account di servizi cognitivi con provisioning.</span><span class="sxs-lookup"><span data-stu-id="31567-106">The **Get-AzureRmCognitiveServicesAccountKey** cmdlet gets the API keys for a provisioned Cognitive Services account.</span></span>

<span data-ttu-id="31567-107">Un account di servizi cognitivi dispone di due chiavi API: key1 e key2.</span><span class="sxs-lookup"><span data-stu-id="31567-107">A Cognitive Services account has two API keys: Key1 and Key2.</span></span>
<span data-ttu-id="31567-108">I tasti consentono l'interazione con l'endpoint dell'account dei servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="31567-108">The keys enable interaction with the Cognitive Services account endpoint.</span></span>

<span data-ttu-id="31567-109">Usare New-AzureRmCognitiveServicesAccountKey per rigenerare una chiave.</span><span class="sxs-lookup"><span data-stu-id="31567-109">Use New-AzureRmCognitiveServicesAccountKey to regenerate a key.</span></span>

## <span data-ttu-id="31567-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31567-110">EXAMPLES</span></span>

## <span data-ttu-id="31567-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31567-111">PARAMETERS</span></span>

### <span data-ttu-id="31567-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31567-112">-DefaultProfile</span></span>
<span data-ttu-id="31567-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="31567-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31567-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="31567-114">-Name</span></span>
<span data-ttu-id="31567-115">Specifica il nome dell'account.</span><span class="sxs-lookup"><span data-stu-id="31567-115">Specifies the name of the account.</span></span>
<span data-ttu-id="31567-116">Questo cmdlet ottiene le chiavi per l'account.</span><span class="sxs-lookup"><span data-stu-id="31567-116">This cmdlet gets the keys for this account.</span></span>

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

### <span data-ttu-id="31567-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31567-117">-ResourceGroupName</span></span>
<span data-ttu-id="31567-118">Specifica il nome del gruppo di risorse a cui è assegnato l'account.</span><span class="sxs-lookup"><span data-stu-id="31567-118">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="31567-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31567-119">CommonParameters</span></span>
<span data-ttu-id="31567-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31567-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31567-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31567-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31567-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31567-122">INPUTS</span></span>

### <span data-ttu-id="31567-123">Nessuno</span><span class="sxs-lookup"><span data-stu-id="31567-123">None</span></span>
<span data-ttu-id="31567-124">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="31567-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31567-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31567-125">OUTPUTS</span></span>

### <span data-ttu-id="31567-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccountKeys</span><span class="sxs-lookup"><span data-stu-id="31567-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccountKeys</span></span>

## <span data-ttu-id="31567-127">Note</span><span class="sxs-lookup"><span data-stu-id="31567-127">NOTES</span></span>

## <span data-ttu-id="31567-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31567-128">RELATED LINKS</span></span>

[<span data-ttu-id="31567-129">New-AzureRmCognitiveServicesAccountKey</span><span class="sxs-lookup"><span data-stu-id="31567-129">New-AzureRmCognitiveServicesAccountKey</span></span>](./New-AzureRmCognitiveServicesAccountKey.md)


