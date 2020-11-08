---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033085"
---
# <span data-ttu-id="4a72b-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="4a72b-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="4a72b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4a72b-102">SYNOPSIS</span></span>
<span data-ttu-id="4a72b-103">Ottenere le destinazioni di archiviazione della cache HPC.</span><span class="sxs-lookup"><span data-stu-id="4a72b-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="4a72b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4a72b-104">SYNTAX</span></span>

### <span data-ttu-id="4a72b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4a72b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a72b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a72b-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a72b-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a72b-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a72b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4a72b-108">DESCRIPTION</span></span>
<span data-ttu-id="4a72b-109">Il cmdlet **Get-AzHpcCacheStorageTarget** ottiene le destinazioni di archiviazione presenti nella cache.</span><span class="sxs-lookup"><span data-stu-id="4a72b-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="4a72b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4a72b-110">EXAMPLES</span></span>

### <span data-ttu-id="4a72b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4a72b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="4a72b-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4a72b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="4a72b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4a72b-113">PARAMETERS</span></span>

### <span data-ttu-id="4a72b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="4a72b-114">-CacheId</span></span>
<span data-ttu-id="4a72b-115">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="4a72b-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="4a72b-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="4a72b-116">-CacheName</span></span>
<span data-ttu-id="4a72b-117">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="4a72b-117">Name of cache.</span></span>

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

### <span data-ttu-id="4a72b-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="4a72b-118">-CacheObject</span></span>
<span data-ttu-id="4a72b-119">L'oggetto cache da avviare.</span><span class="sxs-lookup"><span data-stu-id="4a72b-119">The cache object to start.</span></span>

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

### <span data-ttu-id="4a72b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a72b-120">-DefaultProfile</span></span>
<span data-ttu-id="4a72b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4a72b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a72b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4a72b-122">-Name</span></span>
<span data-ttu-id="4a72b-123">Nome della destinazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4a72b-123">Name of storage target.</span></span>

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

### <span data-ttu-id="4a72b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a72b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4a72b-125">Nome della cache dei gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="4a72b-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="4a72b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a72b-126">CommonParameters</span></span>
<span data-ttu-id="4a72b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a72b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a72b-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a72b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a72b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4a72b-129">INPUTS</span></span>

### <span data-ttu-id="4a72b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4a72b-130">System.String</span></span>

## <span data-ttu-id="4a72b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4a72b-131">OUTPUTS</span></span>

### <span data-ttu-id="4a72b-132">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="4a72b-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="4a72b-133">Note</span><span class="sxs-lookup"><span data-stu-id="4a72b-133">NOTES</span></span>

## <span data-ttu-id="4a72b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4a72b-134">RELATED LINKS</span></span>
