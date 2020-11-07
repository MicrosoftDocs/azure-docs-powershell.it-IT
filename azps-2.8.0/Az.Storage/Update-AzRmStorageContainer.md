---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzRmStorageContainer.md
ms.openlocfilehash: 879645975636a981ded22a0fe63d398fc4659d85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857797"
---
# <span data-ttu-id="97c6c-101">Update-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="97c6c-101">Update-AzRmStorageContainer</span></span>

## <span data-ttu-id="97c6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="97c6c-103">Modifica di un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="97c6c-103">Modifies a Storage blob container</span></span>

## <span data-ttu-id="97c6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97c6c-104">SYNTAX</span></span>

### <span data-ttu-id="97c6c-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="97c6c-105">AccountName (Default)</span></span>
```
Update-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c6c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="97c6c-106">AccountObject</span></span>
```
Update-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97c6c-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="97c6c-107">ContainerObject</span></span>
```
Update-AzRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97c6c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97c6c-108">DESCRIPTION</span></span>
<span data-ttu-id="97c6c-109">Il cmdlet **Update-AzRmStorageContainer** modifica un contenitore di BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="97c6c-109">The **Update-AzRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="97c6c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97c6c-110">EXAMPLES</span></span>

### <span data-ttu-id="97c6c-111">Esempio 1: modifica i metadati di un contenitore BLOB di archiviazione e l'accesso pubblico con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="97c6c-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"}
```

<span data-ttu-id="97c6c-112">Questo comando modifica i metadati di un contenitore BLOB di archiviazione e l'accesso pubblico con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="97c6c-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="97c6c-113">Esempio 2: disabilitare l'accesso pubblico in un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="97c6c-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="97c6c-114">Questo comando Disabilita l'accesso pubblico in un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="97c6c-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="97c6c-115">Esempio 3: impostare l'accesso pubblico come BLOB per tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="97c6c-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="97c6c-116">Questo comando imposta l'accesso pubblico come BLOB per tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="97c6c-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="97c6c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97c6c-117">PARAMETERS</span></span>

### <span data-ttu-id="97c6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97c6c-118">-DefaultProfile</span></span>
<span data-ttu-id="97c6c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97c6c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97c6c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97c6c-120">-InputObject</span></span>
<span data-ttu-id="97c6c-121">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="97c6c-121">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97c6c-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="97c6c-122">-Metadata</span></span>
<span data-ttu-id="97c6c-123">Metadati contenitore</span><span class="sxs-lookup"><span data-stu-id="97c6c-123">Container Metadata</span></span>

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

### <span data-ttu-id="97c6c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="97c6c-124">-Name</span></span>
<span data-ttu-id="97c6c-125">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="97c6c-125">Container Name</span></span>

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

### <span data-ttu-id="97c6c-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="97c6c-126">-PublicAccess</span></span>
<span data-ttu-id="97c6c-127">Contenitore PublicAccess</span><span class="sxs-lookup"><span data-stu-id="97c6c-127">Container PublicAccess</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSPublicAccess
Parameter Sets: (All)
Aliases:
Accepted values: Container, Blob, None

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97c6c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97c6c-128">-ResourceGroupName</span></span>
<span data-ttu-id="97c6c-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="97c6c-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="97c6c-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="97c6c-130">-StorageAccount</span></span>
<span data-ttu-id="97c6c-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="97c6c-131">Storage account object</span></span>

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

### <span data-ttu-id="97c6c-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="97c6c-132">-StorageAccountName</span></span>
<span data-ttu-id="97c6c-133">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="97c6c-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="97c6c-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97c6c-134">-Confirm</span></span>
<span data-ttu-id="97c6c-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97c6c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97c6c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97c6c-136">-WhatIf</span></span>
<span data-ttu-id="97c6c-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97c6c-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="97c6c-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97c6c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97c6c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97c6c-139">CommonParameters</span></span>
<span data-ttu-id="97c6c-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97c6c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97c6c-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97c6c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97c6c-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97c6c-142">INPUTS</span></span>

### <span data-ttu-id="97c6c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="97c6c-143">System.String</span></span>

### <span data-ttu-id="97c6c-144">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="97c6c-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="97c6c-145">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="97c6c-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="97c6c-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97c6c-146">OUTPUTS</span></span>

### <span data-ttu-id="97c6c-147">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="97c6c-147">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="97c6c-148">Note</span><span class="sxs-lookup"><span data-stu-id="97c6c-148">NOTES</span></span>

## <span data-ttu-id="97c6c-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97c6c-149">RELATED LINKS</span></span>
