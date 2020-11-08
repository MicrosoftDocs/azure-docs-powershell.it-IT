---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021643"
---
# <span data-ttu-id="d1c5d-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d1c5d-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="d1c5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1c5d-102">SYNOPSIS</span></span>
<span data-ttu-id="d1c5d-103">Ottiene un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="d1c5d-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="d1c5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1c5d-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1c5d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1c5d-105">DESCRIPTION</span></span>
<span data-ttu-id="d1c5d-106">Il cmdlet **Get-AzCdnProfile** ottiene un profilo CDN (Azure Content Delivery Network) e le relative informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="d1c5d-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="d1c5d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1c5d-107">EXAMPLES</span></span>

## <span data-ttu-id="d1c5d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1c5d-108">PARAMETERS</span></span>

### <span data-ttu-id="d1c5d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1c5d-109">-DefaultProfile</span></span>
<span data-ttu-id="d1c5d-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d1c5d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d1c5d-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d1c5d-111">-ProfileName</span></span>
<span data-ttu-id="d1c5d-112">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="d1c5d-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="d1c5d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1c5d-113">-ResourceGroupName</span></span>
<span data-ttu-id="d1c5d-114">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="d1c5d-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="d1c5d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1c5d-115">CommonParameters</span></span>
<span data-ttu-id="d1c5d-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1c5d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1c5d-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1c5d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1c5d-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1c5d-118">INPUTS</span></span>

### <span data-ttu-id="d1c5d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d1c5d-119">System.String</span></span>

## <span data-ttu-id="d1c5d-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1c5d-120">OUTPUTS</span></span>

### <span data-ttu-id="d1c5d-121">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="d1c5d-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="d1c5d-122">Note</span><span class="sxs-lookup"><span data-stu-id="d1c5d-122">NOTES</span></span>

## <span data-ttu-id="d1c5d-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1c5d-123">RELATED LINKS</span></span>

[<span data-ttu-id="d1c5d-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d1c5d-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="d1c5d-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d1c5d-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="d1c5d-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="d1c5d-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


