---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageShare.md
ms.openlocfilehash: 9c5ff85ef608f623187d9132eea8af0f5da6a164
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190000"
---
# <span data-ttu-id="6344e-101">Update-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="6344e-101">Update-AzRmStorageShare</span></span>

## <span data-ttu-id="6344e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6344e-102">SYNOPSIS</span></span>
<span data-ttu-id="6344e-103">Modifica una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6344e-103">Modifies a Storage file share.</span></span>

## <span data-ttu-id="6344e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6344e-104">SYNTAX</span></span>

### <span data-ttu-id="6344e-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6344e-105">AccountName (Default)</span></span>
```
Update-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6344e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6344e-106">AccountObject</span></span>
```
Update-AzRmStorageShare -Name <String> -StorageAccount <PSStorageAccount> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6344e-107">ShareResourceId</span><span class="sxs-lookup"><span data-stu-id="6344e-107">ShareResourceId</span></span>
```
Update-AzRmStorageShare [-ResourceId] <String> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6344e-108">ShareObject</span><span class="sxs-lookup"><span data-stu-id="6344e-108">ShareObject</span></span>
```
Update-AzRmStorageShare -InputObject <PSShare> [-QuotaGiB <Int32>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6344e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6344e-109">DESCRIPTION</span></span>
<span data-ttu-id="6344e-110">Il cmdlet **New-AzRmStorageShare** modifica una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6344e-110">The **New-AzRmStorageShare** cmdlet modifies a Storage file share.</span></span>

## <span data-ttu-id="6344e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6344e-111">EXAMPLES</span></span>

### <span data-ttu-id="6344e-112">Esempio 1: modifica i metadati di una condivisione file di archiviazione e condividere la quota con il nome dell'account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="6344e-112">Example 1: Modifies a Storage file share's metadata and share quota with Storage account name and share name</span></span>
```
PS C:\>$share = Update-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" -Name "myshare" -QuotaGiB 200 -Metadata @{tag0="value0";tag1="value1"}

PS C:\>$share

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
myshare  200

PS C:\>$share.Metadata

Key  Value  
---  ----- 
tag0 value0
tag1 value1
```

<span data-ttu-id="6344e-113">Questo comando modifica i metadati di una condivisione file di archiviazione e condivide la quota con il nome dell'account di archiviazione e il nome della condivisione e Mostra il risultato di modifica con l'oggetto condivisione file restituito.</span><span class="sxs-lookup"><span data-stu-id="6344e-113">This command modifies a Storage file share's metadata and share quota with Storage account name and share name, and show the modify result with the returned file share object.</span></span>

### <span data-ttu-id="6344e-114">Esempio 2: modifica dei metadati in una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione</span><span class="sxs-lookup"><span data-stu-id="6344e-114">Example 2: Modifies metadata on a Storage file share with Storage account object and share name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount"
PS C:\>$share = Update-AzRmStorageShare -StorageAccount $accountObject -Name "myshare" -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="6344e-115">Questo comando consente di modificare i metadati in una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="6344e-115">This command modifies metadata on a Storage file share with Storage account object and share name.</span></span>

### <span data-ttu-id="6344e-116">Esempio 3: modifica la quota di condivisione per tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="6344e-116">Example 3: Modifies share quota for all Storage file shares in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzRmStorageShare -ResourceGroupName "myresourcegroup" -StorageAccountName "mystorageaccount" | Update-AzRmStorageShare -QuotaGiB 5000

   ResourceGroupName: myresourcegroup, StorageAccountName: mystorageaccount

Name     QuotaGiB EnabledProtocol AccessTier Deleted Version ShareUsageBytes
----     -------- --------------- ---------- ------- ------- ---------------
share1   5000
share2   5000
```

<span data-ttu-id="6344e-117">Questo comando modifica la quota di condivisione come 5000 GiB per tutte le condivisioni file di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="6344e-117">This command modifies share quota as 5000 GiB for all Storage file shares in a Storage account with pipeline.</span></span>

## <span data-ttu-id="6344e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6344e-118">PARAMETERS</span></span>

### <span data-ttu-id="6344e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6344e-119">-DefaultProfile</span></span>
<span data-ttu-id="6344e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6344e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6344e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6344e-121">-InputObject</span></span>
<span data-ttu-id="6344e-122">Oggetto condivisione archiviazione</span><span class="sxs-lookup"><span data-stu-id="6344e-122">Storage Share object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSShare
Parameter Sets: ShareObject
Aliases: Share

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6344e-123">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6344e-123">-Metadata</span></span>
<span data-ttu-id="6344e-124">Condividere metadati</span><span class="sxs-lookup"><span data-stu-id="6344e-124">Share Metadata</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6344e-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="6344e-125">-Name</span></span>
<span data-ttu-id="6344e-126">Nome condivisione</span><span class="sxs-lookup"><span data-stu-id="6344e-126">Share Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6344e-127">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="6344e-127">-QuotaGiB</span></span>
<span data-ttu-id="6344e-128">Condividere la quota in gibibyte.</span><span class="sxs-lookup"><span data-stu-id="6344e-128">Share Quota in Gibibyte.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Quota

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6344e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6344e-129">-ResourceGroupName</span></span>
<span data-ttu-id="6344e-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6344e-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="6344e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6344e-131">-ResourceId</span></span>
<span data-ttu-id="6344e-132">Immettere un ID risorsa condivisione file.</span><span class="sxs-lookup"><span data-stu-id="6344e-132">Input a File Share Resource Id.</span></span>

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

### <span data-ttu-id="6344e-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6344e-133">-StorageAccount</span></span>
<span data-ttu-id="6344e-134">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6344e-134">Storage account object</span></span>

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

### <span data-ttu-id="6344e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6344e-135">-StorageAccountName</span></span>
<span data-ttu-id="6344e-136">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6344e-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="6344e-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6344e-137">-Confirm</span></span>
<span data-ttu-id="6344e-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6344e-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6344e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6344e-139">-WhatIf</span></span>
<span data-ttu-id="6344e-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6344e-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6344e-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6344e-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6344e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6344e-142">CommonParameters</span></span>
<span data-ttu-id="6344e-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6344e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6344e-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6344e-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6344e-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6344e-145">INPUTS</span></span>

### <span data-ttu-id="6344e-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6344e-146">System.String</span></span>

### <span data-ttu-id="6344e-147">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6344e-147">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="6344e-148">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="6344e-148">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="6344e-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6344e-149">OUTPUTS</span></span>

### <span data-ttu-id="6344e-150">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="6344e-150">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="6344e-151">Note</span><span class="sxs-lookup"><span data-stu-id="6344e-151">NOTES</span></span>

## <span data-ttu-id="6344e-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6344e-152">RELATED LINKS</span></span>
