---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainer.md
ms.openlocfilehash: 64e3857ddd9a9bb00b94e3e550c6be33722990a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508996"
---
# <span data-ttu-id="d0ca0-101">Get-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d0ca0-101">Get-AzureRmStorageContainer</span></span>

## <span data-ttu-id="d0ca0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0ca0-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ca0-103">Ottiene o elenca i contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d0ca0-103">Gets or lists Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0ca0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0ca0-104">SYNTAX</span></span>

### <span data-ttu-id="d0ca0-105">AccountName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0ca0-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0ca0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d0ca0-106">AccountObject</span></span>
```
Get-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ca0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0ca0-107">DESCRIPTION</span></span>
<span data-ttu-id="d0ca0-108">Il cmdlet **Get-AzureRmStorageContainer** Ottiene o elenca i contenitori BLOB di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d0ca0-108">The **Get-AzureRmStorageContainer** cmdlet gets or lists  Storage blob containers</span></span>

## <span data-ttu-id="d0ca0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0ca0-109">EXAMPLES</span></span>

### <span data-ttu-id="d0ca0-110">Esempio 1: ottenere un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore</span><span class="sxs-lookup"><span data-stu-id="d0ca0-110">Example 1: Get a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" 
```

<span data-ttu-id="d0ca0-111">Questo comando ottiene un contenitore BLOB di archiviazione con il nome dell'account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-111">This command gets a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="d0ca0-112">Esempio 2: elencare tutti i contenitori BLOB di archiviazione di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d0ca0-112">Example 2: List  all Storage blob containers of a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" 
```

<span data-ttu-id="d0ca0-113">Questo comando elenca tutti i contenitori BLOB di archiviazione di un account di archiviazione con il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-113">This command lists all Storage blob containers of a Storage account with Storage account name.</span></span>

### <span data-ttu-id="d0ca0-114">Esempio 3: ottenere un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-114">Example 3: Get a Storage blob container with Storage account object and container name.</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" 
```

<span data-ttu-id="d0ca0-115">Questo comando ottiene un contenitore BLOB di archiviazione con l'oggetto account di archiviazione e il nome del contenitore.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-115">This command gets a Storage blob container with Storage account object and container name.</span></span>

## <span data-ttu-id="d0ca0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0ca0-116">PARAMETERS</span></span>

### <span data-ttu-id="d0ca0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ca0-117">-DefaultProfile</span></span>
<span data-ttu-id="d0ca0-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0ca0-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0ca0-119">-Name</span></span>
<span data-ttu-id="d0ca0-120">Nome contenitore</span><span class="sxs-lookup"><span data-stu-id="d0ca0-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0ca0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ca0-121">-ResourceGroupName</span></span>
<span data-ttu-id="d0ca0-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="d0ca0-123">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d0ca0-123">-StorageAccount</span></span>
<span data-ttu-id="d0ca0-124">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d0ca0-124">Storage account object</span></span>

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

### <span data-ttu-id="d0ca0-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d0ca0-125">-StorageAccountName</span></span>
<span data-ttu-id="d0ca0-126">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-126">Storage Account Name.</span></span>

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

### <span data-ttu-id="d0ca0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ca0-127">CommonParameters</span></span>
<span data-ttu-id="d0ca0-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ca0-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0ca0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ca0-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0ca0-130">INPUTS</span></span>

### <span data-ttu-id="d0ca0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="d0ca0-131">System.String</span></span>

## <span data-ttu-id="d0ca0-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0ca0-132">OUTPUTS</span></span>

### <span data-ttu-id="d0ca0-133">Microsoft. Azure. Commands. Management. storage. Models. PSContainer</span><span class="sxs-lookup"><span data-stu-id="d0ca0-133">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="d0ca0-134">Note</span><span class="sxs-lookup"><span data-stu-id="d0ca0-134">NOTES</span></span>

## <span data-ttu-id="d0ca0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0ca0-135">RELATED LINKS</span></span>

