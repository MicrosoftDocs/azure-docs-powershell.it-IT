---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509000"
---
# <span data-ttu-id="4c4ff-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4c4ff-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="4c4ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4ff-103">Crea un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c4ff-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c4ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c4ff-104">SYNTAX</span></span>

### <span data-ttu-id="4c4ff-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c4ff-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c4ff-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="4c4ff-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c4ff-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c4ff-107">DESCRIPTION</span></span>
<span data-ttu-id="4c4ff-108">Il cmdlet **New-AzureRmStorageContainer** crea un contenitore di BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c4ff-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="4c4ff-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c4ff-109">EXAMPLES</span></span>

### <span data-ttu-id="4c4ff-110">Esempio 1: creare un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore con metadati</span><span class="sxs-lookup"><span data-stu-id="4c4ff-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="4c4ff-111">Questo comando crea un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore con metadati.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="4c4ff-112">Esempio 2: creare un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore con l'accesso pubblico come BLOB</span><span class="sxs-lookup"><span data-stu-id="4c4ff-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="4c4ff-113">Questo comando crea un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore, con accesso pubblico come BLOB.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="4c4ff-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c4ff-114">PARAMETERS</span></span>

### <span data-ttu-id="4c4ff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4ff-115">-DefaultProfile</span></span>
<span data-ttu-id="4c4ff-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c4ff-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="4c4ff-117">-Metadata</span></span>
<span data-ttu-id="4c4ff-118">Metadati contenitore</span><span class="sxs-lookup"><span data-stu-id="4c4ff-118">Container Metadata</span></span>

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

### <span data-ttu-id="4c4ff-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c4ff-119">-Name</span></span>
<span data-ttu-id="4c4ff-120">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="4c4ff-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4ff-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="4c4ff-121">-PublicAccess</span></span>
<span data-ttu-id="4c4ff-122">Contenitore PublicAccess</span><span class="sxs-lookup"><span data-stu-id="4c4ff-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="4c4ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c4ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="4c4ff-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="4c4ff-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="4c4ff-125">-StorageAccount</span></span>
<span data-ttu-id="4c4ff-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c4ff-126">Storage account object</span></span>

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

### <span data-ttu-id="4c4ff-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4c4ff-127">-StorageAccountName</span></span>
<span data-ttu-id="4c4ff-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="4c4ff-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c4ff-129">-Confirm</span></span>
<span data-ttu-id="4c4ff-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c4ff-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c4ff-131">-WhatIf</span></span>
<span data-ttu-id="4c4ff-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c4ff-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c4ff-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4ff-134">CommonParameters</span></span>
<span data-ttu-id="4c4ff-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c4ff-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4ff-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c4ff-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4ff-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c4ff-137">INPUTS</span></span>

### <span data-ttu-id="4c4ff-138">System. String</span><span class="sxs-lookup"><span data-stu-id="4c4ff-138">System.String</span></span>

## <span data-ttu-id="4c4ff-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c4ff-139">OUTPUTS</span></span>

### <span data-ttu-id="4c4ff-140">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="4c4ff-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="4c4ff-141">Note</span><span class="sxs-lookup"><span data-stu-id="4c4ff-141">NOTES</span></span>

## <span data-ttu-id="4c4ff-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c4ff-142">RELATED LINKS</span></span>

