---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainer.md
ms.openlocfilehash: f15d9905abbc7a61dc77d4e8b28c5942126d7b14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676650"
---
# <span data-ttu-id="0712a-101">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="0712a-101">Get-AzRmStorageContainer</span></span>

## <span data-ttu-id="0712a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0712a-102">SYNOPSIS</span></span>
<span data-ttu-id="0712a-103">Ottiene o elenca i contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0712a-103">Gets or lists Storage blob containers</span></span>

## <span data-ttu-id="0712a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0712a-104">SYNTAX</span></span>

### <span data-ttu-id="0712a-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0712a-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0712a-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0712a-106">AccountObject</span></span>
```
Get-AzRmStorageContainer -StorageAccount <PSStorageAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0712a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0712a-107">DESCRIPTION</span></span>
<span data-ttu-id="0712a-108">Il cmdlet **Get-AzRmStorageContainer** Ottiene o elenca i contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0712a-108">The **Get-AzRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="0712a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0712a-109">EXAMPLES</span></span>

### <span data-ttu-id="0712a-110">Esempio 1: ottenere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="0712a-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="0712a-111">Questo comando ottiene un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0712a-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="0712a-112">Esempio 2: elencare tutti i contenitori BLOB di archiviazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0712a-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="0712a-113">Questo comando elenca tutti i contenitori BLOB di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0712a-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="0712a-114">Esempio 3: ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0712a-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="0712a-115">Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0712a-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="0712a-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0712a-116">PARAMETERS</span></span>

### <span data-ttu-id="0712a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0712a-117">-DefaultProfile</span></span>
<span data-ttu-id="0712a-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0712a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0712a-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0712a-119">-Name</span></span>
<span data-ttu-id="0712a-120">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="0712a-120">Container Name</span></span>

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

### <span data-ttu-id="0712a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0712a-121">-ResourceGroupName</span></span>
<span data-ttu-id="0712a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0712a-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="0712a-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="0712a-123">-StorageAccount</span></span>
<span data-ttu-id="0712a-124">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="0712a-124">Storage account object</span></span>

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

### <span data-ttu-id="0712a-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0712a-125">-StorageAccountName</span></span>
<span data-ttu-id="0712a-126">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0712a-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="0712a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0712a-127">CommonParameters</span></span>
<span data-ttu-id="0712a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0712a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0712a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0712a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0712a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0712a-130">INPUTS</span></span>

### <span data-ttu-id="0712a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="0712a-131">System.String</span></span>

### <span data-ttu-id="0712a-132">Microsoft. Azure. Commands. Management. storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0712a-132">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="0712a-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0712a-133">OUTPUTS</span></span>

### <span data-ttu-id="0712a-134">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="0712a-134">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="0712a-135">Note</span><span class="sxs-lookup"><span data-stu-id="0712a-135">NOTES</span></span>

## <span data-ttu-id="0712a-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0712a-136">RELATED LINKS</span></span>
