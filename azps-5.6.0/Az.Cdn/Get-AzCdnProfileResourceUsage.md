---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 1a4e3f08653f6c7bda799b55618caff4e77fe7bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004589"
---
# <span data-ttu-id="227ba-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="227ba-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="227ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="227ba-102">SYNOPSIS</span></span>
<span data-ttu-id="227ba-103">Recupera l'uso delle risorse di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="227ba-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="227ba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="227ba-104">SYNTAX</span></span>

### <span data-ttu-id="227ba-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="227ba-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="227ba-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="227ba-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="227ba-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="227ba-107">DESCRIPTION</span></span>
<span data-ttu-id="227ba-108">{{Inserire la descrizione}}</span><span class="sxs-lookup"><span data-stu-id="227ba-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="227ba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="227ba-109">EXAMPLES</span></span>

### <span data-ttu-id="227ba-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="227ba-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="227ba-111">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="227ba-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="227ba-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="227ba-112">PARAMETERS</span></span>

### <span data-ttu-id="227ba-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="227ba-113">-CdnProfile</span></span>
<span data-ttu-id="227ba-114">Oggetto profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="227ba-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="227ba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227ba-115">-DefaultProfile</span></span>
<span data-ttu-id="227ba-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="227ba-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="227ba-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="227ba-117">-ProfileName</span></span>
<span data-ttu-id="227ba-118">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="227ba-118">The name of the profile.</span></span>

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

### <span data-ttu-id="227ba-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227ba-119">-ResourceGroupName</span></span>
<span data-ttu-id="227ba-120">Gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="227ba-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="227ba-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227ba-121">CommonParameters</span></span>
<span data-ttu-id="227ba-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="227ba-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227ba-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="227ba-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227ba-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="227ba-124">INPUTS</span></span>

### <span data-ttu-id="227ba-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="227ba-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="227ba-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="227ba-126">OUTPUTS</span></span>

### <span data-ttu-id="227ba-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="227ba-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="227ba-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="227ba-128">NOTES</span></span>

## <span data-ttu-id="227ba-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="227ba-129">RELATED LINKS</span></span>
