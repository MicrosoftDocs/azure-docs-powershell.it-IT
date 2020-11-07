---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688049"
---
# <span data-ttu-id="dfcd5-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="dfcd5-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="dfcd5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dfcd5-102">SYNOPSIS</span></span>
<span data-ttu-id="dfcd5-103">Rimuove un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dfcd5-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfcd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfcd5-104">SYNTAX</span></span>

### <span data-ttu-id="dfcd5-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dfcd5-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfcd5-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="dfcd5-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfcd5-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="dfcd5-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfcd5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dfcd5-108">DESCRIPTION</span></span>
<span data-ttu-id="dfcd5-109">Il cmdlet **Remove-AzureRmStorageContainer** rimuove un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dfcd5-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="dfcd5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfcd5-110">EXAMPLES</span></span>

### <span data-ttu-id="dfcd5-111">Esempio 1: rimuovere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="dfcd5-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="dfcd5-112">Questo comando rimuove un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="dfcd5-113">Esempio 2: rimuovere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="dfcd5-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="dfcd5-114">Questo comando rimuove un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="dfcd5-115">Esempio 3: rimuovere tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline</span><span class="sxs-lookup"><span data-stu-id="dfcd5-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="dfcd5-116">Questo comando rimuove tutti i contenitori BLOB di archiviazione in un account di archiviazione con pipeline.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="dfcd5-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dfcd5-117">PARAMETERS</span></span>

### <span data-ttu-id="dfcd5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfcd5-118">-DefaultProfile</span></span>
<span data-ttu-id="dfcd5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfcd5-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dfcd5-120">-Force</span></span>
<span data-ttu-id="dfcd5-121">Forza per rimuovere il contenitore e tutto il contenuto</span><span class="sxs-lookup"><span data-stu-id="dfcd5-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcd5-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfcd5-122">-InputObject</span></span>
<span data-ttu-id="dfcd5-123">Oggetto contenitore di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dfcd5-123">Storage container object</span></span>

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

### <span data-ttu-id="dfcd5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="dfcd5-124">-Name</span></span>
<span data-ttu-id="dfcd5-125">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="dfcd5-125">Container Name</span></span>

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

### <span data-ttu-id="dfcd5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfcd5-126">-PassThru</span></span>
<span data-ttu-id="dfcd5-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="dfcd5-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcd5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfcd5-128">-ResourceGroupName</span></span>
<span data-ttu-id="dfcd5-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="dfcd5-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="dfcd5-130">-StorageAccount</span></span>
<span data-ttu-id="dfcd5-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dfcd5-131">Storage account object</span></span>

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

### <span data-ttu-id="dfcd5-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dfcd5-132">-StorageAccountName</span></span>
<span data-ttu-id="dfcd5-133">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="dfcd5-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dfcd5-134">-Confirm</span></span>
<span data-ttu-id="dfcd5-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcd5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfcd5-136">-WhatIf</span></span>
<span data-ttu-id="dfcd5-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfcd5-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfcd5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfcd5-139">CommonParameters</span></span>
<span data-ttu-id="dfcd5-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfcd5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfcd5-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfcd5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfcd5-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dfcd5-142">INPUTS</span></span>

### <span data-ttu-id="dfcd5-143">System. String</span><span class="sxs-lookup"><span data-stu-id="dfcd5-143">System.String</span></span>

## <span data-ttu-id="dfcd5-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfcd5-144">OUTPUTS</span></span>

### <span data-ttu-id="dfcd5-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="dfcd5-145">System.Object</span></span>

## <span data-ttu-id="dfcd5-146">Note</span><span class="sxs-lookup"><span data-stu-id="dfcd5-146">NOTES</span></span>

## <span data-ttu-id="dfcd5-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfcd5-147">RELATED LINKS</span></span>
