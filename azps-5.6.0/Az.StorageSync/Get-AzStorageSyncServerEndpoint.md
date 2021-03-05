---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 81baab4f996d7a56b64f055f94a18c09b4305991
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973149"
---
# <span data-ttu-id="9de3b-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9de3b-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="9de3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9de3b-102">SYNOPSIS</span></span>
<span data-ttu-id="9de3b-103">Questo comando elenca tutti gli endpoint del server all'interno di un determinato gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9de3b-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="9de3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9de3b-104">SYNTAX</span></span>

### <span data-ttu-id="9de3b-105">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="9de3b-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de3b-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de3b-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9de3b-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9de3b-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9de3b-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9de3b-108">DESCRIPTION</span></span>
<span data-ttu-id="9de3b-109">Questo comando elenca tutti gli endpoint del server all'interno di un determinato gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9de3b-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="9de3b-110">Può essere usato per elencare anche gli attributi di ogni endpoint server.</span><span class="sxs-lookup"><span data-stu-id="9de3b-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="9de3b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9de3b-111">EXAMPLES</span></span>

### <span data-ttu-id="9de3b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9de3b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="9de3b-113">Questo comando recupera tutti gli endpoint del server contenuti nel gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="9de3b-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="9de3b-114">Specificare -ServerEndpointName per restituire un nome specifico.</span><span class="sxs-lookup"><span data-stu-id="9de3b-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="9de3b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9de3b-115">PARAMETERS</span></span>

### <span data-ttu-id="9de3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de3b-116">-DefaultProfile</span></span>
<span data-ttu-id="9de3b-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9de3b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9de3b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9de3b-118">-Name</span></span>
<span data-ttu-id="9de3b-119">Nome dell'endpoint del server.</span><span class="sxs-lookup"><span data-stu-id="9de3b-119">Name of the server endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9de3b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9de3b-120">-ParentObject</span></span>
<span data-ttu-id="9de3b-121">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="9de3b-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9de3b-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9de3b-122">-ParentResourceId</span></span>
<span data-ttu-id="9de3b-123">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="9de3b-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="9de3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="9de3b-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9de3b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="9de3b-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9de3b-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="9de3b-127">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="9de3b-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9de3b-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9de3b-128">-SyncGroupName</span></span>
<span data-ttu-id="9de3b-129">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9de3b-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9de3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de3b-130">CommonParameters</span></span>
<span data-ttu-id="9de3b-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de3b-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9de3b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de3b-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="9de3b-133">INPUTS</span></span>

### <span data-ttu-id="9de3b-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="9de3b-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="9de3b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="9de3b-135">System.String</span></span>

## <span data-ttu-id="9de3b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9de3b-136">OUTPUTS</span></span>

### <span data-ttu-id="9de3b-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9de3b-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="9de3b-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="9de3b-138">NOTES</span></span>

## <span data-ttu-id="9de3b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9de3b-139">RELATED LINKS</span></span>
