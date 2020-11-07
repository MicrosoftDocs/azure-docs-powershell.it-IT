---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: decf935cd61c052e2e77dd8fd2eadacd7a548974
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676463"
---
# <span data-ttu-id="144df-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="144df-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="144df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="144df-102">SYNOPSIS</span></span>
<span data-ttu-id="144df-103">Questo comando elenca tutti gli endpoint del cloud all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="144df-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="144df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="144df-104">SYNTAX</span></span>

### <span data-ttu-id="144df-105">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="144df-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="144df-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="144df-106">StringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="144df-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="144df-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="144df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="144df-108">DESCRIPTION</span></span>
<span data-ttu-id="144df-109">Questo comando elenca tutti gli endpoint del cloud all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="144df-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="144df-110">Può essere usato anche per elencare gli attributi di ogni endpoint del cloud.</span><span class="sxs-lookup"><span data-stu-id="144df-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="144df-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="144df-111">EXAMPLES</span></span>

### <span data-ttu-id="144df-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="144df-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="144df-113">Questo comando consente di ottenere tutti gli endpoint del cloud contenuti nel gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="144df-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="144df-114">Specifica-CloudEndpointName per restituirne uno specifico.</span><span class="sxs-lookup"><span data-stu-id="144df-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="144df-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="144df-115">PARAMETERS</span></span>

### <span data-ttu-id="144df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144df-116">-DefaultProfile</span></span>
<span data-ttu-id="144df-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="144df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="144df-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="144df-118">-Name</span></span>
<span data-ttu-id="144df-119">Nome della CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="144df-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="144df-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="144df-120">-ParentObject</span></span>
<span data-ttu-id="144df-121">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="144df-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="144df-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="144df-122">-ParentResourceId</span></span>
<span data-ttu-id="144df-123">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="144df-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="144df-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="144df-124">-ResourceGroupName</span></span>
<span data-ttu-id="144df-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="144df-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="144df-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="144df-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="144df-127">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="144df-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="144df-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="144df-128">-SyncGroupName</span></span>
<span data-ttu-id="144df-129">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="144df-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="144df-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144df-130">CommonParameters</span></span>
<span data-ttu-id="144df-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="144df-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144df-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="144df-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144df-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="144df-133">INPUTS</span></span>

### <span data-ttu-id="144df-134">System. String</span><span class="sxs-lookup"><span data-stu-id="144df-134">System.String</span></span>

### <span data-ttu-id="144df-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="144df-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="144df-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="144df-136">OUTPUTS</span></span>

### <span data-ttu-id="144df-137">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="144df-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="144df-138">Note</span><span class="sxs-lookup"><span data-stu-id="144df-138">NOTES</span></span>

## <span data-ttu-id="144df-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="144df-139">RELATED LINKS</span></span>
