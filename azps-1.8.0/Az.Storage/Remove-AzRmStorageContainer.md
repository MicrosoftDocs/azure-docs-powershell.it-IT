---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676545"
---
# <span data-ttu-id="52e0b-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="52e0b-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="52e0b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="52e0b-103">Rimuove un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52e0b-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="52e0b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52e0b-104">SYNTAX</span></span>

### <span data-ttu-id="52e0b-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52e0b-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52e0b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="52e0b-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52e0b-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="52e0b-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52e0b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52e0b-108">DESCRIPTION</span></span>
<span data-ttu-id="52e0b-109">Il cmdlet **Remove-AzRmStorageContainer** rimuove un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52e0b-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="52e0b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52e0b-110">EXAMPLES</span></span>

### <span data-ttu-id="52e0b-111">Esempio 1: rimuovere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="52e0b-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="52e0b-112">Questo comando rimuove un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="52e0b-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="52e0b-113">Esempio 2: rimuovere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="52e0b-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="52e0b-114">Questo comando rimuove un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="52e0b-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="52e0b-115">Esempio 3: rimuovere tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="52e0b-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="52e0b-116">Questo comando rimuove tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="52e0b-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="52e0b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52e0b-117">PARAMETERS</span></span>

### <span data-ttu-id="52e0b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52e0b-118">-DefaultProfile</span></span>
<span data-ttu-id="52e0b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52e0b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52e0b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="52e0b-120">-Force</span></span>
<span data-ttu-id="52e0b-121">Forza per rimuovere il contenitore e tutto il contenuto</span><span class="sxs-lookup"><span data-stu-id="52e0b-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e0b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52e0b-122">-InputObject</span></span>
<span data-ttu-id="52e0b-123">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52e0b-123">Storage container object</span></span>

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

### <span data-ttu-id="52e0b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="52e0b-124">-Name</span></span>
<span data-ttu-id="52e0b-125">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="52e0b-125">Container Name</span></span>

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

### <span data-ttu-id="52e0b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52e0b-126">-PassThru</span></span>
<span data-ttu-id="52e0b-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="52e0b-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e0b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52e0b-128">-ResourceGroupName</span></span>
<span data-ttu-id="52e0b-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52e0b-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="52e0b-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="52e0b-130">-StorageAccount</span></span>
<span data-ttu-id="52e0b-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52e0b-131">Storage account object</span></span>

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

### <span data-ttu-id="52e0b-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="52e0b-132">-StorageAccountName</span></span>
<span data-ttu-id="52e0b-133">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52e0b-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="52e0b-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="52e0b-134">-Confirm</span></span>
<span data-ttu-id="52e0b-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52e0b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e0b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52e0b-136">-WhatIf</span></span>
<span data-ttu-id="52e0b-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52e0b-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52e0b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52e0b-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52e0b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52e0b-139">CommonParameters</span></span>
<span data-ttu-id="52e0b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52e0b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52e0b-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52e0b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52e0b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52e0b-142">INPUTS</span></span>

### <span data-ttu-id="52e0b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="52e0b-143">System.String</span></span>

### <span data-ttu-id="52e0b-144">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="52e0b-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="52e0b-145">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="52e0b-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="52e0b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52e0b-146">OUTPUTS</span></span>

### <span data-ttu-id="52e0b-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52e0b-147">System.Boolean</span></span>

## <span data-ttu-id="52e0b-148">Note</span><span class="sxs-lookup"><span data-stu-id="52e0b-148">NOTES</span></span>

## <span data-ttu-id="52e0b-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52e0b-149">RELATED LINKS</span></span>
