---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: a9d5b5582a630a3131761d44c329a47c49546f11
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676461"
---
# <span data-ttu-id="42b2a-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="42b2a-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="42b2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="42b2a-103">Questo comando elenca tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="42b2a-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="42b2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42b2a-104">SYNTAX</span></span>

### <span data-ttu-id="42b2a-105">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="42b2a-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42b2a-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="42b2a-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42b2a-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="42b2a-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42b2a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42b2a-108">DESCRIPTION</span></span>
<span data-ttu-id="42b2a-109">Questo comando elenca tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="42b2a-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="42b2a-110">Può essere usato anche per elencare gli attributi di ogni server registrato.</span><span class="sxs-lookup"><span data-stu-id="42b2a-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="42b2a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42b2a-111">EXAMPLES</span></span>

### <span data-ttu-id="42b2a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="42b2a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="42b2a-113">Questo comando consente di ottenere tutti i server registrati in un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="42b2a-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="42b2a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42b2a-114">PARAMETERS</span></span>

### <span data-ttu-id="42b2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42b2a-115">-DefaultProfile</span></span>
<span data-ttu-id="42b2a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="42b2a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42b2a-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="42b2a-117">-ParentObject</span></span>
<span data-ttu-id="42b2a-118">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="42b2a-118">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="42b2a-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="42b2a-119">-ParentResourceId</span></span>
<span data-ttu-id="42b2a-120">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="42b2a-120">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="42b2a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42b2a-121">-ResourceGroupName</span></span>
<span data-ttu-id="42b2a-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42b2a-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="42b2a-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="42b2a-123">-ServerId</span></span>
<span data-ttu-id="42b2a-124">Nome della RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="42b2a-124">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="42b2a-125">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="42b2a-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="42b2a-126">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="42b2a-126">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="42b2a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42b2a-127">CommonParameters</span></span>
<span data-ttu-id="42b2a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42b2a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42b2a-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42b2a-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42b2a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42b2a-130">INPUTS</span></span>

### <span data-ttu-id="42b2a-131">System. String</span><span class="sxs-lookup"><span data-stu-id="42b2a-131">System.String</span></span>

### <span data-ttu-id="42b2a-132">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="42b2a-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="42b2a-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="42b2a-133">System.Guid</span></span>

## <span data-ttu-id="42b2a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42b2a-134">OUTPUTS</span></span>

### <span data-ttu-id="42b2a-135">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="42b2a-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="42b2a-136">Note</span><span class="sxs-lookup"><span data-stu-id="42b2a-136">NOTES</span></span>

## <span data-ttu-id="42b2a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42b2a-137">RELATED LINKS</span></span>
