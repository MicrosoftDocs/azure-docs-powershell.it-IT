---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: aa2a03355431f027a9efd374f5af45199cc77452
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857825"
---
# <span data-ttu-id="0e16a-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0e16a-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="0e16a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e16a-102">SYNOPSIS</span></span>
<span data-ttu-id="0e16a-103">Ottiene o elenca i contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e16a-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="0e16a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e16a-104">SYNTAX</span></span>

### <span data-ttu-id="0e16a-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0e16a-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e16a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0e16a-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e16a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e16a-107">DESCRIPTION</span></span>
<span data-ttu-id="0e16a-108">Il cmdlet **Get-AzRmStorageContainer** Ottiene o elenca i contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e16a-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="0e16a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e16a-109">EXAMPLES</span></span>

### <span data-ttu-id="0e16a-110">Esempio 1: ottenere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="0e16a-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="0e16a-111">Questo comando ottiene un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0e16a-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="0e16a-112">Esempio 2: elencare tutti i contenitori BLOB di archiviazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e16a-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="0e16a-113">Questo comando elenca tutti i contenitori BLOB di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0e16a-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="0e16a-114">Esempio 3: ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0e16a-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="0e16a-115">Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0e16a-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="0e16a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e16a-116">PARAMETERS</span></span>

### <span data-ttu-id="0e16a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e16a-117">-AsJob</span></span>
<span data-ttu-id="0e16a-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0e16a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e16a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e16a-119">-DefaultProfile</span></span>
<span data-ttu-id="0e16a-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e16a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e16a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e16a-121">-Name</span></span>
<span data-ttu-id="0e16a-122">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="0e16a-122">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e16a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e16a-123">-ResourceGroupName</span></span>
<span data-ttu-id="0e16a-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e16a-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="0e16a-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e16a-125">-StorageAccount</span></span>
<span data-ttu-id="0e16a-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0e16a-126">Storage account object</span></span>

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

### <span data-ttu-id="0e16a-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0e16a-127">-StorageAccountName</span></span>
<span data-ttu-id="0e16a-128">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0e16a-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="0e16a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e16a-129">CommonParameters</span></span>
<span data-ttu-id="0e16a-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e16a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e16a-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e16a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e16a-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e16a-132">INPUTS</span></span>

### <span data-ttu-id="0e16a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e16a-133">System.String</span></span>

### <span data-ttu-id="0e16a-134">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0e16a-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0e16a-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e16a-135">OUTPUTS</span></span>

### <span data-ttu-id="0e16a-136">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="0e16a-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="0e16a-137">Note</span><span class="sxs-lookup"><span data-stu-id="0e16a-137">NOTES</span></span>

## <span data-ttu-id="0e16a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e16a-138">RELATED LINKS</span></span>
