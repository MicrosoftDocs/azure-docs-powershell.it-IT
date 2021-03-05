---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 88e10d5f887d290139ee465217756c598bef0a3c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975501"
---
# <span data-ttu-id="286b3-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="286b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286b3-102">SYNOPSIS</span></span>
<span data-ttu-id="286b3-103">Aggiorna un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="286b3-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="286b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="286b3-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="286b3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="286b3-105">DESCRIPTION</span></span>
<span data-ttu-id="286b3-106">Il cmdlet **Set-AzCdnProfile** aggiorna un profilo di rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="286b3-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="286b3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="286b3-107">EXAMPLES</span></span>

## <span data-ttu-id="286b3-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="286b3-108">PARAMETERS</span></span>

### <span data-ttu-id="286b3-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-109">-CdnProfile</span></span>
<span data-ttu-id="286b3-110">Specifica il profilo aggiornato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286b3-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="286b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-111">-DefaultProfile</span></span>
<span data-ttu-id="286b3-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="286b3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="286b3-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="286b3-113">-Confirm</span></span>
<span data-ttu-id="286b3-114">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="286b3-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286b3-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286b3-115">-WhatIf</span></span>
<span data-ttu-id="286b3-116">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="286b3-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="286b3-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="286b3-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="286b3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286b3-118">CommonParameters</span></span>
<span data-ttu-id="286b3-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="286b3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286b3-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="286b3-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286b3-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="286b3-121">INPUTS</span></span>

### <span data-ttu-id="286b3-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="286b3-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="286b3-123">OUTPUTS</span></span>

### <span data-ttu-id="286b3-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="286b3-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="286b3-125">NOTES</span></span>

## <span data-ttu-id="286b3-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="286b3-126">RELATED LINKS</span></span>

[<span data-ttu-id="286b3-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="286b3-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="286b3-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="286b3-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


