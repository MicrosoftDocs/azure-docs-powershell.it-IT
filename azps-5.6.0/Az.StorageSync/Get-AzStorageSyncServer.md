---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: 525d51d62477db88da78eaecc482d6cf64dbf810
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973150"
---
# <span data-ttu-id="e5891-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="e5891-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="e5891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5891-102">SYNOPSIS</span></span>
<span data-ttu-id="e5891-103">Questo comando elenca tutti i server registrati con un determinato servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5891-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="e5891-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e5891-104">SYNTAX</span></span>

### <span data-ttu-id="e5891-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="e5891-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5891-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5891-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5891-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e5891-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5891-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e5891-108">DESCRIPTION</span></span>
<span data-ttu-id="e5891-109">Questo comando elenca tutti i server registrati con un determinato servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5891-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="e5891-110">Può essere usato per elencare anche gli attributi di ogni server registrato.</span><span class="sxs-lookup"><span data-stu-id="e5891-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="e5891-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e5891-111">EXAMPLES</span></span>

### <span data-ttu-id="e5891-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e5891-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="e5891-113">Questo comando recupera tutti i server registrati in uno specifico servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="e5891-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="e5891-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5891-114">PARAMETERS</span></span>

### <span data-ttu-id="e5891-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5891-115">-DefaultProfile</span></span>
<span data-ttu-id="e5891-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e5891-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5891-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e5891-117">-ParentObject</span></span>
<span data-ttu-id="e5891-118">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="e5891-118">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5891-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e5891-119">-ParentResourceId</span></span>
<span data-ttu-id="e5891-120">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="e5891-120">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5891-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5891-121">-ResourceGroupName</span></span>
<span data-ttu-id="e5891-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e5891-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5891-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="e5891-123">-ServerId</span></span>
<span data-ttu-id="e5891-124">Nome del server registrato.</span><span class="sxs-lookup"><span data-stu-id="e5891-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5891-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="e5891-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="e5891-126">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="e5891-126">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5891-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5891-127">CommonParameters</span></span>
<span data-ttu-id="e5891-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5891-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5891-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5891-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5891-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="e5891-130">INPUTS</span></span>

### <span data-ttu-id="e5891-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e5891-131">System.String</span></span>

### <span data-ttu-id="e5891-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="e5891-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="e5891-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e5891-133">System.Guid</span></span>

## <span data-ttu-id="e5891-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e5891-134">OUTPUTS</span></span>

### <span data-ttu-id="e5891-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="e5891-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="e5891-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="e5891-136">NOTES</span></span>

## <span data-ttu-id="e5891-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e5891-137">RELATED LINKS</span></span>
