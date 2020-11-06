---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 11D5BFDF-5E5D-46B2-9F9B-A0524EFA1B42
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccount.md
ms.openlocfilehash: 41d217579175de3c1de6f36b6850dfd391ca04b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516911"
---
# <span data-ttu-id="692b3-101">Get-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="692b3-101">Get-AzureRmCognitiveServicesAccount</span></span>

## <span data-ttu-id="692b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="692b3-102">SYNOPSIS</span></span>
<span data-ttu-id="692b3-103">Ottiene un account.</span><span class="sxs-lookup"><span data-stu-id="692b3-103">Gets an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="692b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="692b3-104">SYNTAX</span></span>

### <span data-ttu-id="692b3-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="692b3-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="692b3-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="692b3-106">AccountNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="692b3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="692b3-107">DESCRIPTION</span></span>
<span data-ttu-id="692b3-108">Il cmdlet **Get-AzureRmCognitiveServicesAccount** ottiene gli account di servizi cognitivi con provisioning nel gruppo di risorse specificato dal parametro *ResoureGroupName* .</span><span class="sxs-lookup"><span data-stu-id="692b3-108">The **Get-AzureRmCognitiveServicesAccount** cmdlet gets the provisioned Cognitive Services accounts in the resource group specified by the *ResoureGroupName* parameter.</span></span>

<span data-ttu-id="692b3-109">Se non specifichi il parametro *ResoureGroupName* , questo cmdlet ottiene tutti gli account dei servizi cognitivi per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="692b3-109">If you do not specify the *ResoureGroupName* parameter, this cmdlet gets all Cognitive Services accounts for the current subscription.</span></span>

## <span data-ttu-id="692b3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="692b3-110">EXAMPLES</span></span>

## <span data-ttu-id="692b3-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="692b3-111">PARAMETERS</span></span>

### <span data-ttu-id="692b3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="692b3-112">-DefaultProfile</span></span>
<span data-ttu-id="692b3-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="692b3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="692b3-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="692b3-114">-Name</span></span>
<span data-ttu-id="692b3-115">Specifica il nome dell'account dei servizi cognitivi da ottenere.</span><span class="sxs-lookup"><span data-stu-id="692b3-115">Specifies the name of the Cognitive Services account to get.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692b3-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="692b3-116">-ResourceGroupName</span></span>
<span data-ttu-id="692b3-117">Specifica il nome del gruppo di risorse a cui è assegnato l'account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="692b3-117">Specifies the name of the resource group the Cognitive Services account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="692b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="692b3-118">CommonParameters</span></span>
<span data-ttu-id="692b3-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="692b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="692b3-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="692b3-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="692b3-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="692b3-121">INPUTS</span></span>

### <span data-ttu-id="692b3-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="692b3-122">None</span></span>
<span data-ttu-id="692b3-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="692b3-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="692b3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="692b3-124">OUTPUTS</span></span>

### <span data-ttu-id="692b3-125">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="692b3-125">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="692b3-126">Note</span><span class="sxs-lookup"><span data-stu-id="692b3-126">NOTES</span></span>

## <span data-ttu-id="692b3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="692b3-127">RELATED LINKS</span></span>

[<span data-ttu-id="692b3-128">New-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="692b3-128">New-AzureRmCognitiveServicesAccount</span></span>](./New-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="692b3-129">Remove-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="692b3-129">Remove-AzureRmCognitiveServicesAccount</span></span>](./Remove-AzureRmCognitiveServicesAccount.md)

[<span data-ttu-id="692b3-130">Set-AzureRmCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="692b3-130">Set-AzureRmCognitiveServicesAccount</span></span>](./Set-AzureRmCognitiveServicesAccount.md)


