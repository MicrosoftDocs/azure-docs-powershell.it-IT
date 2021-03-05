---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c1e68d77df44688961f867d473a9dfce1205c2dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002862"
---
# <span data-ttu-id="1dbba-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1dbba-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="1dbba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dbba-102">SYNOPSIS</span></span>
<span data-ttu-id="1dbba-103">Ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1dbba-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="1dbba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dbba-104">SYNTAX</span></span>

### <span data-ttu-id="1dbba-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1dbba-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbba-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1dbba-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1dbba-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="1dbba-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dbba-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1dbba-108">DESCRIPTION</span></span>
<span data-ttu-id="1dbba-109">Il cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1dbba-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="1dbba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dbba-110">EXAMPLES</span></span>

### <span data-ttu-id="1dbba-111">Esempio 1: Ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="1dbba-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="1dbba-112">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1dbba-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1dbba-113">Esempio 2: Ottenere ImmutabilityPolicy di un contenitore BLOB Di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="1dbba-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="1dbba-114">Questo comando ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1dbba-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="1dbba-115">Esempio 3: Ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con un oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1dbba-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="1dbba-116">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB Di archiviazione con un oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1dbba-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="1dbba-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1dbba-117">PARAMETERS</span></span>

### <span data-ttu-id="1dbba-118">-Container</span><span class="sxs-lookup"><span data-stu-id="1dbba-118">-Container</span></span>
<span data-ttu-id="1dbba-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1dbba-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbba-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="1dbba-120">-ContainerName</span></span>
<span data-ttu-id="1dbba-121">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="1dbba-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbba-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dbba-122">-DefaultProfile</span></span>
<span data-ttu-id="1dbba-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dbba-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dbba-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="1dbba-124">-Etag</span></span>
<span data-ttu-id="1dbba-125">Etag dei criteri di non modificabilità.</span><span class="sxs-lookup"><span data-stu-id="1dbba-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dbba-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dbba-126">-ResourceGroupName</span></span>
<span data-ttu-id="1dbba-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dbba-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbba-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1dbba-128">-StorageAccount</span></span>
<span data-ttu-id="1dbba-129">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1dbba-129">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbba-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1dbba-130">-StorageAccountName</span></span>
<span data-ttu-id="1dbba-131">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1dbba-131">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dbba-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dbba-132">CommonParameters</span></span>
<span data-ttu-id="1dbba-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dbba-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dbba-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dbba-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dbba-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="1dbba-135">INPUTS</span></span>

### <span data-ttu-id="1dbba-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1dbba-136">System.String</span></span>

### <span data-ttu-id="1dbba-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1dbba-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1dbba-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="1dbba-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="1dbba-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dbba-139">OUTPUTS</span></span>

### <span data-ttu-id="1dbba-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="1dbba-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="1dbba-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="1dbba-141">NOTES</span></span>

## <span data-ttu-id="1dbba-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dbba-142">RELATED LINKS</span></span>
