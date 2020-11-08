---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: ebee7b772fc4da3ef14d2273b79b089d57fa317f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188701"
---
# <span data-ttu-id="1e752-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="1e752-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="1e752-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e752-102">SYNOPSIS</span></span>
<span data-ttu-id="1e752-103">Questo comando elenca tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="1e752-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="1e752-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e752-104">SYNTAX</span></span>

### <span data-ttu-id="1e752-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e752-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e752-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e752-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e752-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e752-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e752-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e752-108">DESCRIPTION</span></span>
<span data-ttu-id="1e752-109">Questo comando elenca tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="1e752-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="1e752-110">Può essere usato anche per elencare gli attributi di ogni server registrato.</span><span class="sxs-lookup"><span data-stu-id="1e752-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="1e752-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e752-111">EXAMPLES</span></span>

### <span data-ttu-id="1e752-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1e752-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="1e752-113">Questo comando consente di ottenere tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="1e752-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="1e752-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e752-114">PARAMETERS</span></span>

### <span data-ttu-id="1e752-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e752-115">-DefaultProfile</span></span>
<span data-ttu-id="1e752-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e752-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e752-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1e752-117">-ParentObject</span></span>
<span data-ttu-id="1e752-118">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="1e752-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1e752-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1e752-119">-ParentResourceId</span></span>
<span data-ttu-id="1e752-120">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="1e752-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="1e752-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e752-121">-ResourceGroupName</span></span>
<span data-ttu-id="1e752-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e752-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="1e752-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="1e752-123">-ServerId</span></span>
<span data-ttu-id="1e752-124">Nome della RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="1e752-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="1e752-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1e752-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="1e752-126">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1e752-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="1e752-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e752-127">CommonParameters</span></span>
<span data-ttu-id="1e752-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e752-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e752-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e752-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e752-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e752-130">INPUTS</span></span>

### <span data-ttu-id="1e752-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1e752-131">System.String</span></span>

### <span data-ttu-id="1e752-132">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="1e752-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="1e752-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="1e752-133">System.Guid</span></span>

## <span data-ttu-id="1e752-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e752-134">OUTPUTS</span></span>

### <span data-ttu-id="1e752-135">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="1e752-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="1e752-136">Note</span><span class="sxs-lookup"><span data-stu-id="1e752-136">NOTES</span></span>

## <span data-ttu-id="1e752-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e752-137">RELATED LINKS</span></span>
