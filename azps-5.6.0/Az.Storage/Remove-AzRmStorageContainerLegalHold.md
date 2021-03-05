---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azrmstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainerLegalHold.md
ms.openlocfilehash: 9788acb95be63d9e76525cbeaf7904cd260baae0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988692"
---
# <span data-ttu-id="cad1b-101">Remove-AzRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="cad1b-101">Remove-AzRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="cad1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cad1b-102">SYNOPSIS</span></span>
<span data-ttu-id="cad1b-103">Rimuove i tag di blocco legale da un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cad1b-103">Removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="cad1b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cad1b-104">SYNTAX</span></span>

### <span data-ttu-id="cad1b-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cad1b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cad1b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cad1b-106">AccountObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad1b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="cad1b-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad1b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cad1b-108">DESCRIPTION</span></span>
<span data-ttu-id="cad1b-109">Il cmdlet **Remove-AzRmStorageContainerLegalHold** rimuove i tag di blocco legale da un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cad1b-109">The **Remove-AzRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="cad1b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cad1b-110">EXAMPLES</span></span>

### <span data-ttu-id="cad1b-111">Esempio 1: Rimuovere tag di blocco a livello legale da un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="cad1b-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="cad1b-112">Questo comando rimuove i tag per i blocchi legali da un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="cad1b-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="cad1b-113">Esempio 2: Rimuovere tag di blocco a livello legale da un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="cad1b-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2
```

<span data-ttu-id="cad1b-114">Questo comando rimuove i tag di blocco legale da un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="cad1b-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="cad1b-115">Esempio 3: Rimuovere tag di blocco a livello legale da tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="cad1b-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="cad1b-116">Questo comando rimuove i tag di blocco legale da tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="cad1b-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="cad1b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cad1b-117">PARAMETERS</span></span>

### <span data-ttu-id="cad1b-118">-Container</span><span class="sxs-lookup"><span data-stu-id="cad1b-118">-Container</span></span>
<span data-ttu-id="cad1b-119">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cad1b-119">Storage container object</span></span>

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

### <span data-ttu-id="cad1b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad1b-120">-DefaultProfile</span></span>
<span data-ttu-id="cad1b-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cad1b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cad1b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cad1b-122">-Name</span></span>
<span data-ttu-id="cad1b-123">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="cad1b-123">Container Name</span></span>

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

### <span data-ttu-id="cad1b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cad1b-124">-ResourceGroupName</span></span>
<span data-ttu-id="cad1b-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cad1b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="cad1b-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="cad1b-126">-StorageAccount</span></span>
<span data-ttu-id="cad1b-127">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cad1b-127">Storage account object</span></span>

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

### <span data-ttu-id="cad1b-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cad1b-128">-StorageAccountName</span></span>
<span data-ttu-id="cad1b-129">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cad1b-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="cad1b-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="cad1b-130">-Tag</span></span>
<span data-ttu-id="cad1b-131">Container LegalHold Tag</span><span class="sxs-lookup"><span data-stu-id="cad1b-131">Container LegalHold Tags</span></span>

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

### <span data-ttu-id="cad1b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cad1b-132">-Confirm</span></span>
<span data-ttu-id="cad1b-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cad1b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad1b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad1b-134">-WhatIf</span></span>
<span data-ttu-id="cad1b-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cad1b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cad1b-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cad1b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad1b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad1b-137">CommonParameters</span></span>
<span data-ttu-id="cad1b-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad1b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad1b-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cad1b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad1b-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="cad1b-140">INPUTS</span></span>

### <span data-ttu-id="cad1b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="cad1b-141">System.String</span></span>

### <span data-ttu-id="cad1b-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cad1b-142">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="cad1b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="cad1b-143">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="cad1b-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cad1b-144">OUTPUTS</span></span>

### <span data-ttu-id="cad1b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span><span class="sxs-lookup"><span data-stu-id="cad1b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="cad1b-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="cad1b-146">NOTES</span></span>

## <span data-ttu-id="cad1b-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cad1b-147">RELATED LINKS</span></span>
