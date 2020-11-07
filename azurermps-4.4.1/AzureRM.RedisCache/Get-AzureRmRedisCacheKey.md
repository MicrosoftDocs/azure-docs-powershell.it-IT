---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: C0BEC701-8CE2-4B19-9F04-D32A42D9249E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Get-AzureRmRedisCacheKey.md
ms.openlocfilehash: e7e50488f69adb2b168453fd18264bf25a69942d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688250"
---
# <span data-ttu-id="e13a7-101">Get-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="e13a7-101">Get-AzureRmRedisCacheKey</span></span>

## <span data-ttu-id="e13a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e13a7-102">SYNOPSIS</span></span>
<span data-ttu-id="e13a7-103">Ottiene i tasti di scelta per una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="e13a7-103">Gets the access keys for a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e13a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e13a7-104">SYNTAX</span></span>

```
Get-AzureRmRedisCacheKey -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e13a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e13a7-105">DESCRIPTION</span></span>
<span data-ttu-id="e13a7-106">Il cmdlet **Get-AzureRmRedisCacheKey** ottiene i tasti di scelta per una cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="e13a7-106">The **Get-AzureRmRedisCacheKey** cmdlet gets the access keys for an Azure Redis Cache.</span></span>

## <span data-ttu-id="e13a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e13a7-107">EXAMPLES</span></span>

### <span data-ttu-id="e13a7-108">Esempio 1: ottenere i tasti di scelta per una cache di redis</span><span class="sxs-lookup"><span data-stu-id="e13a7-108">Example 1: Get the access keys for a Redis Cache</span></span>
```
PS C:\>Get-AzureRmRedisCacheKey -ResourceGroupName "MyResourceGroup" -Name "MyCacheKey"
PrimaryKey        : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
SecondaryKey      : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
```

<span data-ttu-id="e13a7-109">Questo comando consente di ottenere i tasti di scelta denominati MyCacheKey.</span><span class="sxs-lookup"><span data-stu-id="e13a7-109">This command gets the access keys named MyCacheKey.</span></span>

## <span data-ttu-id="e13a7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e13a7-110">PARAMETERS</span></span>

### <span data-ttu-id="e13a7-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="e13a7-111">-Name</span></span>
<span data-ttu-id="e13a7-112">Specifica il nome di una cache Redis.</span><span class="sxs-lookup"><span data-stu-id="e13a7-112">Specifies the name of a Redis Cache.</span></span>

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

### <span data-ttu-id="e13a7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e13a7-113">-ResourceGroupName</span></span>
<span data-ttu-id="e13a7-114">Specifica il nome del gruppo di risorse che contiene la cache Redis.</span><span class="sxs-lookup"><span data-stu-id="e13a7-114">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="e13a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e13a7-115">-DefaultProfile</span></span>
<span data-ttu-id="e13a7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e13a7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e13a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e13a7-117">CommonParameters</span></span>
<span data-ttu-id="e13a7-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e13a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e13a7-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e13a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e13a7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e13a7-120">INPUTS</span></span>

### <span data-ttu-id="e13a7-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e13a7-121">None</span></span>
<span data-ttu-id="e13a7-122">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="e13a7-122">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="e13a7-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e13a7-123">OUTPUTS</span></span>

### <span data-ttu-id="e13a7-124">Microsoft. Azure. Management. Redis. Models. RedisAccessKeys</span><span class="sxs-lookup"><span data-stu-id="e13a7-124">Microsoft.Azure.Management.Redis.Models.RedisAccessKeys</span></span>
<span data-ttu-id="e13a7-125">Questo cmdlet restituisce i tasti di scelta primari e secondari per una cache di Redis.</span><span class="sxs-lookup"><span data-stu-id="e13a7-125">This cmdlet returns primary and secondary access keys for a Redis Cache.</span></span>

## <span data-ttu-id="e13a7-126">Note</span><span class="sxs-lookup"><span data-stu-id="e13a7-126">NOTES</span></span>

## <span data-ttu-id="e13a7-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e13a7-127">RELATED LINKS</span></span>

[<span data-ttu-id="e13a7-128">New-AzureRmRedisCacheKey</span><span class="sxs-lookup"><span data-stu-id="e13a7-128">New-AzureRmRedisCacheKey</span></span>](./New-AzureRmRedisCacheKey.md)


