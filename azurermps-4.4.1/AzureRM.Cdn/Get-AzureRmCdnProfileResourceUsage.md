---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521982"
---
# <span data-ttu-id="3208f-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="3208f-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="3208f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3208f-102">SYNOPSIS</span></span>
<span data-ttu-id="3208f-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="3208f-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3208f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3208f-104">SYNTAX</span></span>

### <span data-ttu-id="3208f-105">Parametro set per i parametri dei campi (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3208f-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3208f-106">Parametro impostato per i parametri degli oggetti</span><span class="sxs-lookup"><span data-stu-id="3208f-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3208f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3208f-107">DESCRIPTION</span></span>
<span data-ttu-id="3208f-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="3208f-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3208f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3208f-109">EXAMPLES</span></span>

### <span data-ttu-id="3208f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3208f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3208f-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="3208f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="3208f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3208f-112">PARAMETERS</span></span>

### <span data-ttu-id="3208f-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="3208f-113">-CdnProfile</span></span>
<span data-ttu-id="3208f-114">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="3208f-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3208f-115">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="3208f-115">-ProfileName</span></span>
<span data-ttu-id="3208f-116">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="3208f-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3208f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3208f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3208f-118">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="3208f-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3208f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3208f-119">-DefaultProfile</span></span>
<span data-ttu-id="3208f-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3208f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3208f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3208f-121">CommonParameters</span></span>
<span data-ttu-id="3208f-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3208f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3208f-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3208f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3208f-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3208f-124">INPUTS</span></span>

### <span data-ttu-id="3208f-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="3208f-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="3208f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3208f-126">OUTPUTS</span></span>

### <span data-ttu-id="3208f-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="3208f-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="3208f-128">Note</span><span class="sxs-lookup"><span data-stu-id="3208f-128">NOTES</span></span>

## <span data-ttu-id="3208f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3208f-129">RELATED LINKS</span></span>

