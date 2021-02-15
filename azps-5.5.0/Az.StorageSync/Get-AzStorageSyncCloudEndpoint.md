---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 076a1393365e93a8008f15137d078a49491d81f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183119"
---
# <span data-ttu-id="a68dc-101">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68dc-101">Get-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="a68dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a68dc-102">SYNOPSIS</span></span>
<span data-ttu-id="a68dc-103">Questo comando elenca tutti gli endpoint cloud all'interno di un determinato gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a68dc-103">This command lists all cloud endpoints within a given sync group.</span></span>

## <span data-ttu-id="a68dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a68dc-104">SYNTAX</span></span>

### <span data-ttu-id="a68dc-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="a68dc-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a68dc-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a68dc-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a68dc-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a68dc-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a68dc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a68dc-108">DESCRIPTION</span></span>
<span data-ttu-id="a68dc-109">Questo comando elenca tutti gli endpoint cloud all'interno di un determinato gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a68dc-109">This command lists all cloud endpoints within a given sync group.</span></span> <span data-ttu-id="a68dc-110">Può essere usato per elencare anche gli attributi di ogni endpoint cloud.</span><span class="sxs-lookup"><span data-stu-id="a68dc-110">It can be used to also list the attributes of each cloud endpoint.</span></span>

## <span data-ttu-id="a68dc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a68dc-111">EXAMPLES</span></span>

### <span data-ttu-id="a68dc-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a68dc-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="a68dc-113">Questo comando recupera tutti gli endpoint cloud contenuti nel gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="a68dc-113">This command gets all cloud endpoints contained within the specified sync group.</span></span> <span data-ttu-id="a68dc-114">Specificare -CloudEndpointName per restituire un nome specifico.</span><span class="sxs-lookup"><span data-stu-id="a68dc-114">Specify -CloudEndpointName to return a specific one.</span></span>

## <span data-ttu-id="a68dc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a68dc-115">PARAMETERS</span></span>

### <span data-ttu-id="a68dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a68dc-116">-DefaultProfile</span></span>
<span data-ttu-id="a68dc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a68dc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a68dc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a68dc-118">-Name</span></span>
<span data-ttu-id="a68dc-119">Nome di CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a68dc-119">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="a68dc-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a68dc-120">-ParentObject</span></span>
<span data-ttu-id="a68dc-121">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="a68dc-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a68dc-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a68dc-122">-ParentResourceId</span></span>
<span data-ttu-id="a68dc-123">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="a68dc-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="a68dc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a68dc-124">-ResourceGroupName</span></span>
<span data-ttu-id="a68dc-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a68dc-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a68dc-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="a68dc-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="a68dc-127">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a68dc-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="a68dc-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="a68dc-128">-SyncGroupName</span></span>
<span data-ttu-id="a68dc-129">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="a68dc-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="a68dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a68dc-130">CommonParameters</span></span>
<span data-ttu-id="a68dc-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a68dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a68dc-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a68dc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a68dc-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="a68dc-133">INPUTS</span></span>

### <span data-ttu-id="a68dc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="a68dc-134">System.String</span></span>

### <span data-ttu-id="a68dc-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="a68dc-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="a68dc-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a68dc-136">OUTPUTS</span></span>

### <span data-ttu-id="a68dc-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="a68dc-137">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="a68dc-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="a68dc-138">NOTES</span></span>

## <span data-ttu-id="a68dc-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a68dc-139">RELATED LINKS</span></span>
