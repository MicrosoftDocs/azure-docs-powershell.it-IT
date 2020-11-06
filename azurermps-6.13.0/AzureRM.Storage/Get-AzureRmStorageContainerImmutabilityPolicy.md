---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520571"
---
# <span data-ttu-id="a15bb-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a15bb-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="a15bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a15bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a15bb-103">Ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a15bb-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a15bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a15bb-104">SYNTAX</span></span>

### <span data-ttu-id="a15bb-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a15bb-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a15bb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a15bb-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a15bb-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="a15bb-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a15bb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a15bb-108">DESCRIPTION</span></span>
<span data-ttu-id="a15bb-109">Il cmdlet **Get-AzureRmStorageContainerImmutabilityPolicy** ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a15bb-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="a15bb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a15bb-110">EXAMPLES</span></span>

### <span data-ttu-id="a15bb-111">Esempio 1: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="a15bb-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="a15bb-112">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a15bb-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="a15bb-113">Esempio 2: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="a15bb-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="a15bb-114">Questo comando ottiene ImmutabilityPolicy di contenitori BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a15bb-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="a15bb-115">Esempio 3: ottenere ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a15bb-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="a15bb-116">Questo comando ottiene ImmutabilityPolicy di un contenitore BLOB di archiviazione con l'oggetto contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a15bb-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="a15bb-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a15bb-117">PARAMETERS</span></span>

### <span data-ttu-id="a15bb-118">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="a15bb-118">-Container</span></span>
<span data-ttu-id="a15bb-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a15bb-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a15bb-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a15bb-120">-ContainerName</span></span>
<span data-ttu-id="a15bb-121">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="a15bb-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a15bb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a15bb-122">-DefaultProfile</span></span>
<span data-ttu-id="a15bb-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a15bb-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a15bb-124">-ETag</span><span class="sxs-lookup"><span data-stu-id="a15bb-124">-Etag</span></span>
<span data-ttu-id="a15bb-125">Criteri di immutabilità ETag.</span><span class="sxs-lookup"><span data-stu-id="a15bb-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a15bb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a15bb-126">-ResourceGroupName</span></span>
<span data-ttu-id="a15bb-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a15bb-127">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a15bb-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a15bb-128">-StorageAccount</span></span>
<span data-ttu-id="a15bb-129">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a15bb-129">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a15bb-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a15bb-130">-StorageAccountName</span></span>
<span data-ttu-id="a15bb-131">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a15bb-131">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a15bb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a15bb-132">CommonParameters</span></span>
<span data-ttu-id="a15bb-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a15bb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a15bb-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a15bb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a15bb-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a15bb-135">INPUTS</span></span>

### <span data-ttu-id="a15bb-136">System. String</span><span class="sxs-lookup"><span data-stu-id="a15bb-136">System.String</span></span>

## <span data-ttu-id="a15bb-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a15bb-137">OUTPUTS</span></span>

### <span data-ttu-id="a15bb-138">Microsoft. Azure. Commands. Management. storage. Models. PSImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="a15bb-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="a15bb-139">Note</span><span class="sxs-lookup"><span data-stu-id="a15bb-139">NOTES</span></span>

## <span data-ttu-id="a15bb-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a15bb-140">RELATED LINKS</span></span>

