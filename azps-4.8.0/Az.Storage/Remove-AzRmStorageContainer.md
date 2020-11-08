---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: 333df1432ed892e75e0b798f1412cb7b0327a334
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191142"
---
# <span data-ttu-id="fa706-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fa706-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="fa706-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fa706-102">SYNOPSIS</span></span>
<span data-ttu-id="fa706-103">Rimuove un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fa706-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="fa706-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa706-104">SYNTAX</span></span>

### <span data-ttu-id="fa706-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fa706-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa706-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fa706-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa706-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="fa706-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa706-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fa706-108">DESCRIPTION</span></span>
<span data-ttu-id="fa706-109">Il cmdlet **Remove-AzRmStorageContainer** rimuove un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fa706-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="fa706-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa706-110">EXAMPLES</span></span>

### <span data-ttu-id="fa706-111">Esempio 1: rimuovere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="fa706-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="fa706-112">Questo comando rimuove un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="fa706-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="fa706-113">Esempio 2: rimuovere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="fa706-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="fa706-114">Questo comando rimuove un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="fa706-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fa706-115">Esempio 3: rimuovere tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="fa706-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="fa706-116">Questo comando rimuove tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="fa706-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="fa706-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fa706-117">PARAMETERS</span></span>

### <span data-ttu-id="fa706-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa706-118">-DefaultProfile</span></span>
<span data-ttu-id="fa706-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa706-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa706-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fa706-120">-Force</span></span>
<span data-ttu-id="fa706-121">Forza per rimuovere il contenitore e tutto il contenuto</span><span class="sxs-lookup"><span data-stu-id="fa706-121">Force to remove the container and all content in it</span></span>

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

### <span data-ttu-id="fa706-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa706-122">-InputObject</span></span>
<span data-ttu-id="fa706-123">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fa706-123">Storage container object</span></span>

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

### <span data-ttu-id="fa706-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa706-124">-Name</span></span>
<span data-ttu-id="fa706-125">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="fa706-125">Container Name</span></span>

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

### <span data-ttu-id="fa706-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa706-126">-PassThru</span></span>
<span data-ttu-id="fa706-127">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fa706-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fa706-128">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fa706-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fa706-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa706-129">-ResourceGroupName</span></span>
<span data-ttu-id="fa706-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fa706-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="fa706-131">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa706-131">-StorageAccount</span></span>
<span data-ttu-id="fa706-132">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fa706-132">Storage account object</span></span>

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

### <span data-ttu-id="fa706-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fa706-133">-StorageAccountName</span></span>
<span data-ttu-id="fa706-134">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="fa706-134">Storage Account Name.</span></span>

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

### <span data-ttu-id="fa706-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fa706-135">-Confirm</span></span>
<span data-ttu-id="fa706-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa706-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa706-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa706-137">-WhatIf</span></span>
<span data-ttu-id="fa706-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa706-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa706-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa706-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa706-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa706-140">CommonParameters</span></span>
<span data-ttu-id="fa706-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa706-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa706-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa706-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa706-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fa706-143">INPUTS</span></span>

### <span data-ttu-id="fa706-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fa706-144">System.String</span></span>

### <span data-ttu-id="fa706-145">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa706-145">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fa706-146">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="fa706-146">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="fa706-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa706-147">OUTPUTS</span></span>

### <span data-ttu-id="fa706-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fa706-148">System.Boolean</span></span>

## <span data-ttu-id="fa706-149">Note</span><span class="sxs-lookup"><span data-stu-id="fa706-149">NOTES</span></span>

## <span data-ttu-id="fa706-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa706-150">RELATED LINKS</span></span>
