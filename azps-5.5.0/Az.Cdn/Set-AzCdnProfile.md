---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177863"
---
# <span data-ttu-id="f0b93-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="f0b93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0b93-102">SYNOPSIS</span></span>
<span data-ttu-id="f0b93-103">Aggiorna un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="f0b93-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="f0b93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0b93-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0b93-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0b93-105">DESCRIPTION</span></span>
<span data-ttu-id="f0b93-106">Il cmdlet **Set-AzCdnProfile** aggiorna un profilo di rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0b93-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="f0b93-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0b93-107">EXAMPLES</span></span>

## <span data-ttu-id="f0b93-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0b93-108">PARAMETERS</span></span>

### <span data-ttu-id="f0b93-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-109">-CdnProfile</span></span>
<span data-ttu-id="f0b93-110">Specifica il profilo aggiornato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b93-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="f0b93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-111">-DefaultProfile</span></span>
<span data-ttu-id="f0b93-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f0b93-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0b93-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0b93-113">-Confirm</span></span>
<span data-ttu-id="f0b93-114">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0b93-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0b93-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0b93-115">-WhatIf</span></span>
<span data-ttu-id="f0b93-116">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0b93-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0b93-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0b93-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0b93-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0b93-118">CommonParameters</span></span>
<span data-ttu-id="f0b93-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0b93-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0b93-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0b93-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0b93-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0b93-121">INPUTS</span></span>

### <span data-ttu-id="f0b93-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f0b93-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0b93-123">OUTPUTS</span></span>

### <span data-ttu-id="f0b93-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="f0b93-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0b93-125">NOTES</span></span>

## <span data-ttu-id="f0b93-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0b93-126">RELATED LINKS</span></span>

[<span data-ttu-id="f0b93-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="f0b93-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="f0b93-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="f0b93-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


