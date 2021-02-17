---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 8395fc4d90eb4e6d38eda18753761a1bf2598479
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205107"
---
# <span data-ttu-id="e771f-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e771f-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="e771f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e771f-102">SYNOPSIS</span></span>
<span data-ttu-id="e771f-103">Recupera l'uso delle risorse di un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="e771f-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="e771f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e771f-104">SYNTAX</span></span>

### <span data-ttu-id="e771f-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e771f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e771f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e771f-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e771f-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e771f-107">DESCRIPTION</span></span>
<span data-ttu-id="e771f-108">{{Inserire la descrizione}}</span><span class="sxs-lookup"><span data-stu-id="e771f-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e771f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e771f-109">EXAMPLES</span></span>

### <span data-ttu-id="e771f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e771f-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e771f-111">{{ Aggiungi la descrizione di esempio qui }}</span><span class="sxs-lookup"><span data-stu-id="e771f-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e771f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e771f-112">PARAMETERS</span></span>

### <span data-ttu-id="e771f-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e771f-113">-CdnProfile</span></span>
<span data-ttu-id="e771f-114">Oggetto profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="e771f-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="e771f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e771f-115">-DefaultProfile</span></span>
<span data-ttu-id="e771f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e771f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e771f-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e771f-117">-ProfileName</span></span>
<span data-ttu-id="e771f-118">Nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="e771f-118">The name of the profile.</span></span>

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

### <span data-ttu-id="e771f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e771f-119">-ResourceGroupName</span></span>
<span data-ttu-id="e771f-120">Gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="e771f-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e771f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e771f-121">CommonParameters</span></span>
<span data-ttu-id="e771f-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e771f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e771f-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e771f-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e771f-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="e771f-124">INPUTS</span></span>

### <span data-ttu-id="e771f-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="e771f-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e771f-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e771f-126">OUTPUTS</span></span>

### <span data-ttu-id="e771f-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e771f-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="e771f-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="e771f-128">NOTES</span></span>

## <span data-ttu-id="e771f-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e771f-129">RELATED LINKS</span></span>
