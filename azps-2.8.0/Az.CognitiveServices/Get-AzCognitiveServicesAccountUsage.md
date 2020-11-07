---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: 7d197cdb7ee8fbfa63d8a3b36da5f038a5a0b8de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675498"
---
# <span data-ttu-id="d498b-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="d498b-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="d498b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d498b-102">SYNOPSIS</span></span>
<span data-ttu-id="d498b-103">Ottenere gli usi correnti per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d498b-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="d498b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d498b-104">SYNTAX</span></span>

### <span data-ttu-id="d498b-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d498b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d498b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d498b-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d498b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d498b-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d498b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d498b-108">DESCRIPTION</span></span>
<span data-ttu-id="d498b-109">Il cmdlet **Get-AzCognitiveServicesAccountUsage** ottiene gli usi correnti per un account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d498b-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="d498b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d498b-110">EXAMPLES</span></span>

### <span data-ttu-id="d498b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d498b-111">Example 1</span></span>
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

### <span data-ttu-id="d498b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d498b-112">Example 2</span></span>
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

### <span data-ttu-id="d498b-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="d498b-113">Example 3</span></span>
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

## <span data-ttu-id="d498b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d498b-114">PARAMETERS</span></span>

### <span data-ttu-id="d498b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d498b-115">-DefaultProfile</span></span>
<span data-ttu-id="d498b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d498b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d498b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d498b-117">-InputObject</span></span>
<span data-ttu-id="d498b-118">Oggetto account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d498b-118">Cognitive Services Account Object.</span></span>

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

### <span data-ttu-id="d498b-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d498b-119">-Name</span></span>
<span data-ttu-id="d498b-120">Nome account servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d498b-120">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="d498b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d498b-121">-ResourceGroupName</span></span>
<span data-ttu-id="d498b-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d498b-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d498b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d498b-123">-ResourceId</span></span>
<span data-ttu-id="d498b-124">ID risorsa account di servizi cognitivi.</span><span class="sxs-lookup"><span data-stu-id="d498b-124">Cognitive Services Account Resource ID.</span></span>

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

### <span data-ttu-id="d498b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d498b-125">CommonParameters</span></span>
<span data-ttu-id="d498b-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d498b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d498b-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d498b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d498b-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d498b-128">INPUTS</span></span>

### <span data-ttu-id="d498b-129">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d498b-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="d498b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d498b-130">System.String</span></span>

## <span data-ttu-id="d498b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d498b-131">OUTPUTS</span></span>

### <span data-ttu-id="d498b-132">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="d498b-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="d498b-133">Note</span><span class="sxs-lookup"><span data-stu-id="d498b-133">NOTES</span></span>

## <span data-ttu-id="d498b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d498b-134">RELATED LINKS</span></span>