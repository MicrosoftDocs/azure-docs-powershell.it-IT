---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190542"
---
# <span data-ttu-id="98030-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="98030-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="98030-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="98030-102">SYNOPSIS</span></span>
<span data-ttu-id="98030-103">Ottiene i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="98030-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="98030-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="98030-104">SYNTAX</span></span>

### <span data-ttu-id="98030-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="98030-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98030-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98030-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="98030-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="98030-107">DESCRIPTION</span></span>
<span data-ttu-id="98030-108">Il cmdlet **Get-AzCdnProfileSupportedOptimizationType** ottiene i tipi di ottimizzazione supportati per il profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="98030-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="98030-109">Un utente può creare un endpoint con un tipo di ottimizzazione dei valori elencati.</span><span class="sxs-lookup"><span data-stu-id="98030-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="98030-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="98030-110">EXAMPLES</span></span>

### <span data-ttu-id="98030-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="98030-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="98030-112">Ottenere i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="98030-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="98030-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="98030-113">PARAMETERS</span></span>

### <span data-ttu-id="98030-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="98030-114">-CdnProfile</span></span>
<span data-ttu-id="98030-115">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="98030-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="98030-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98030-116">-DefaultProfile</span></span>
<span data-ttu-id="98030-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="98030-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98030-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="98030-118">-ProfileName</span></span>
<span data-ttu-id="98030-119">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="98030-119">The name of the profile.</span></span>

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

### <span data-ttu-id="98030-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98030-120">-ResourceGroupName</span></span>
<span data-ttu-id="98030-121">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="98030-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="98030-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98030-122">CommonParameters</span></span>
<span data-ttu-id="98030-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98030-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98030-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98030-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98030-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="98030-125">INPUTS</span></span>

### <span data-ttu-id="98030-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="98030-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="98030-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="98030-127">OUTPUTS</span></span>

### <span data-ttu-id="98030-128">Microsoft. Azure. Commands. CDN. Models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="98030-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="98030-129">Note</span><span class="sxs-lookup"><span data-stu-id="98030-129">NOTES</span></span>

## <span data-ttu-id="98030-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="98030-130">RELATED LINKS</span></span>
