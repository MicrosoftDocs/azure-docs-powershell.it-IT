---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376277"
---
# <span data-ttu-id="2de15-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2de15-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="2de15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2de15-102">SYNOPSIS</span></span>
<span data-ttu-id="2de15-103">Ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2de15-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="2de15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2de15-104">SYNTAX</span></span>

### <span data-ttu-id="2de15-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2de15-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2de15-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2de15-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2de15-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="2de15-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2de15-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2de15-108">DESCRIPTION</span></span>
<span data-ttu-id="2de15-109">Il cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2de15-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="2de15-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2de15-110">EXAMPLES</span></span>

### <span data-ttu-id="2de15-111">Esempio 1: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="2de15-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="2de15-112">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="2de15-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="2de15-113">Esempio 2: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="2de15-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="2de15-114">Questo comando ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="2de15-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="2de15-115">Esempio 3: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2de15-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="2de15-116">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2de15-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="2de15-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2de15-117">PARAMETERS</span></span>

### <span data-ttu-id="2de15-118">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="2de15-118">-Container</span></span>
<span data-ttu-id="2de15-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2de15-119">Storage container object</span></span>

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

### <span data-ttu-id="2de15-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="2de15-120">-ContainerName</span></span>
<span data-ttu-id="2de15-121">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="2de15-121">Container Name</span></span>

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

### <span data-ttu-id="2de15-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2de15-122">-DefaultProfile</span></span>
<span data-ttu-id="2de15-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2de15-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2de15-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="2de15-124">-Etag</span></span>
<span data-ttu-id="2de15-125">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="2de15-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="2de15-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2de15-126">-ResourceGroupName</span></span>
<span data-ttu-id="2de15-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2de15-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="2de15-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2de15-128">-StorageAccount</span></span>
<span data-ttu-id="2de15-129">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2de15-129">Storage account object</span></span>

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

### <span data-ttu-id="2de15-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2de15-130">-StorageAccountName</span></span>
<span data-ttu-id="2de15-131">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2de15-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="2de15-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2de15-132">CommonParameters</span></span>
<span data-ttu-id="2de15-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2de15-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2de15-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2de15-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2de15-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2de15-135">INPUTS</span></span>

### <span data-ttu-id="2de15-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2de15-136">System.String</span></span>

### <span data-ttu-id="2de15-137">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2de15-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2de15-138">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="2de15-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="2de15-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2de15-139">OUTPUTS</span></span>

### <span data-ttu-id="2de15-140">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="2de15-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="2de15-141">Note</span><span class="sxs-lookup"><span data-stu-id="2de15-141">NOTES</span></span>

## <span data-ttu-id="2de15-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2de15-142">RELATED LINKS</span></span>
