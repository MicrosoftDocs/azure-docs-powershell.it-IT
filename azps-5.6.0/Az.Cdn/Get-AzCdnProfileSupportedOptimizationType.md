---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: f26e1bd19b9856df7bf68de6c8afddefb3ee64a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988482"
---
# <span data-ttu-id="5d4fa-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="5d4fa-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="5d4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4fa-103">Ottiene i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="5d4fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d4fa-104">SYNTAX</span></span>

### <span data-ttu-id="5d4fa-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5d4fa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d4fa-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d4fa-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d4fa-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5d4fa-107">DESCRIPTION</span></span>
<span data-ttu-id="5d4fa-108">Il cmdlet **Get-AzCdnProfileSupportedOptimizationType** ottiene i tipi di ottimizzazione supportati per il profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="5d4fa-109">Un utente può creare un endpoint con un tipo di ottimizzazione dai valori elencati.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="5d4fa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d4fa-110">EXAMPLES</span></span>

### <span data-ttu-id="5d4fa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5d4fa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="5d4fa-112">Ottenere i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="5d4fa-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d4fa-113">PARAMETERS</span></span>

### <span data-ttu-id="5d4fa-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5d4fa-114">-CdnProfile</span></span>
<span data-ttu-id="5d4fa-115">Oggetto profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="5d4fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4fa-116">-DefaultProfile</span></span>
<span data-ttu-id="5d4fa-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d4fa-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5d4fa-118">-ProfileName</span></span>
<span data-ttu-id="5d4fa-119">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-119">The name of the profile.</span></span>

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

### <span data-ttu-id="5d4fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="5d4fa-121">Gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5d4fa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4fa-122">CommonParameters</span></span>
<span data-ttu-id="5d4fa-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4fa-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d4fa-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4fa-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="5d4fa-125">INPUTS</span></span>

### <span data-ttu-id="5d4fa-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="5d4fa-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="5d4fa-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d4fa-127">OUTPUTS</span></span>

### <span data-ttu-id="5d4fa-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="5d4fa-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="5d4fa-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="5d4fa-129">NOTES</span></span>

## <span data-ttu-id="5d4fa-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d4fa-130">RELATED LINKS</span></span>
