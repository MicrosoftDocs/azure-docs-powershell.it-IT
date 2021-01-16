---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzRmStorageContainer.md
ms.openlocfilehash: 06a37226c1915ef858d72ec123dd238011c19f19
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324878"
---
# <span data-ttu-id="e55cb-101">New-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="e55cb-101">New-AzRmStorageContainer</span></span>

## <span data-ttu-id="e55cb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e55cb-102">SYNOPSIS</span></span>
<span data-ttu-id="e55cb-103">Crea un contenitore BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e55cb-103">Creates a Storage blob container</span></span>

## <span data-ttu-id="e55cb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e55cb-104">SYNTAX</span></span>

### <span data-ttu-id="e55cb-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e55cb-105">AccountName (Default)</span></span>
```
New-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e55cb-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="e55cb-106">AccountObject</span></span>
```
New-AzRmStorageContainer -StorageAccount <PSStorageAccount> -Name <String> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e55cb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e55cb-107">DESCRIPTION</span></span>
<span data-ttu-id="e55cb-108">Il cmdlet **New-AzRmStorageContainer** crea un contenitore di BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e55cb-108">The **New-AzRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="e55cb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e55cb-109">EXAMPLES</span></span>

### <span data-ttu-id="e55cb-110">Esempio 1: creare un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore con metadati</span><span class="sxs-lookup"><span data-stu-id="e55cb-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="e55cb-111">Questo comando crea un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore con metadati.</span><span class="sxs-lookup"><span data-stu-id="e55cb-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="e55cb-112">Esempio 2: creare un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore con l'accesso pubblico come BLOB</span><span class="sxs-lookup"><span data-stu-id="e55cb-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="e55cb-113">Questo comando crea un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore, con accesso pubblico come BLOB.</span><span class="sxs-lookup"><span data-stu-id="e55cb-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="e55cb-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e55cb-114">PARAMETERS</span></span>

### <span data-ttu-id="e55cb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55cb-115">-DefaultProfile</span></span>
<span data-ttu-id="e55cb-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e55cb-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e55cb-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e55cb-117">-Metadata</span></span>
<span data-ttu-id="e55cb-118">Metadati contenitore</span><span class="sxs-lookup"><span data-stu-id="e55cb-118">Container Metadata</span></span>

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

### <span data-ttu-id="e55cb-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e55cb-119">-Name</span></span>
<span data-ttu-id="e55cb-120">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="e55cb-120">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e55cb-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="e55cb-121">-PublicAccess</span></span>
<span data-ttu-id="e55cb-122">Contenitore PublicAccess</span><span class="sxs-lookup"><span data-stu-id="e55cb-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="e55cb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e55cb-123">-ResourceGroupName</span></span>
<span data-ttu-id="e55cb-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e55cb-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="e55cb-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="e55cb-125">-StorageAccount</span></span>
<span data-ttu-id="e55cb-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="e55cb-126">Storage account object</span></span>

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

### <span data-ttu-id="e55cb-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e55cb-127">-StorageAccountName</span></span>
<span data-ttu-id="e55cb-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e55cb-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="e55cb-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e55cb-129">-Confirm</span></span>
<span data-ttu-id="e55cb-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e55cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55cb-131">-WhatIf</span></span>
<span data-ttu-id="e55cb-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e55cb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e55cb-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e55cb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55cb-134">CommonParameters</span></span>
<span data-ttu-id="e55cb-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e55cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55cb-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e55cb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55cb-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e55cb-137">INPUTS</span></span>

### <span data-ttu-id="e55cb-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e55cb-138">System.String</span></span>

### <span data-ttu-id="e55cb-139">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="e55cb-139">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="e55cb-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e55cb-140">OUTPUTS</span></span>

### <span data-ttu-id="e55cb-141">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="e55cb-141">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="e55cb-142">Note</span><span class="sxs-lookup"><span data-stu-id="e55cb-142">NOTES</span></span>

## <span data-ttu-id="e55cb-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e55cb-143">RELATED LINKS</span></span>
