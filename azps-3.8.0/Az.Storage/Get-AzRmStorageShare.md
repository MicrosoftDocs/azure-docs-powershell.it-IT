---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 2ef5ddb4a260f4749d6ccca6fa964f5e205c4b4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020260"
---
# <span data-ttu-id="a8800-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="a8800-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="a8800-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8800-102">SYNOPSIS</span></span>
<span data-ttu-id="a8800-103">Ottiene o elenca le condivisioni file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a8800-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="a8800-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8800-104">SYNTAX</span></span>

### <span data-ttu-id="a8800-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8800-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8800-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="a8800-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a8800-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="a8800-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a8800-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8800-108">DESCRIPTION</span></span>
<span data-ttu-id="a8800-109">Il cmdlet **Get-AzRmStorageShare** Ottiene o elenca le condivisioni file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a8800-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="a8800-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8800-110">EXAMPLES</span></span>

### <span data-ttu-id="a8800-111">Esempio 1: ottenere una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="a8800-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="a8800-112">Questo comando consente di ottenere una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="a8800-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="a8800-113">Esempio 2: elencare tutte le condivisioni file di archiviazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a8800-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="a8800-114">Questo comando elenca tutte le condivisioni file di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a8800-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="a8800-115">Esempio 3: ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8800-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="a8800-116">Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="a8800-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="a8800-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8800-117">PARAMETERS</span></span>

### <span data-ttu-id="a8800-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8800-118">-DefaultProfile</span></span>
<span data-ttu-id="a8800-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8800-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8800-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8800-120">-Name</span></span>
<span data-ttu-id="a8800-121">Nome condivisione</span><span class="sxs-lookup"><span data-stu-id="a8800-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8800-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8800-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8800-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a8800-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8800-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8800-124">-ResourceId</span></span>
<span data-ttu-id="a8800-125">Immettere un ID risorsa condivisione file.</span><span class="sxs-lookup"><span data-stu-id="a8800-125">Input a File Share Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8800-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8800-126">-StorageAccount</span></span>
<span data-ttu-id="a8800-127">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a8800-127">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8800-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8800-128">-StorageAccountName</span></span>
<span data-ttu-id="a8800-129">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a8800-129">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8800-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8800-130">CommonParameters</span></span>
<span data-ttu-id="a8800-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8800-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8800-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8800-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8800-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8800-133">INPUTS</span></span>

### <span data-ttu-id="a8800-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a8800-134">System.String</span></span>

### <span data-ttu-id="a8800-135">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a8800-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="a8800-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8800-136">OUTPUTS</span></span>

### <span data-ttu-id="a8800-137">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="a8800-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="a8800-138">Note</span><span class="sxs-lookup"><span data-stu-id="a8800-138">NOTES</span></span>

## <span data-ttu-id="a8800-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8800-139">RELATED LINKS</span></span>
