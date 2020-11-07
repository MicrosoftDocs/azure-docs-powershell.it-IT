---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 3b12fdd4b82446f67eaaaec7a46bbc7f49307e94
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852222"
---
# <span data-ttu-id="7cc37-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="7cc37-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="7cc37-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7cc37-102">SYNOPSIS</span></span>
<span data-ttu-id="7cc37-103">Ottenere gli usi correnti per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7cc37-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="7cc37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7cc37-104">SYNTAX</span></span>

### <span data-ttu-id="7cc37-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7cc37-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc37-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc37-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7cc37-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7cc37-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7cc37-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7cc37-108">DESCRIPTION</span></span>
<span data-ttu-id="7cc37-109">Il cmdlet **Get-AzCognitiveServicesAccountUsage** ottiene gli usi correnti per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7cc37-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="7cc37-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7cc37-110">EXAMPLES</span></span>

### <span data-ttu-id="7cc37-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7cc37-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="7cc37-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7cc37-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="7cc37-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7cc37-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="7cc37-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7cc37-114">PARAMETERS</span></span>

### <span data-ttu-id="7cc37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cc37-115">-DefaultProfile</span></span>
<span data-ttu-id="7cc37-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7cc37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7cc37-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7cc37-117">-InputObject</span></span>
<span data-ttu-id="7cc37-118">Oggetto account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7cc37-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc37-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7cc37-119">-Name</span></span>
<span data-ttu-id="7cc37-120">Nome account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7cc37-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc37-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cc37-121">-ResourceGroupName</span></span>
<span data-ttu-id="7cc37-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7cc37-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cc37-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7cc37-123">-ResourceId</span></span>
<span data-ttu-id="7cc37-124">ID risorsa account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="7cc37-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cc37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cc37-125">CommonParameters</span></span>
<span data-ttu-id="7cc37-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cc37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cc37-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cc37-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cc37-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7cc37-128">INPUTS</span></span>

### <span data-ttu-id="7cc37-129">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7cc37-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="7cc37-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7cc37-130">System.String</span></span>

## <span data-ttu-id="7cc37-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7cc37-131">OUTPUTS</span></span>

### <span data-ttu-id="7cc37-132">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="7cc37-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="7cc37-133">Note</span><span class="sxs-lookup"><span data-stu-id="7cc37-133">NOTES</span></span>

## <span data-ttu-id="7cc37-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7cc37-134">RELATED LINKS</span></span>
