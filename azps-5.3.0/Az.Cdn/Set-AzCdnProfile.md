---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnProfile.md
ms.openlocfilehash: 341d46e5dd4ceefaf8baa76a71de462559115a5d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477967"
---
# <span data-ttu-id="07155-101">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07155-101">Set-AzCdnProfile</span></span>

## <span data-ttu-id="07155-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07155-102">SYNOPSIS</span></span>
<span data-ttu-id="07155-103">Aggiorna un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="07155-103">Updates a CDN profile.</span></span>

## <span data-ttu-id="07155-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07155-104">SYNTAX</span></span>

```
Set-AzCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="07155-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07155-105">DESCRIPTION</span></span>
<span data-ttu-id="07155-106">Il cmdlet **set-AzCdnProfile** aggiorna un profilo della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="07155-106">The **Set-AzCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="07155-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07155-107">EXAMPLES</span></span>

## <span data-ttu-id="07155-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07155-108">PARAMETERS</span></span>

### <span data-ttu-id="07155-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="07155-109">-CdnProfile</span></span>
<span data-ttu-id="07155-110">Specifica il profilo che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="07155-110">Specifies the profile that this cmdlet updates.</span></span>

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

### <span data-ttu-id="07155-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07155-111">-DefaultProfile</span></span>
<span data-ttu-id="07155-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="07155-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07155-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07155-113">-Confirm</span></span>
<span data-ttu-id="07155-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07155-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07155-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07155-115">-WhatIf</span></span>
<span data-ttu-id="07155-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07155-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07155-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07155-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07155-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07155-118">CommonParameters</span></span>
<span data-ttu-id="07155-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07155-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07155-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07155-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07155-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07155-121">INPUTS</span></span>

### <span data-ttu-id="07155-122">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="07155-122">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="07155-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07155-123">OUTPUTS</span></span>

### <span data-ttu-id="07155-124">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="07155-124">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="07155-125">Note</span><span class="sxs-lookup"><span data-stu-id="07155-125">NOTES</span></span>

## <span data-ttu-id="07155-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07155-126">RELATED LINKS</span></span>

[<span data-ttu-id="07155-127">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07155-127">Get-AzCdnProfile</span></span>](./Get-AzCdnProfile.md)

[<span data-ttu-id="07155-128">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07155-128">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="07155-129">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="07155-129">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)


