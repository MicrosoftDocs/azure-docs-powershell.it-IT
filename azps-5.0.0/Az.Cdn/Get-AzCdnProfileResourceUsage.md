---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202991"
---
# <span data-ttu-id="ca5d9-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ca5d9-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="ca5d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca5d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5d9-103">Ottiene l'utilizzo delle risorse di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="ca5d9-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="ca5d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca5d9-104">SYNTAX</span></span>

### <span data-ttu-id="ca5d9-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca5d9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca5d9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca5d9-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca5d9-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca5d9-107">DESCRIPTION</span></span>
<span data-ttu-id="ca5d9-108">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="ca5d9-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ca5d9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca5d9-109">EXAMPLES</span></span>

### <span data-ttu-id="ca5d9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca5d9-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ca5d9-111">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ca5d9-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="ca5d9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca5d9-112">PARAMETERS</span></span>

### <span data-ttu-id="ca5d9-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="ca5d9-113">-CdnProfile</span></span>
<span data-ttu-id="ca5d9-114">Oggetto profilo di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="ca5d9-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="ca5d9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca5d9-115">-DefaultProfile</span></span>
<span data-ttu-id="ca5d9-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ca5d9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca5d9-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ca5d9-117">-ProfileName</span></span>
<span data-ttu-id="ca5d9-118">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="ca5d9-118">The name of the profile.</span></span>

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

### <span data-ttu-id="ca5d9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca5d9-119">-ResourceGroupName</span></span>
<span data-ttu-id="ca5d9-120">Il gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="ca5d9-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="ca5d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5d9-121">CommonParameters</span></span>
<span data-ttu-id="ca5d9-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca5d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5d9-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca5d9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5d9-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca5d9-124">INPUTS</span></span>

### <span data-ttu-id="ca5d9-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="ca5d9-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="ca5d9-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca5d9-126">OUTPUTS</span></span>

### <span data-ttu-id="ca5d9-127">Microsoft. Azure. Commands. CDN. Models. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="ca5d9-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="ca5d9-128">Note</span><span class="sxs-lookup"><span data-stu-id="ca5d9-128">NOTES</span></span>

## <span data-ttu-id="ca5d9-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca5d9-129">RELATED LINKS</span></span>
