---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328227"
---
# <span data-ttu-id="273a7-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="273a7-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="273a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="273a7-102">SYNOPSIS</span></span>
<span data-ttu-id="273a7-103">Ottenere le destinazioni di archiviazione della cache HPC.</span><span class="sxs-lookup"><span data-stu-id="273a7-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="273a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="273a7-104">SYNTAX</span></span>

### <span data-ttu-id="273a7-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="273a7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="273a7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="273a7-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="273a7-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="273a7-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="273a7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="273a7-108">DESCRIPTION</span></span>
<span data-ttu-id="273a7-109">Il cmdlet **Get-AzHpcCacheStorageTarget** ottiene le destinazioni di archiviazione presenti nella cache.</span><span class="sxs-lookup"><span data-stu-id="273a7-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="273a7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="273a7-110">EXAMPLES</span></span>

### <span data-ttu-id="273a7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="273a7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="273a7-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="273a7-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="273a7-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="273a7-113">PARAMETERS</span></span>

### <span data-ttu-id="273a7-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="273a7-114">-CacheId</span></span>
<span data-ttu-id="273a7-115">ID risorsa della cache</span><span class="sxs-lookup"><span data-stu-id="273a7-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="273a7-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="273a7-116">-CacheName</span></span>
<span data-ttu-id="273a7-117">Nome della cache.</span><span class="sxs-lookup"><span data-stu-id="273a7-117">Name of cache.</span></span>

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

### <span data-ttu-id="273a7-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="273a7-118">-CacheObject</span></span>
<span data-ttu-id="273a7-119">L'oggetto cache da avviare.</span><span class="sxs-lookup"><span data-stu-id="273a7-119">The cache object to start.</span></span>

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

### <span data-ttu-id="273a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273a7-120">-DefaultProfile</span></span>
<span data-ttu-id="273a7-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="273a7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="273a7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="273a7-122">-Name</span></span>
<span data-ttu-id="273a7-123">Nome della destinazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="273a7-123">Name of storage target.</span></span>

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

### <span data-ttu-id="273a7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="273a7-124">-ResourceGroupName</span></span>
<span data-ttu-id="273a7-125">Nome della cache dei gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="273a7-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="273a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273a7-126">CommonParameters</span></span>
<span data-ttu-id="273a7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="273a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273a7-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="273a7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273a7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="273a7-129">INPUTS</span></span>

### <span data-ttu-id="273a7-130">System. String</span><span class="sxs-lookup"><span data-stu-id="273a7-130">System.String</span></span>

## <span data-ttu-id="273a7-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="273a7-131">OUTPUTS</span></span>

### <span data-ttu-id="273a7-132">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="273a7-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="273a7-133">Note</span><span class="sxs-lookup"><span data-stu-id="273a7-133">NOTES</span></span>

## <span data-ttu-id="273a7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="273a7-134">RELATED LINKS</span></span>
