---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: e6434b2b5b07cad811f245d72e1d6bd34da63bb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519757"
---
# <span data-ttu-id="4bd0a-101">Get-AzureRmCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="4bd0a-101">Get-AzureRmCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="4bd0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4bd0a-102">SYNOPSIS</span></span>
<span data-ttu-id="4bd0a-103">Ottiene i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-103">Gets the supported optimization types for a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bd0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4bd0a-104">SYNTAX</span></span>

### <span data-ttu-id="4bd0a-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4bd0a-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bd0a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4bd0a-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileSupportedOptimizationType -CdnProfile <PSProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bd0a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4bd0a-107">DESCRIPTION</span></span>
<span data-ttu-id="4bd0a-108">Il cmdlet **Get-AzureRmCdnProfileSupportedOptimizationType** ottiene i tipi di ottimizzazione supportati per il profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-108">The **Get-AzureRmCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="4bd0a-109">Un utente può creare un endpoint con un tipo di ottimizzazione dei valori elencati.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="4bd0a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4bd0a-110">EXAMPLES</span></span>

### <span data-ttu-id="4bd0a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4bd0a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="4bd0a-112">Ottenere i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="4bd0a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4bd0a-113">PARAMETERS</span></span>

### <span data-ttu-id="4bd0a-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="4bd0a-114">-CdnProfile</span></span>
<span data-ttu-id="4bd0a-115">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="4bd0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bd0a-116">-DefaultProfile</span></span>
<span data-ttu-id="4bd0a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bd0a-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="4bd0a-118">-ProfileName</span></span>
<span data-ttu-id="4bd0a-119">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-119">The name of the profile.</span></span>

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

### <span data-ttu-id="4bd0a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bd0a-120">-ResourceGroupName</span></span>
<span data-ttu-id="4bd0a-121">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="4bd0a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bd0a-122">CommonParameters</span></span>
<span data-ttu-id="4bd0a-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bd0a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bd0a-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bd0a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bd0a-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4bd0a-125">INPUTS</span></span>

### <span data-ttu-id="4bd0a-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="4bd0a-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="4bd0a-127">Parametri: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4bd0a-127">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="4bd0a-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4bd0a-128">OUTPUTS</span></span>

### <span data-ttu-id="4bd0a-129">Microsoft. Azure. Commands. CDN. Models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="4bd0a-129">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="4bd0a-130">Note</span><span class="sxs-lookup"><span data-stu-id="4bd0a-130">NOTES</span></span>

## <span data-ttu-id="4bd0a-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4bd0a-131">RELATED LINKS</span></span>
