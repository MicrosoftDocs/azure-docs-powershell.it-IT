---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: a549e6c94ae43c8c1cc267448552565f932aa63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508380"
---
# <span data-ttu-id="21879-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="21879-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="21879-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21879-102">SYNOPSIS</span></span>
<span data-ttu-id="21879-103">Ottenere gli usi correnti per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="21879-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21879-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21879-104">SYNTAX</span></span>

### <span data-ttu-id="21879-105">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="21879-105">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="21879-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="21879-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="21879-107">ResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="21879-107">ResourceNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21879-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21879-108">DESCRIPTION</span></span>
<span data-ttu-id="21879-109">Il cmdlet **Get-AzureRmCognitiveServicesAccountUsage** ottiene gli usi correnti per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="21879-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="21879-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21879-110">EXAMPLES</span></span>

### <span data-ttu-id="21879-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="21879-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="21879-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="21879-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="21879-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="21879-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="21879-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21879-114">PARAMETERS</span></span>

### <span data-ttu-id="21879-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21879-115">-DefaultProfile</span></span>
<span data-ttu-id="21879-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21879-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21879-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21879-117">-InputObject</span></span>
<span data-ttu-id="21879-118">Oggetto account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="21879-118">Cognitive Services Account Object.</span></span>
```yaml
Type: PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21879-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="21879-119">-Name</span></span>
<span data-ttu-id="21879-120">Nome account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="21879-120">Cognitive Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21879-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21879-121">-ResourceGroupName</span></span>
<span data-ttu-id="21879-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="21879-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21879-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21879-123">-ResourceId</span></span>
<span data-ttu-id="21879-124">ID risorsa account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="21879-124">Cognitive Services Account Resource ID.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21879-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21879-125">CommonParameters</span></span>
<span data-ttu-id="21879-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21879-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21879-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21879-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21879-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21879-128">INPUTS</span></span>

### <span data-ttu-id="21879-129">System. String</span><span class="sxs-lookup"><span data-stu-id="21879-129">System.String</span></span>

## <span data-ttu-id="21879-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21879-130">OUTPUTS</span></span>

### <span data-ttu-id="21879-131">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="21879-131">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="21879-132">Note</span><span class="sxs-lookup"><span data-stu-id="21879-132">NOTES</span></span>

## <span data-ttu-id="21879-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21879-133">RELATED LINKS</span></span>
