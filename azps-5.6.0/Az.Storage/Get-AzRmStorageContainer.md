---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: c4f5fe5fa703d2706d37cd0bebf9df79fd272f5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002909"
---
# <span data-ttu-id="8b0df-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="8b0df-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="8b0df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b0df-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0df-103">Ottiene o elenca contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8b0df-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="8b0df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8b0df-104">SYNTAX</span></span>

### <span data-ttu-id="8b0df-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8b0df-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b0df-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8b0df-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b0df-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8b0df-107">DESCRIPTION</span></span>
<span data-ttu-id="8b0df-108">Il cmdlet **Get-AzRmStorageContainer** ottiene o elenca contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8b0df-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="8b0df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8b0df-109">EXAMPLES</span></span>

### <span data-ttu-id="8b0df-110">Esempio 1: Ottenere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="8b0df-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="8b0df-111">Questo comando ottiene un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b0df-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="8b0df-112">Esempio 2: Elencare tutti i contenitori BLOB di archiviazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8b0df-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="8b0df-113">Questo comando elenca tutti i contenitori BLOB di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8b0df-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="8b0df-114">Esempio 3: Ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b0df-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="8b0df-115">Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="8b0df-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="8b0df-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b0df-116">PARAMETERS</span></span>

### <span data-ttu-id="8b0df-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b0df-117">-AsJob</span></span>
<span data-ttu-id="8b0df-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8b0df-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b0df-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0df-119">-DefaultProfile</span></span>
<span data-ttu-id="8b0df-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8b0df-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b0df-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b0df-121">-Name</span></span>
<span data-ttu-id="8b0df-122">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="8b0df-122">Container Name</span></span>

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

### <span data-ttu-id="8b0df-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0df-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b0df-124">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8b0df-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="8b0df-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b0df-125">-StorageAccount</span></span>
<span data-ttu-id="8b0df-126">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="8b0df-126">Storage account object</span></span>

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

### <span data-ttu-id="8b0df-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8b0df-127">-StorageAccountName</span></span>
<span data-ttu-id="8b0df-128">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8b0df-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="8b0df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0df-129">CommonParameters</span></span>
<span data-ttu-id="8b0df-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0df-131">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0df-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0df-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="8b0df-132">INPUTS</span></span>

### <span data-ttu-id="8b0df-133">System.String</span><span class="sxs-lookup"><span data-stu-id="8b0df-133">System.String</span></span>

### <span data-ttu-id="8b0df-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8b0df-134">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="8b0df-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8b0df-135">OUTPUTS</span></span>

### <span data-ttu-id="8b0df-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span><span class="sxs-lookup"><span data-stu-id="8b0df-136">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="8b0df-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="8b0df-137">NOTES</span></span>

## <span data-ttu-id="8b0df-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8b0df-138">RELATED LINKS</span></span>
