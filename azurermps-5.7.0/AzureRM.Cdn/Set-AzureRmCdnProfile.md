---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 863DD160-4443-4D50-804E-089255F3EA4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/set-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Set-AzureRmCdnProfile.md
ms.openlocfilehash: 033755c47965420d3983cc8b3a4d2731ab331152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514536"
---
# <span data-ttu-id="87933-101">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87933-101">Set-AzureRmCdnProfile</span></span>

## <span data-ttu-id="87933-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87933-102">SYNOPSIS</span></span>
<span data-ttu-id="87933-103">Aggiorna un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="87933-103">Updates a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87933-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87933-104">SYNTAX</span></span>

```
Set-AzureRmCdnProfile -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="87933-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87933-105">DESCRIPTION</span></span>
<span data-ttu-id="87933-106">Il cmdlet **set-AzureRmCdnProfile** aggiorna un profilo della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="87933-106">The **Set-AzureRmCdnProfile** cmdlet updates an Azure Content Delivery Network (CDN) profile.</span></span>

## <span data-ttu-id="87933-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87933-107">EXAMPLES</span></span>

## <span data-ttu-id="87933-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87933-108">PARAMETERS</span></span>

### <span data-ttu-id="87933-109">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="87933-109">-CdnProfile</span></span>
<span data-ttu-id="87933-110">Specifica il profilo che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="87933-110">Specifies the profile that this cmdlet updates.</span></span>

```yaml
Type: PSProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87933-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87933-111">-DefaultProfile</span></span>
<span data-ttu-id="87933-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="87933-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87933-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="87933-113">-Confirm</span></span>
<span data-ttu-id="87933-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87933-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87933-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87933-115">-WhatIf</span></span>
<span data-ttu-id="87933-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87933-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87933-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="87933-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87933-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87933-118">CommonParameters</span></span>
<span data-ttu-id="87933-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87933-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87933-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87933-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87933-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87933-121">INPUTS</span></span>

### <span data-ttu-id="87933-122">PSProfile</span><span class="sxs-lookup"><span data-stu-id="87933-122">PSProfile</span></span>
<span data-ttu-id="87933-123">Il parametro ' CdnProfile ' accetta il valore di tipo ' PSProfile ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="87933-123">Parameter 'CdnProfile' accepts value of type 'PSProfile' from the pipeline</span></span>

## <span data-ttu-id="87933-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87933-124">OUTPUTS</span></span>

### <span data-ttu-id="87933-125">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="87933-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="87933-126">Note</span><span class="sxs-lookup"><span data-stu-id="87933-126">NOTES</span></span>

## <span data-ttu-id="87933-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87933-127">RELATED LINKS</span></span>

[<span data-ttu-id="87933-128">Get-AzureRMCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87933-128">Get-AzureRMCdnProfile</span></span>](./Get-AzureRMCdnProfile.md)

[<span data-ttu-id="87933-129">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87933-129">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="87933-130">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="87933-130">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)


