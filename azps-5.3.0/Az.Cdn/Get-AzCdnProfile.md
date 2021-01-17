---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfile.md
ms.openlocfilehash: 1af77b3fec469b9bb60d5531c89534d5de11b4f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488667"
---
# <span data-ttu-id="870f5-101">Get-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="870f5-101">Get-AzCdnProfile</span></span>

## <span data-ttu-id="870f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="870f5-102">SYNOPSIS</span></span>
<span data-ttu-id="870f5-103">Ottiene un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="870f5-103">Gets a CDN profile.</span></span>

## <span data-ttu-id="870f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="870f5-104">SYNTAX</span></span>

```
Get-AzCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="870f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="870f5-105">DESCRIPTION</span></span>
<span data-ttu-id="870f5-106">Il cmdlet **Get-AzCdnProfile** ottiene un profilo CDN (Azure Content Delivery Network) e le relative informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="870f5-106">The **Get-AzCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="870f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="870f5-107">EXAMPLES</span></span>

## <span data-ttu-id="870f5-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="870f5-108">PARAMETERS</span></span>

### <span data-ttu-id="870f5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870f5-109">-DefaultProfile</span></span>
<span data-ttu-id="870f5-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="870f5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="870f5-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="870f5-111">-ProfileName</span></span>
<span data-ttu-id="870f5-112">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="870f5-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="870f5-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870f5-113">-ResourceGroupName</span></span>
<span data-ttu-id="870f5-114">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="870f5-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="870f5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870f5-115">CommonParameters</span></span>
<span data-ttu-id="870f5-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="870f5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870f5-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="870f5-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870f5-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="870f5-118">INPUTS</span></span>

### <span data-ttu-id="870f5-119">System. String</span><span class="sxs-lookup"><span data-stu-id="870f5-119">System.String</span></span>

## <span data-ttu-id="870f5-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="870f5-120">OUTPUTS</span></span>

### <span data-ttu-id="870f5-121">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="870f5-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="870f5-122">Note</span><span class="sxs-lookup"><span data-stu-id="870f5-122">NOTES</span></span>

## <span data-ttu-id="870f5-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="870f5-123">RELATED LINKS</span></span>

[<span data-ttu-id="870f5-124">New-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="870f5-124">New-AzCdnProfile</span></span>](./New-AzCdnProfile.md)

[<span data-ttu-id="870f5-125">Remove-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="870f5-125">Remove-AzCdnProfile</span></span>](./Remove-AzCdnProfile.md)

[<span data-ttu-id="870f5-126">Set-AzCdnProfile</span><span class="sxs-lookup"><span data-stu-id="870f5-126">Set-AzCdnProfile</span></span>](./Set-AzCdnProfile.md)


