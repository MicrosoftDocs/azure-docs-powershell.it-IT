---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: f53b02d54164b6cc4e3aad8cf07357e7f2e156e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520676"
---
# <span data-ttu-id="1a440-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1a440-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="1a440-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a440-102">SYNOPSIS</span></span>
<span data-ttu-id="1a440-103">Ottiene un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="1a440-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a440-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a440-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a440-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a440-105">DESCRIPTION</span></span>
<span data-ttu-id="1a440-106">Il cmdlet **Get-AzureRMCdnProfile** ottiene un profilo CDN (Azure Content Delivery Network) e le relative informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="1a440-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="1a440-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a440-107">EXAMPLES</span></span>

## <span data-ttu-id="1a440-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a440-108">PARAMETERS</span></span>

### <span data-ttu-id="1a440-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a440-109">-DefaultProfile</span></span>
<span data-ttu-id="1a440-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1a440-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a440-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1a440-111">-ProfileName</span></span>
<span data-ttu-id="1a440-112">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="1a440-112">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="1a440-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a440-113">-ResourceGroupName</span></span>
<span data-ttu-id="1a440-114">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="1a440-114">Specifies the name of the resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="1a440-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a440-115">CommonParameters</span></span>
<span data-ttu-id="1a440-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a440-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a440-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a440-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a440-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a440-118">INPUTS</span></span>

### <span data-ttu-id="1a440-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1a440-119">System.String</span></span>

## <span data-ttu-id="1a440-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a440-120">OUTPUTS</span></span>

### <span data-ttu-id="1a440-121">Microsoft. Azure. Commands. CDN. Models. profile. PSProfile</span><span class="sxs-lookup"><span data-stu-id="1a440-121">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="1a440-122">Note</span><span class="sxs-lookup"><span data-stu-id="1a440-122">NOTES</span></span>

## <span data-ttu-id="1a440-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a440-123">RELATED LINKS</span></span>

[<span data-ttu-id="1a440-124">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1a440-124">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="1a440-125">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1a440-125">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="1a440-126">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="1a440-126">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


