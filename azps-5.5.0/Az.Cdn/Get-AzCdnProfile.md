---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181854"
---
# <span data-ttu-id="82843-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="82843-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="82843-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82843-102">SYNOPSIS</span></span>
<span data-ttu-id="82843-103">Ottiene un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="82843-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="82843-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="82843-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82843-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="82843-105">DESCRIPTION</span></span>
<span data-ttu-id="82843-106">Il cmdlet **Get-AzCdnProfile** ottiene un profilo di rete per la distribuzione di contenuti (CDN) di Azure e le relative informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="82843-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="82843-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="82843-107">EXAMPLES</span></span>

## <span data-ttu-id="82843-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82843-108">PARAMETERS</span></span>

### <span data-ttu-id="82843-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82843-109">-DefaultProfile</span></span>
<span data-ttu-id="82843-110">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="82843-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82843-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="82843-111">-ProfileName</span></span>
<span data-ttu-id="82843-112">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="82843-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="82843-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82843-113">-ResourceGroupName</span></span>
<span data-ttu-id="82843-114">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="82843-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="82843-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82843-115">CommonParameters</span></span>
<span data-ttu-id="82843-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82843-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82843-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82843-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82843-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="82843-118">INPUTS</span></span>

### <span data-ttu-id="82843-119">System.String</span><span class="sxs-lookup"><span data-stu-id="82843-119">System.String</span></span>

## <span data-ttu-id="82843-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="82843-120">OUTPUTS</span></span>

### <span data-ttu-id="82843-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="82843-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="82843-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="82843-122">NOTES</span></span>

## <span data-ttu-id="82843-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="82843-123">RELATED LINKS</span></span>

[<span data-ttu-id="82843-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="82843-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="82843-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="82843-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="82843-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="82843-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


