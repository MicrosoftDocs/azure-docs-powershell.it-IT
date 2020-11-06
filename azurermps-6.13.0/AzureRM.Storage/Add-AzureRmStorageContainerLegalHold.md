---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Add-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: 465a40e384e5ea7240e0ced2a010c88529feb2f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509003"
---
# <span data-ttu-id="76eab-101">Add-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="76eab-101">Add-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="76eab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76eab-102">SYNOPSIS</span></span>
<span data-ttu-id="76eab-103">Aggiunge tag di blocco legale a un contenitore di archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="76eab-103">Adds legal hold tags to a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76eab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76eab-104">SYNTAX</span></span>

### <span data-ttu-id="76eab-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76eab-105">AccountName (Default)</span></span>
```
Add-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76eab-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="76eab-106">AccountObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76eab-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="76eab-107">ContainerObject</span></span>
```
Add-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76eab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76eab-108">DESCRIPTION</span></span>
<span data-ttu-id="76eab-109">Il cmdlet **Add-AzureRmStorageContainerLegalHold** aggiunge tag di blocco legale a un contenitore di archiviazione BLOB</span><span class="sxs-lookup"><span data-stu-id="76eab-109">The **Add-AzureRmStorageContainerLegalHold** cmdlet adds legal hold tags to a Storage blob container</span></span>

## <span data-ttu-id="76eab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76eab-110">EXAMPLES</span></span>

### <span data-ttu-id="76eab-111">Esempio 1: aggiungere i tag di blocco legale a un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="76eab-111">Example 1: Add legal hold tags to a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Add-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1,tag2 
```

<span data-ttu-id="76eab-112">Questo comando aggiunge i tag di blocco legale a un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="76eab-112">This command adds legal hold tags to a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="76eab-113">Esempio 2: aggiungere i tag di blocco legale a un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="76eab-113">Example 2: Add legal hold tags to a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Add-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1
```

<span data-ttu-id="76eab-114">Questo comando aggiunge i tag di blocco legale a un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="76eab-114">This command adds legal hold tags to a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="76eab-115">Esempio 3: aggiungere tag di blocco legale a tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="76eab-115">Example 3: Add legal hold tags to all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Add-AzureRmStorageContainerLegalHold -Tag  tag1,tag2,tag3
```

<span data-ttu-id="76eab-116">Questo comando aggiunge i tag di blocco legale a tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="76eab-116">This command adds legal hold tags to all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="76eab-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76eab-117">PARAMETERS</span></span>

### <span data-ttu-id="76eab-118">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="76eab-118">-Container</span></span>
<span data-ttu-id="76eab-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="76eab-119">Storage container object</span></span>

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

### <span data-ttu-id="76eab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76eab-120">-DefaultProfile</span></span>
<span data-ttu-id="76eab-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76eab-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76eab-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="76eab-122">-Name</span></span>
<span data-ttu-id="76eab-123">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="76eab-123">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76eab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76eab-124">-ResourceGroupName</span></span>
<span data-ttu-id="76eab-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76eab-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="76eab-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="76eab-126">-StorageAccount</span></span>
<span data-ttu-id="76eab-127">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="76eab-127">Storage account object</span></span>

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

### <span data-ttu-id="76eab-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="76eab-128">-StorageAccountName</span></span>
<span data-ttu-id="76eab-129">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76eab-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="76eab-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="76eab-130">-Tag</span></span>
<span data-ttu-id="76eab-131">Tag LegalHold contenitore</span><span class="sxs-lookup"><span data-stu-id="76eab-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76eab-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="76eab-132">-Confirm</span></span>
<span data-ttu-id="76eab-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76eab-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76eab-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76eab-134">-WhatIf</span></span>
<span data-ttu-id="76eab-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76eab-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76eab-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76eab-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76eab-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76eab-137">CommonParameters</span></span>
<span data-ttu-id="76eab-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76eab-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76eab-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76eab-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76eab-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76eab-140">INPUTS</span></span>

### <span data-ttu-id="76eab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="76eab-141">System.String</span></span>

## <span data-ttu-id="76eab-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76eab-142">OUTPUTS</span></span>

### <span data-ttu-id="76eab-143">Microsoft. Azure. Commands. Management. storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="76eab-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="76eab-144">Note</span><span class="sxs-lookup"><span data-stu-id="76eab-144">NOTES</span></span>

## <span data-ttu-id="76eab-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76eab-145">RELATED LINKS</span></span>

