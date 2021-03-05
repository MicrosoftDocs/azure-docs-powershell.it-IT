---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageShare.md
ms.openlocfilehash: 44ad4fadb86b84b5eacb82a15bf92b7b1d831b70
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002829"
---
# <span data-ttu-id="3fa3b-101">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="3fa3b-101">Get-AzRmStorageShare</span></span>

## <span data-ttu-id="3fa3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fa3b-102">SYNOPSIS</span></span>
<span data-ttu-id="3fa3b-103">Ottiene o elenca le condivisioni file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-103">Gets or lists Storage file shares.</span></span>

## <span data-ttu-id="3fa3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fa3b-104">SYNTAX</span></span>

### <span data-ttu-id="3fa3b-105">AccountNameSingle (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fa3b-105">AccountNameSingle (Default)</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-GetShareUsage] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fa3b-106">AccountName</span><span class="sxs-lookup"><span data-stu-id="3fa3b-106">AccountName</span></span>
```
Get-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fa3b-107">AccountObjectSingle</span><span class="sxs-lookup"><span data-stu-id="3fa3b-107">AccountObjectSingle</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fa3b-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="3fa3b-108">AccountObject</span></span>
```
Get-AzRmStorageShare -StorageAccount <PSStorageAccount> [-IncludeDeleted]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fa3b-109">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa3b-109">ShareResourceId</span></span>
```
Get-AzRmStorageShare [-ResourceId] <String> [-Name <String>] [-GetShareUsage]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fa3b-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3fa3b-110">DESCRIPTION</span></span>
<span data-ttu-id="3fa3b-111">Il **cmdlet Get-AzRmStorageShare** ottiene o elenca le condivisioni file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-111">The **Get-AzRmStorageShare** cmdlet gets or lists Storage file shares.</span></span>

## <span data-ttu-id="3fa3b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fa3b-112">EXAMPLES</span></span>

### <span data-ttu-id="3fa3b-113">Esempio 1: Ottenere una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="3fa3b-113">Example 1: Get a Storage file share with Storage account name and share name</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="3fa3b-114">Questo comando ottiene una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-114">This command gets a Storage file share with Storage account name and share name.</span></span>

### <span data-ttu-id="3fa3b-115">Esempio 2: Elencare tutte le condivisioni file di archiviazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3fa3b-115">Example 2: List all Storage file shares of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version ShareUsageBytes
----     -------- --------------- ----------           ------- ------- ---------------
share1   5120                     TransactionOptimized
share2   5120                     TransactionOptimized
```

<span data-ttu-id="3fa3b-116">Questo comando elenca tutte le condivisioni file di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-116">This command lists all Storage file shares of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="3fa3b-117">Esempio 3: Ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-117">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Get-AzRmStorageShare -Name "myshare"

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120
```

<span data-ttu-id="3fa3b-118">Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-118">This command gets a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="3fa3b-119">Esempio 4: Ottenere una condivisione file di archiviazione con l'utilizzo della condivisione in byte</span><span class="sxs-lookup"><span data-stu-id="3fa3b-119">Example 4: Get a Storage file share with the share usage in bytes</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -GetShareUsage

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  5120                                                2097152
```

<span data-ttu-id="3fa3b-120">Questo comando ottiene una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione e include l'utilizzo della condivisione in byte.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-120">This command gets a Storage file share with Storage account name and share name, and include the share usage in bytes.</span></span>

### <span data-ttu-id="3fa3b-121">Esempio 5: Elencare tutte le condivisioni file di archiviazione di un account di archiviazione e includere le condivisioni eliminate</span><span class="sxs-lookup"><span data-stu-id="3fa3b-121">Example 5: List all Storage file shares of a Storage account, include the deleted shares</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -IncludeDeleted 

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier           Deleted Version          ShareUsageBytes
----     -------- --------------- ----------           ------- -------          ---------------
test     100                      TransactionOptimized                                         
share1   100                      TransactionOptimized True    01D61FD1FC5498B6
```

<span data-ttu-id="3fa3b-122">Questo comando elenca tutte le condivisioni file di archiviazione e include le condivisioni eliminate di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-122">This command lists all Storage file shares include the deleted shares of a Storage account with Storage account name.</span></span>

## <span data-ttu-id="3fa3b-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fa3b-123">PARAMETERS</span></span>

### <span data-ttu-id="3fa3b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fa3b-124">-DefaultProfile</span></span>
<span data-ttu-id="3fa3b-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fa3b-126">-GetShareUsage</span><span class="sxs-lookup"><span data-stu-id="3fa3b-126">-GetShareUsage</span></span>
<span data-ttu-id="3fa3b-127">Specificare questo parametro per ottenere l'utilizzo della condivisione in byte.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-127">Specify this parameter to get the Share Usage in Bytes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountNameSingle, AccountObjectSingle, ShareResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3b-128">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="3fa3b-128">-IncludeDeleted</span></span>
<span data-ttu-id="3fa3b-129">Includi condivisioni eliminate, per impostazione predefinita le condivisioni elenco non includono le condivisioni eliminate</span><span class="sxs-lookup"><span data-stu-id="3fa3b-129">Include deleted shares, by default list shares won't include deleted shares</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AccountName, AccountObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="3fa3b-130">-Name</span></span>
<span data-ttu-id="3fa3b-131">Condividi nome</span><span class="sxs-lookup"><span data-stu-id="3fa3b-131">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, ShareResourceId
Aliases: N, ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountObjectSingle
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fa3b-132">-ResourceGroupName</span></span>
<span data-ttu-id="3fa3b-133">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fa3b-134">-ResourceId</span></span>
<span data-ttu-id="3fa3b-135">Immettere un ID di risorsa condivisione file.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-135">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="3fa3b-136">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fa3b-136">-StorageAccount</span></span>
<span data-ttu-id="3fa3b-137">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3fa3b-137">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectSingle, AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3b-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3fa3b-138">-StorageAccountName</span></span>
<span data-ttu-id="3fa3b-139">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-139">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameSingle, AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fa3b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fa3b-140">CommonParameters</span></span>
<span data-ttu-id="3fa3b-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fa3b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fa3b-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fa3b-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fa3b-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="3fa3b-143">INPUTS</span></span>

### <span data-ttu-id="3fa3b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3fa3b-144">System.String</span></span>

### <span data-ttu-id="3fa3b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3fa3b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3fa3b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fa3b-146">OUTPUTS</span></span>

### <span data-ttu-id="3fa3b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span><span class="sxs-lookup"><span data-stu-id="3fa3b-147">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="3fa3b-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="3fa3b-148">NOTES</span></span>

## <span data-ttu-id="3fa3b-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fa3b-149">RELATED LINKS</span></span>
