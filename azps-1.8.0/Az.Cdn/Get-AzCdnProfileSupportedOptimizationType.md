---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: be7528f33bc51732c9345bbf7c9b718f590a8a5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684872"
---
# <span data-ttu-id="7d43d-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7d43d-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="7d43d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d43d-102">SYNOPSIS</span></span>
<span data-ttu-id="7d43d-103">Ottiene i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="7d43d-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7d43d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d43d-104">SYNTAX</span></span>

### <span data-ttu-id="7d43d-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d43d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d43d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d43d-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d43d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d43d-107">DESCRIPTION</span></span>
<span data-ttu-id="7d43d-108">Il cmdlet **Get-AzCdnProfileSupportedOptimizationType** ottiene i tipi di ottimizzazione supportati per il profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="7d43d-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="7d43d-109">Un utente può creare un endpoint con un tipo di ottimizzazione dei valori elencati.</span><span class="sxs-lookup"><span data-stu-id="7d43d-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="7d43d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d43d-110">EXAMPLES</span></span>

### <span data-ttu-id="7d43d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d43d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="7d43d-112">Ottenere i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="7d43d-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="7d43d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d43d-113">PARAMETERS</span></span>

### <span data-ttu-id="7d43d-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7d43d-114">-CdnProfile</span></span>
<span data-ttu-id="7d43d-115">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="7d43d-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d43d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d43d-116">-DefaultProfile</span></span>
<span data-ttu-id="7d43d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d43d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d43d-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7d43d-118">-ProfileName</span></span>
<span data-ttu-id="7d43d-119">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="7d43d-119">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d43d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d43d-120">-ResourceGroupName</span></span>
<span data-ttu-id="7d43d-121">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="7d43d-121">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d43d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d43d-122">CommonParameters</span></span>
<span data-ttu-id="7d43d-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d43d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d43d-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d43d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d43d-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d43d-125">INPUTS</span></span>

### <span data-ttu-id="7d43d-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7d43d-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="7d43d-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d43d-127">OUTPUTS</span></span>

### <span data-ttu-id="7d43d-128">Microsoft. Azure. Commands. CDN. Models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="7d43d-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="7d43d-129">Note</span><span class="sxs-lookup"><span data-stu-id="7d43d-129">NOTES</span></span>

## <span data-ttu-id="7d43d-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d43d-130">RELATED LINKS</span></span>
