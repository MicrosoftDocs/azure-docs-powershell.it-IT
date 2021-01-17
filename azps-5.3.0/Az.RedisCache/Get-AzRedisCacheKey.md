---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/get-azrediscachekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Get-AzRedisCacheKey.md
ms.openlocfilehash: 5588a3abecdec741aa6630083c38c01178669bae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378262"
---
# <span data-ttu-id="15891-101">Get-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="15891-101">Get-AzRedisCacheKey</span></span>

## <span data-ttu-id="15891-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15891-102">SYNOPSIS</span></span>
<span data-ttu-id="15891-103">Ottiene i tasti di scelta per una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="15891-103">Gets the access keys for a Redis Cache.</span></span>

## <span data-ttu-id="15891-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15891-104">SYNTAX</span></span>

```
Get-AzRedisCacheKey [-ResourceGroupName <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15891-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15891-105">DESCRIPTION</span></span>
<span data-ttu-id="15891-106">Il cmdlet **Get-AzRedisCacheKey** ottiene i tasti di scelta per una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="15891-106">The **Get-AzRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="15891-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15891-107">EXAMPLES</span></span>

### <span data-ttu-id="15891-108">Esempio 1: ottenere i tasti di scelta per una cache di redis</span><span class="sxs-lookup"><span data-stu-id="15891-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="15891-109">Questo comando consente di ottenere i tasti di scelta denominati MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="15891-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="15891-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15891-110">PARAMETERS</span></span>

### <span data-ttu-id="15891-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15891-111">-DefaultProfile</span></span>
<span data-ttu-id="15891-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15891-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15891-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="15891-113">-Name</span></span>
<span data-ttu-id="15891-114">Specifica il nome di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="15891-114">Specifies the name of a Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15891-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15891-115">-ResourceGroupName</span></span>
<span data-ttu-id="15891-116">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="15891-116">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="15891-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15891-117">CommonParameters</span></span>
<span data-ttu-id="15891-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15891-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15891-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15891-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15891-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15891-120">INPUTS</span></span>

### <span data-ttu-id="15891-121">System. String</span><span class="sxs-lookup"><span data-stu-id="15891-121">System.String</span></span>

## <span data-ttu-id="15891-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15891-122">OUTPUTS</span></span>

### <span data-ttu-id="15891-123">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="15891-123">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>

## <span data-ttu-id="15891-124">Note</span><span class="sxs-lookup"><span data-stu-id="15891-124">NOTES</span></span>

## <span data-ttu-id="15891-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15891-125">RELATED LINKS</span></span>

[<span data-ttu-id="15891-126">New-AzRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="15891-126">New-AzRedisCacheKey</span></span>](./New-AzRedisCacheKey.md)


