---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178254"
---
# <span data-ttu-id="83d04-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="83d04-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="83d04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83d04-102">SYNOPSIS</span></span>
<span data-ttu-id="83d04-103">Ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="83d04-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="83d04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83d04-104">SYNTAX</span></span>

### <span data-ttu-id="83d04-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83d04-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83d04-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="83d04-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83d04-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="83d04-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83d04-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="83d04-108">DESCRIPTION</span></span>
<span data-ttu-id="83d04-109">Il cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="83d04-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="83d04-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83d04-110">EXAMPLES</span></span>

### <span data-ttu-id="83d04-111">Esempio 1: Ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="83d04-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="83d04-112">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="83d04-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="83d04-113">Esempio 2: Ottenere ImmutabilityPolicy di un contenitore BLOB Di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="83d04-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="83d04-114">Questo comando ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="83d04-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="83d04-115">Esempio 3: Ottenere ImmutabilityPolicy di un contenitore BLOB Storage con oggetto contenitore Storage</span><span class="sxs-lookup"><span data-stu-id="83d04-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="83d04-116">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB Di archiviazione con un oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83d04-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="83d04-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83d04-117">PARAMETERS</span></span>

### <span data-ttu-id="83d04-118">-Container</span><span class="sxs-lookup"><span data-stu-id="83d04-118">-Container</span></span>
<span data-ttu-id="83d04-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="83d04-119">Storage container object</span></span>

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

### <span data-ttu-id="83d04-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="83d04-120">-ContainerName</span></span>
<span data-ttu-id="83d04-121">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="83d04-121">Container Name</span></span>

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

### <span data-ttu-id="83d04-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83d04-122">-DefaultProfile</span></span>
<span data-ttu-id="83d04-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83d04-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83d04-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="83d04-124">-Etag</span></span>
<span data-ttu-id="83d04-125">Etag dei criteri di non modificabilità.</span><span class="sxs-lookup"><span data-stu-id="83d04-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="83d04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83d04-126">-ResourceGroupName</span></span>
<span data-ttu-id="83d04-127">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="83d04-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="83d04-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="83d04-128">-StorageAccount</span></span>
<span data-ttu-id="83d04-129">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="83d04-129">Storage account object</span></span>

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

### <span data-ttu-id="83d04-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="83d04-130">-StorageAccountName</span></span>
<span data-ttu-id="83d04-131">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="83d04-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="83d04-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83d04-132">CommonParameters</span></span>
<span data-ttu-id="83d04-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83d04-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83d04-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83d04-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83d04-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="83d04-135">INPUTS</span></span>

### <span data-ttu-id="83d04-136">System.String</span><span class="sxs-lookup"><span data-stu-id="83d04-136">System.String</span></span>

### <span data-ttu-id="83d04-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="83d04-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="83d04-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="83d04-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="83d04-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83d04-139">OUTPUTS</span></span>

### <span data-ttu-id="83d04-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="83d04-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="83d04-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="83d04-141">NOTES</span></span>

## <span data-ttu-id="83d04-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83d04-142">RELATED LINKS</span></span>
