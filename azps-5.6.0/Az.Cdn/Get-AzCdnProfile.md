---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: e82e455d603ca4fd5d577e18337c93a2368fbcf5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004606"
---
# <span data-ttu-id="695dd-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="695dd-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="695dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="695dd-102">SYNOPSIS</span></span>
<span data-ttu-id="695dd-103">Ottiene un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="695dd-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="695dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="695dd-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="695dd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="695dd-105">DESCRIPTION</span></span>
<span data-ttu-id="695dd-106">Il cmdlet **Get-AzCdnProfile** ottiene un profilo di rete per la distribuzione di contenuti (CDN) di Azure e le relative informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="695dd-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="695dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="695dd-107">EXAMPLES</span></span>

## <span data-ttu-id="695dd-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="695dd-108">PARAMETERS</span></span>

### <span data-ttu-id="695dd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="695dd-109">-DefaultProfile</span></span>
<span data-ttu-id="695dd-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="695dd-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="695dd-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="695dd-111">-ProfileName</span></span>
<span data-ttu-id="695dd-112">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="695dd-112">Specifies the name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="695dd-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="695dd-113">-ResourceGroupName</span></span>
<span data-ttu-id="695dd-114">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="695dd-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="695dd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="695dd-115">CommonParameters</span></span>
<span data-ttu-id="695dd-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="695dd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="695dd-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="695dd-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="695dd-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="695dd-118">INPUTS</span></span>

### <span data-ttu-id="695dd-119">System.String</span><span class="sxs-lookup"><span data-stu-id="695dd-119">System.String</span></span>

## <span data-ttu-id="695dd-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="695dd-120">OUTPUTS</span></span>

### <span data-ttu-id="695dd-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="695dd-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="695dd-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="695dd-122">NOTES</span></span>

## <span data-ttu-id="695dd-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="695dd-123">RELATED LINKS</span></span>

[<span data-ttu-id="695dd-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="695dd-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="695dd-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="695dd-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="695dd-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="695dd-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


