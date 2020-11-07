---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: f54196ef5b055a5e1968c682d21f861ee41c77ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857850"
---
# <span data-ttu-id="24b17-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="24b17-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="24b17-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="24b17-102">SYNOPSIS</span></span>
<span data-ttu-id="24b17-103">Ottiene o elenca le condivisioni file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24b17-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="24b17-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="24b17-104">SYNTAX</span></span>

### <span data-ttu-id="24b17-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="24b17-105">AccountName (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24b17-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="24b17-106">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24b17-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="24b17-107">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24b17-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="24b17-108">DESCRIPTION</span></span>
<span data-ttu-id="24b17-109">Il cmdlet **Get-AzRmStorageShare** Ottiene o elenca le condivisioni file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24b17-109">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="24b17-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="24b17-110">EXAMPLES</span></span>

### <span data-ttu-id="24b17-111">Esempio 1: ottenere una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="24b17-111">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="24b17-112">Questo comando consente di ottenere una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="24b17-112">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="24b17-113">Esempio 2: elencare tutte le condivisioni file di archiviazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="24b17-113">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
share1   myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
share2   myStorageAccount   myResourceGroup   "0x8D6FF862774FE57" 5120     2019-07-03 07:14:57Z
```

<span data-ttu-id="24b17-114">Questo comando elenca tutte le condivisioni file di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24b17-114">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="24b17-115">Esempio 3: ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="24b17-115">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | Get-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup   "0x8D71F03028DDDC9" 5120     2019-08-12 08:56:48Z
```

<span data-ttu-id="24b17-116">Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="24b17-116">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="24b17-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="24b17-117">PARAMETERS</span></span>

### <span data-ttu-id="24b17-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b17-118">-DefaultProfile</span></span>
<span data-ttu-id="24b17-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="24b17-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b17-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="24b17-120">-Name</span></span>
<span data-ttu-id="24b17-121">Nome condivisione</span><span class="sxs-lookup"><span data-stu-id="24b17-121">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24b17-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b17-122">-ResourceGroupName</span></span>
<span data-ttu-id="24b17-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="24b17-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="24b17-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24b17-124">-ResourceId</span></span>
<span data-ttu-id="24b17-125">Immettere un ID risorsa condivisione file.</span><span class="sxs-lookup"><span data-stu-id="24b17-125">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="24b17-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="24b17-126">-StorageAccount</span></span>
<span data-ttu-id="24b17-127">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="24b17-127">Storage account object</span></span>

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

### <span data-ttu-id="24b17-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24b17-128">-StorageAccountName</span></span>
<span data-ttu-id="24b17-129">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="24b17-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="24b17-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b17-130">CommonParameters</span></span>
<span data-ttu-id="24b17-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24b17-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b17-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b17-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b17-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="24b17-133">INPUTS</span></span>

### <span data-ttu-id="24b17-134">System. String</span><span class="sxs-lookup"><span data-stu-id="24b17-134">System.String</span></span>

### <span data-ttu-id="24b17-135">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="24b17-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="24b17-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="24b17-136">OUTPUTS</span></span>

### <span data-ttu-id="24b17-137">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="24b17-137">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="24b17-138">Note</span><span class="sxs-lookup"><span data-stu-id="24b17-138">NOTES</span></span>

## <span data-ttu-id="24b17-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="24b17-139">RELATED LINKS</span></span>
