---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357332"
---
# <span data-ttu-id="2ea9c-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="2ea9c-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="2ea9c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2ea9c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ea9c-103">Ottiene i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="2ea9c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2ea9c-104">SYNTAX</span></span>

### <span data-ttu-id="2ea9c-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2ea9c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ea9c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ea9c-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ea9c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2ea9c-107">DESCRIPTION</span></span>
<span data-ttu-id="2ea9c-108">Il cmdlet **Get-AzCdnProfileSupportedOptimizationType** ottiene i tipi di ottimizzazione supportati per il profilo corrente.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="2ea9c-109">Un utente può creare un endpoint con un tipo di ottimizzazione dei valori elencati.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="2ea9c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2ea9c-110">EXAMPLES</span></span>

### <span data-ttu-id="2ea9c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2ea9c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="2ea9c-112">Ottenere i tipi di ottimizzazione supportati per un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="2ea9c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2ea9c-113">PARAMETERS</span></span>

### <span data-ttu-id="2ea9c-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="2ea9c-114">-CdnProfile</span></span>
<span data-ttu-id="2ea9c-115">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="2ea9c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ea9c-116">-DefaultProfile</span></span>
<span data-ttu-id="2ea9c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ea9c-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2ea9c-118">-ProfileName</span></span>
<span data-ttu-id="2ea9c-119">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-119">The name of the profile.</span></span>

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

### <span data-ttu-id="2ea9c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ea9c-120">-ResourceGroupName</span></span>
<span data-ttu-id="2ea9c-121">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="2ea9c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ea9c-122">CommonParameters</span></span>
<span data-ttu-id="2ea9c-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ea9c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ea9c-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ea9c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ea9c-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2ea9c-125">INPUTS</span></span>

### <span data-ttu-id="2ea9c-126">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="2ea9c-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="2ea9c-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2ea9c-127">OUTPUTS</span></span>

### <span data-ttu-id="2ea9c-128">Microsoft. Azure. Commands. CDN. Models. profile. PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="2ea9c-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="2ea9c-129">Note</span><span class="sxs-lookup"><span data-stu-id="2ea9c-129">NOTES</span></span>

## <span data-ttu-id="2ea9c-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2ea9c-130">RELATED LINKS</span></span>
