---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 28DECA86-37A5-48BE-9727-0C1A3B867E9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRMCdnProfile.md
ms.openlocfilehash: a345b69fdc6695706f61a85c2926392c9f522aeb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510084"
---
# <span data-ttu-id="30fd0-101">Get-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="30fd0-101">Get-AzureRmCdnProfile</span></span>

## <span data-ttu-id="30fd0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="30fd0-103">Ottiene un profilo CDN.</span><span class="sxs-lookup"><span data-stu-id="30fd0-103">Gets a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30fd0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30fd0-104">SYNTAX</span></span>

```
Get-AzureRmCdnProfile [-ProfileName <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30fd0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="30fd0-106">Il cmdlet **Get-AzureRMCdnProfile** ottiene un profilo CDN (Azure Content Delivery Network) e le relative informazioni correlate.</span><span class="sxs-lookup"><span data-stu-id="30fd0-106">The **Get-AzureRMCdnProfile** cmdlet gets an Azure Content Delivery Network (CDN) profile and its related information.</span></span>

## <span data-ttu-id="30fd0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30fd0-107">EXAMPLES</span></span>

## <span data-ttu-id="30fd0-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30fd0-108">PARAMETERS</span></span>

### <span data-ttu-id="30fd0-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30fd0-109">-DefaultProfile</span></span>
<span data-ttu-id="30fd0-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30fd0-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30fd0-111">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="30fd0-111">-ProfileName</span></span>
<span data-ttu-id="30fd0-112">Specifica il nome del profilo.</span><span class="sxs-lookup"><span data-stu-id="30fd0-112">Specifies the name of the profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30fd0-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30fd0-113">-ResourceGroupName</span></span>
<span data-ttu-id="30fd0-114">Specifica il nome del gruppo di risorse a cui appartiene il profilo.</span><span class="sxs-lookup"><span data-stu-id="30fd0-114">Specifies the name of the resource group to which the profile belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30fd0-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30fd0-115">CommonParameters</span></span>
<span data-ttu-id="30fd0-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30fd0-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30fd0-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30fd0-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30fd0-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30fd0-118">INPUTS</span></span>

### <span data-ttu-id="30fd0-119">Nessuno</span><span class="sxs-lookup"><span data-stu-id="30fd0-119">None</span></span>
<span data-ttu-id="30fd0-120">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="30fd0-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30fd0-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30fd0-121">OUTPUTS</span></span>

###  
<span data-ttu-id="30fd0-122">Questo cmdlet restituisce un oggetto profile.</span><span class="sxs-lookup"><span data-stu-id="30fd0-122">This cmdlet returns a profile object.</span></span>

## <span data-ttu-id="30fd0-123">Note</span><span class="sxs-lookup"><span data-stu-id="30fd0-123">NOTES</span></span>

## <span data-ttu-id="30fd0-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30fd0-124">RELATED LINKS</span></span>

[<span data-ttu-id="30fd0-125">New-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="30fd0-125">New-AzureRmCdnProfile</span></span>](./New-AzureRmCdnProfile.md)

[<span data-ttu-id="30fd0-126">Remove-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="30fd0-126">Remove-AzureRmCdnProfile</span></span>](./Remove-AzureRmCdnProfile.md)

[<span data-ttu-id="30fd0-127">Set-AzureRmCdnProfile</span><span class="sxs-lookup"><span data-stu-id="30fd0-127">Set-AzureRmCdnProfile</span></span>](./Set-AzureRmCdnProfile.md)


