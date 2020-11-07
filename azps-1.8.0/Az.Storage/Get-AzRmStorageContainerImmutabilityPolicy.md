---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2b324d1b038a6ab97e4e68303bd98570fe0704ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676645"
---
# <span data-ttu-id="d6dd8-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d6dd8-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="d6dd8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6dd8-103">Ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d6dd8-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d6dd8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6dd8-104">SYNTAX</span></span>

### <span data-ttu-id="d6dd8-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d6dd8-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6dd8-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d6dd8-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6dd8-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="d6dd8-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6dd8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6dd8-108">DESCRIPTION</span></span>
<span data-ttu-id="d6dd8-109">Il cmdlet **Get-AzRmStorageContainerImmutabilityPolicy** ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d6dd8-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="d6dd8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6dd8-110">EXAMPLES</span></span>

### <span data-ttu-id="d6dd8-111">Esempio 1: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="d6dd8-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="d6dd8-112">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d6dd8-113">Esempio 2: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="d6dd8-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="d6dd8-114">Questo comando ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="d6dd8-115">Esempio 3: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d6dd8-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="d6dd8-116">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="d6dd8-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6dd8-117">PARAMETERS</span></span>

### <span data-ttu-id="d6dd8-118">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="d6dd8-118">-Container</span></span>
<span data-ttu-id="d6dd8-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d6dd8-119">Storage container object</span></span>

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

### <span data-ttu-id="d6dd8-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="d6dd8-120">-ContainerName</span></span>
<span data-ttu-id="d6dd8-121">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="d6dd8-121">Container Name</span></span>

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

### <span data-ttu-id="d6dd8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6dd8-122">-DefaultProfile</span></span>
<span data-ttu-id="d6dd8-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d6dd8-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="d6dd8-124">-Etag</span></span>
<span data-ttu-id="d6dd8-125">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-125">Immutability policy etag.</span></span>

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

### <span data-ttu-id="d6dd8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6dd8-126">-ResourceGroupName</span></span>
<span data-ttu-id="d6dd8-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="d6dd8-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6dd8-128">-StorageAccount</span></span>
<span data-ttu-id="d6dd8-129">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d6dd8-129">Storage account object</span></span>

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

### <span data-ttu-id="d6dd8-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d6dd8-130">-StorageAccountName</span></span>
<span data-ttu-id="d6dd8-131">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="d6dd8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6dd8-132">CommonParameters</span></span>
<span data-ttu-id="d6dd8-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6dd8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6dd8-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6dd8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6dd8-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6dd8-135">INPUTS</span></span>

### <span data-ttu-id="d6dd8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d6dd8-136">System.String</span></span>

### <span data-ttu-id="d6dd8-137">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d6dd8-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d6dd8-138">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d6dd8-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d6dd8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6dd8-139">OUTPUTS</span></span>

### <span data-ttu-id="d6dd8-140">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="d6dd8-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="d6dd8-141">Note</span><span class="sxs-lookup"><span data-stu-id="d6dd8-141">NOTES</span></span>

## <span data-ttu-id="d6dd8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6dd8-142">RELATED LINKS</span></span>
