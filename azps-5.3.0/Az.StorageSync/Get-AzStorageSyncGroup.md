---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncGroup.md
ms.openlocfilehash: b59d5dd1ca094d4b4d5eed276957f07b7d34f1f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474624"
---
# <span data-ttu-id="0395a-101">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0395a-101">Get-AzStorageSyncGroup</span></span>

## <span data-ttu-id="0395a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0395a-102">SYNOPSIS</span></span>
<span data-ttu-id="0395a-103">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="0395a-103">This command lists all sync groups within a given storage sync service.</span></span>

## <span data-ttu-id="0395a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0395a-104">SYNTAX</span></span>

### <span data-ttu-id="0395a-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0395a-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0395a-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0395a-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0395a-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0395a-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncGroup [-ParentResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0395a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0395a-108">DESCRIPTION</span></span>
<span data-ttu-id="0395a-109">Questo comando elenca tutti i gruppi di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specifico.</span><span class="sxs-lookup"><span data-stu-id="0395a-109">This command lists all sync groups within a given storage sync service.</span></span> <span data-ttu-id="0395a-110">Può essere usato anche per elencare gli attributi di ogni gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="0395a-110">It can be used to also list the attributes of each sync group.</span></span>

## <span data-ttu-id="0395a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0395a-111">EXAMPLES</span></span>

### <span data-ttu-id="0395a-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0395a-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncGroup New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="0395a-113">Questo comando consente di ottenere tutti i gruppi di sincronizzazione contenuti nel servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="0395a-113">This command gets all sync groups contained within the specified storage sync service.</span></span> <span data-ttu-id="0395a-114">Specifica-nome per restituirne uno specifico.</span><span class="sxs-lookup"><span data-stu-id="0395a-114">Specify -Name to return a specific one.</span></span>

## <span data-ttu-id="0395a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0395a-115">PARAMETERS</span></span>

### <span data-ttu-id="0395a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0395a-116">-DefaultProfile</span></span>
<span data-ttu-id="0395a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0395a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0395a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="0395a-118">-Name</span></span>
<span data-ttu-id="0395a-119">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="0395a-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0395a-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0395a-120">-ParentObject</span></span>
<span data-ttu-id="0395a-121">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="0395a-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0395a-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="0395a-122">-ParentResourceId</span></span>
<span data-ttu-id="0395a-123">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="0395a-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0395a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0395a-124">-ResourceGroupName</span></span>
<span data-ttu-id="0395a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0395a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0395a-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0395a-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="0395a-127">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0395a-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0395a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0395a-128">CommonParameters</span></span>
<span data-ttu-id="0395a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0395a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0395a-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0395a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0395a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0395a-131">INPUTS</span></span>

### <span data-ttu-id="0395a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0395a-132">System.String</span></span>

### <span data-ttu-id="0395a-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0395a-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="0395a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0395a-134">OUTPUTS</span></span>

### <span data-ttu-id="0395a-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0395a-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="0395a-136">Note</span><span class="sxs-lookup"><span data-stu-id="0395a-136">NOTES</span></span>

## <span data-ttu-id="0395a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0395a-137">RELATED LINKS</span></span>
