---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 6fb1e00f74bcd170d8117e4e37655da6c275a62f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988229"
---
# <span data-ttu-id="3f79b-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3f79b-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="3f79b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f79b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f79b-103">Ottenere i target di archiviazione cache HPC.</span><span class="sxs-lookup"><span data-stu-id="3f79b-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="3f79b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f79b-104">SYNTAX</span></span>

### <span data-ttu-id="3f79b-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f79b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f79b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f79b-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f79b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f79b-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3f79b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3f79b-108">DESCRIPTION</span></span>
<span data-ttu-id="3f79b-109">Il cmdlet **Get-AzHpcCacheStorageTarget ottiene** le destinazione di archiviazione presenti nella cache.</span><span class="sxs-lookup"><span data-stu-id="3f79b-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="3f79b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f79b-110">EXAMPLES</span></span>

### <span data-ttu-id="3f79b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3f79b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="3f79b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3f79b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="3f79b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f79b-113">PARAMETERS</span></span>

### <span data-ttu-id="3f79b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="3f79b-114">-CacheId</span></span>
<span data-ttu-id="3f79b-115">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="3f79b-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f79b-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="3f79b-116">-CacheName</span></span>
<span data-ttu-id="3f79b-117">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="3f79b-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f79b-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="3f79b-118">-CacheObject</span></span>
<span data-ttu-id="3f79b-119">Oggetto cache da avviare.</span><span class="sxs-lookup"><span data-stu-id="3f79b-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f79b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f79b-120">-DefaultProfile</span></span>
<span data-ttu-id="3f79b-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f79b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f79b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3f79b-122">-Name</span></span>
<span data-ttu-id="3f79b-123">Nome della destinazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3f79b-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f79b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f79b-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f79b-125">Il nome della cache dei gruppi di risorse è in.</span><span class="sxs-lookup"><span data-stu-id="3f79b-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f79b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f79b-126">CommonParameters</span></span>
<span data-ttu-id="3f79b-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f79b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f79b-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3f79b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f79b-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="3f79b-129">INPUTS</span></span>

### <span data-ttu-id="3f79b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="3f79b-130">System.String</span></span>

## <span data-ttu-id="3f79b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f79b-131">OUTPUTS</span></span>

### <span data-ttu-id="3f79b-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="3f79b-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="3f79b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="3f79b-133">NOTES</span></span>

## <span data-ttu-id="3f79b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f79b-134">RELATED LINKS</span></span>
