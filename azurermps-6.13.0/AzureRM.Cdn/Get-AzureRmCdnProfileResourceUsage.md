---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 3d0f93a732739b94832a5e411580fb80958b27c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509300"
---
# <span data-ttu-id="5fe95-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="5fe95-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="5fe95-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fe95-102">SYNOPSIS</span></span>
<span data-ttu-id="5fe95-103">Ottiene l'utilizzo delle risorse di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="5fe95-103">Gets the resource usage of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fe95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fe95-104">SYNTAX</span></span>

### <span data-ttu-id="5fe95-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5fe95-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5fe95-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5fe95-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fe95-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fe95-107">DESCRIPTION</span></span>
<span data-ttu-id="5fe95-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="5fe95-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="5fe95-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fe95-109">EXAMPLES</span></span>

### <span data-ttu-id="5fe95-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5fe95-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5fe95-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="5fe95-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="5fe95-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fe95-112">PARAMETERS</span></span>

### <span data-ttu-id="5fe95-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="5fe95-113">-CdnProfile</span></span>
<span data-ttu-id="5fe95-114">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="5fe95-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="5fe95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fe95-115">-DefaultProfile</span></span>
<span data-ttu-id="5fe95-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5fe95-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fe95-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5fe95-117">-ProfileName</span></span>
<span data-ttu-id="5fe95-118">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="5fe95-118">The name of the profile.</span></span>

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

### <span data-ttu-id="5fe95-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fe95-119">-ResourceGroupName</span></span>
<span data-ttu-id="5fe95-120">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="5fe95-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="5fe95-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fe95-121">CommonParameters</span></span>
<span data-ttu-id="5fe95-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fe95-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fe95-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fe95-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fe95-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fe95-124">INPUTS</span></span>

### <span data-ttu-id="5fe95-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="5fe95-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="5fe95-126">Parametri: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5fe95-126">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="5fe95-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fe95-127">OUTPUTS</span></span>

### <span data-ttu-id="5fe95-128">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="5fe95-128">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="5fe95-129">Note</span><span class="sxs-lookup"><span data-stu-id="5fe95-129">NOTES</span></span>

## <span data-ttu-id="5fe95-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fe95-130">RELATED LINKS</span></span>
