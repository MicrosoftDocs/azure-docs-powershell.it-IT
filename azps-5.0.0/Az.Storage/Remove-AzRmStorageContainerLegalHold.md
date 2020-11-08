---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 494995a97ccb74df9ad9a9fc1f88272505598bb9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202794"
---
# <span data-ttu-id="1409e-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="1409e-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="1409e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1409e-102">SYNOPSIS</span></span>
<span data-ttu-id="1409e-103">Rimuove i tag di blocco legale da un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1409e-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="1409e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1409e-104">SYNTAX</span></span>

### <span data-ttu-id="1409e-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1409e-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1409e-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="1409e-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1409e-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="1409e-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1409e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1409e-108">DESCRIPTION</span></span>
<span data-ttu-id="1409e-109">Il cmdlet **Remove-AzRmStorageContainerLegalHold** rimuove i tag di blocco legale da un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1409e-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="1409e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1409e-110">EXAMPLES</span></span>

### <span data-ttu-id="1409e-111">Esempio 1: rimuovere i tag di blocco legale da un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="1409e-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="1409e-112">Questo comando rimuove i tag di blocco legale da un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1409e-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="1409e-113">Esempio 2: rimuovere i tag di blocco legale da un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="1409e-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="1409e-114">Questo comando rimuove i tag di blocco legale da un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="1409e-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="1409e-115">Esempio 3: rimuovere i tag di blocco legale da tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="1409e-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="1409e-116">Questo comando rimuove i tag di blocco legale da tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="1409e-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="1409e-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1409e-117">PARAMETERS</span></span>

### <span data-ttu-id="1409e-118">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="1409e-118">-Container</span></span>
<span data-ttu-id="1409e-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1409e-119">Storage container object</span></span>

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

### <span data-ttu-id="1409e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1409e-120">-DefaultProfile</span></span>
<span data-ttu-id="1409e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1409e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1409e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1409e-122">-Name</span></span>
<span data-ttu-id="1409e-123">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="1409e-123">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1409e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1409e-124">-ResourceGroupName</span></span>
<span data-ttu-id="1409e-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1409e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="1409e-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="1409e-126">-StorageAccount</span></span>
<span data-ttu-id="1409e-127">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1409e-127">Storage account object</span></span>

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

### <span data-ttu-id="1409e-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1409e-128">-StorageAccountName</span></span>
<span data-ttu-id="1409e-129">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1409e-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="1409e-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="1409e-130">-Tag</span></span>
<span data-ttu-id="1409e-131">Tag LegalHold contenitore</span><span class="sxs-lookup"><span data-stu-id="1409e-131">Container LegalHold Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1409e-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1409e-132">-Confirm</span></span>
<span data-ttu-id="1409e-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1409e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1409e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1409e-134">-WhatIf</span></span>
<span data-ttu-id="1409e-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1409e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1409e-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1409e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1409e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1409e-137">CommonParameters</span></span>
<span data-ttu-id="1409e-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1409e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1409e-139">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1409e-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1409e-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1409e-140">INPUTS</span></span>

### <span data-ttu-id="1409e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1409e-141">System.String</span></span>

### <span data-ttu-id="1409e-142">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1409e-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="1409e-143">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="1409e-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="1409e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1409e-144">OUTPUTS</span></span>

### <span data-ttu-id="1409e-145">Microsoft. Azure. Commands. Management. storage. Models. PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="1409e-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="1409e-146">Note</span><span class="sxs-lookup"><span data-stu-id="1409e-146">NOTES</span></span>

## <span data-ttu-id="1409e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1409e-147">RELATED LINKS</span></span>
