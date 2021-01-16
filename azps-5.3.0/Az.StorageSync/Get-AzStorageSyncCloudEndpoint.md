---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375927"
---
# <span data-ttu-id="b0779-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0779-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="b0779-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0779-102">SYNOPSIS</span></span>
<span data-ttu-id="b0779-103">Questo comando elenca tutti gli endpoint del cloud all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="b0779-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="b0779-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0779-104">SYNTAX</span></span>

### <span data-ttu-id="b0779-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b0779-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0779-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0779-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0779-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b0779-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0779-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0779-108">DESCRIPTION</span></span>
<span data-ttu-id="b0779-109">Questo comando elenca tutti gli endpoint del cloud all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="b0779-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="b0779-110">Può essere usato anche per elencare gli attributi di ogni endpoint del cloud.</span><span class="sxs-lookup"><span data-stu-id="b0779-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="b0779-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0779-111">EXAMPLES</span></span>

### <span data-ttu-id="b0779-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0779-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="b0779-113">Questo comando consente di ottenere tutti gli endpoint del cloud contenuti nel gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="b0779-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="b0779-114">Specifica-CloudEndpointName per restituirne uno specifico.</span><span class="sxs-lookup"><span data-stu-id="b0779-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="b0779-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0779-115">PARAMETERS</span></span>

### <span data-ttu-id="b0779-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0779-116">-DefaultProfile</span></span>
<span data-ttu-id="b0779-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0779-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0779-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0779-118">-Name</span></span>
<span data-ttu-id="b0779-119">Nome della CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b0779-119">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0779-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b0779-120">-ParentObject</span></span>
<span data-ttu-id="b0779-121">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="b0779-121">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0779-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b0779-122">-ParentResourceId</span></span>
<span data-ttu-id="b0779-123">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="b0779-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0779-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0779-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0779-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b0779-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="b0779-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b0779-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="b0779-127">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b0779-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b0779-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b0779-128">-SyncGroupName</span></span>
<span data-ttu-id="b0779-129">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="b0779-129">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0779-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0779-130">CommonParameters</span></span>
<span data-ttu-id="b0779-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0779-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0779-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0779-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0779-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0779-133">INPUTS</span></span>

### <span data-ttu-id="b0779-134">System. String</span><span class="sxs-lookup"><span data-stu-id="b0779-134">System.String</span></span>

### <span data-ttu-id="b0779-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b0779-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="b0779-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0779-136">OUTPUTS</span></span>

### <span data-ttu-id="b0779-137">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b0779-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="b0779-138">Note</span><span class="sxs-lookup"><span data-stu-id="b0779-138">NOTES</span></span>

## <span data-ttu-id="b0779-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0779-139">RELATED LINKS</span></span>
