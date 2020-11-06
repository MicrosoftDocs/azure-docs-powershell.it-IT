---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517287"
---
# <span data-ttu-id="b0904-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b0904-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="b0904-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0904-102">SYNOPSIS</span></span>
<span data-ttu-id="b0904-103">Modifica di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b0904-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0904-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0904-104">SYNTAX</span></span>

### <span data-ttu-id="b0904-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0904-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0904-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b0904-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0904-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="b0904-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0904-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0904-108">DESCRIPTION</span></span>
<span data-ttu-id="b0904-109">Il cmdlet **Update-AzureRmStorageContainer** modifica un contenitore di BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b0904-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="b0904-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0904-110">EXAMPLES</span></span>

### <span data-ttu-id="b0904-111">Esempio 1: modifica i metadati di un contenitore BLOB di archiviazione e l'accesso pubblico con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="b0904-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="b0904-112">Questo comando modifica i metadati di un contenitore BLOB di archiviazione e l'accesso pubblico con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="b0904-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="b0904-113">Esempio 2: disabilitare l'accesso pubblico in un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="b0904-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="b0904-114">Questo comando Disabilita l'accesso pubblico in un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="b0904-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="b0904-115">Esempio 3: impostare l'accesso pubblico come BLOB per tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="b0904-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="b0904-116">Questo comando imposta l'accesso pubblico come BLOB per tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0904-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="b0904-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0904-117">PARAMETERS</span></span>

### <span data-ttu-id="b0904-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0904-118">-DefaultProfile</span></span>
<span data-ttu-id="b0904-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0904-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0904-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0904-120">-InputObject</span></span>
<span data-ttu-id="b0904-121">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b0904-121">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0904-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b0904-122">-Metadata</span></span>
<span data-ttu-id="b0904-123">Metadati contenitore</span><span class="sxs-lookup"><span data-stu-id="b0904-123">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0904-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0904-124">-Name</span></span>
<span data-ttu-id="b0904-125">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="b0904-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0904-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="b0904-126">-PublicAccess</span></span>
<span data-ttu-id="b0904-127">Contenitore PublicAccess</span><span class="sxs-lookup"><span data-stu-id="b0904-127">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0904-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0904-128">-ResourceGroupName</span></span>
<span data-ttu-id="b0904-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0904-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0904-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b0904-130">-StorageAccount</span></span>
<span data-ttu-id="b0904-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b0904-131">Storage account object</span></span>

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

### <span data-ttu-id="b0904-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b0904-132">-StorageAccountName</span></span>
<span data-ttu-id="b0904-133">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b0904-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="b0904-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0904-134">-Confirm</span></span>
<span data-ttu-id="b0904-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0904-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0904-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0904-136">-WhatIf</span></span>
<span data-ttu-id="b0904-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0904-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0904-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0904-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0904-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0904-139">CommonParameters</span></span>
<span data-ttu-id="b0904-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0904-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0904-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0904-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0904-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0904-142">INPUTS</span></span>

### <span data-ttu-id="b0904-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b0904-143">System.String</span></span>

## <span data-ttu-id="b0904-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0904-144">OUTPUTS</span></span>

### <span data-ttu-id="b0904-145">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="b0904-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="b0904-146">Note</span><span class="sxs-lookup"><span data-stu-id="b0904-146">NOTES</span></span>

## <span data-ttu-id="b0904-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0904-147">RELATED LINKS</span></span>

