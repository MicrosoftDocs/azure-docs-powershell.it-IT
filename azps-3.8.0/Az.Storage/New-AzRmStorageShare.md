---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageShare.md
ms.openlocfilehash: 040e4e8584c29f77e6b847eea886851c41e606e9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021105"
---
# <span data-ttu-id="fd75d-101">New-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="fd75d-101">New-AzRmStorageShare</span></span>

## <span data-ttu-id="fd75d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fd75d-102">SYNOPSIS</span></span>
<span data-ttu-id="fd75d-103">Crea una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fd75d-103">Creates a Storage file share.</span></span>

## <span data-ttu-id="fd75d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fd75d-104">SYNTAX</span></span>

### <span data-ttu-id="fd75d-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fd75d-105">AccountName (Default)</span></span>
```
New-AzRmStorageShare [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-QuotaGiB <Int32>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd75d-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fd75d-106">AccountObject</span></span>
```
New-AzRmStorageShare -StorageAccount <PSStorageAccount> -Name <String> [-QuotaGiB <Int32>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd75d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd75d-107">DESCRIPTION</span></span>
<span data-ttu-id="fd75d-108">Il cmdlet **New-AzRmStorageShare** crea una condivisione file di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fd75d-108">The **New-AzRmStorageShare** cmdlet creates a Storage file share.</span></span>

## <span data-ttu-id="fd75d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fd75d-109">EXAMPLES</span></span>

### <span data-ttu-id="fd75d-110">Esempio 1: creare una condivisione file di archiviazione con il nome dell'account di archiviazione e il nome della condivisione, con i metadati e la quota di condivisione come 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="fd75d-110">Example 1: Create a Storage file share with Storage account name and share name, with metadata and share quota as 100 GiB.</span></span>
```
PS C:\>New-AzRmStorageShare -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" -Name "myshare" -QuotaGiB 100 -Metadata @{"tag1" = "value1"; "tag2" = "value2" } 

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="fd75d-111">Questo comando crea una condivisione file di archiviazione con metadati e Condividi quota come 100 GiB.</span><span class="sxs-lookup"><span data-stu-id="fd75d-111">This command creates a Storage file share with metadata and share quota as 100 GiB.</span></span>

### <span data-ttu-id="fd75d-112">Esempio 2: creare una condivisione file di archiviazione con l'oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fd75d-112">Example 2: Create a Storage file share with Storage account object</span></span>
```
Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -StorageAccountName "myStorageAccount" | New-AzRmStorageShare -Name "myshare"

Name     StorageAccountName ResourceGroupName Etag                QuotaGiB LastModifiedTime    
----     ------------------ ----------------- ----                -------- ----------------    
myshare  myStorageAccount   myResourceGroup
```

<span data-ttu-id="fd75d-113">Questo comando crea una condivisione file di archiviazione con l'oggetto account di archiviazione e il nome della condivisione.</span><span class="sxs-lookup"><span data-stu-id="fd75d-113">This command creates a Storage file share with Storage account object and share name.</span></span>

## <span data-ttu-id="fd75d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fd75d-114">PARAMETERS</span></span>

### <span data-ttu-id="fd75d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd75d-115">-DefaultProfile</span></span>
<span data-ttu-id="fd75d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fd75d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd75d-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="fd75d-117">-Metadata</span></span>
<span data-ttu-id="fd75d-118">Condividere metadati</span><span class="sxs-lookup"><span data-stu-id="fd75d-118">Share Metadata</span></span>

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

### <span data-ttu-id="fd75d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd75d-119">-Name</span></span>
<span data-ttu-id="fd75d-120">Nome condivisione file di Azure</span><span class="sxs-lookup"><span data-stu-id="fd75d-120">Azure File share name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd75d-121">-QuotaGiB</span><span class="sxs-lookup"><span data-stu-id="fd75d-121">-QuotaGiB</span></span>
<span data-ttu-id="fd75d-122">Condividere la quota in gibibyte.</span><span class="sxs-lookup"><span data-stu-id="fd75d-122">Share Quota in Gibibyte.</span></span>

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

### <span data-ttu-id="fd75d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd75d-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd75d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fd75d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="fd75d-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fd75d-125">-StorageAccount</span></span>
<span data-ttu-id="fd75d-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fd75d-126">Storage account object</span></span>

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

### <span data-ttu-id="fd75d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fd75d-127">-StorageAccountName</span></span>
<span data-ttu-id="fd75d-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fd75d-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="fd75d-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fd75d-129">-Confirm</span></span>
<span data-ttu-id="fd75d-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd75d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd75d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd75d-131">-WhatIf</span></span>
<span data-ttu-id="fd75d-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd75d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd75d-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fd75d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd75d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd75d-134">CommonParameters</span></span>
<span data-ttu-id="fd75d-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd75d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd75d-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd75d-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd75d-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fd75d-137">INPUTS</span></span>

### <span data-ttu-id="fd75d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fd75d-138">System.String</span></span>

### <span data-ttu-id="fd75d-139">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fd75d-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="fd75d-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fd75d-140">OUTPUTS</span></span>

### <span data-ttu-id="fd75d-141">Microsoft. Azure. Commands. Management. storage. Models. PSShare</span><span class="sxs-lookup"><span data-stu-id="fd75d-141">Microsoft.Azure.Commands.Management.Storage.Models.PSShare</span></span>

## <span data-ttu-id="fd75d-142">Note</span><span class="sxs-lookup"><span data-stu-id="fd75d-142">NOTES</span></span>

## <span data-ttu-id="fd75d-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fd75d-143">RELATED LINKS</span></span>
