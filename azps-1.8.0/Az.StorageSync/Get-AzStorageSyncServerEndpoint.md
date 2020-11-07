---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: b71da416d7609f05d4716090dc8f09bf0ec0b084
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676458"
---
# <span data-ttu-id="40b5b-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40b5b-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="40b5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40b5b-102">SYNOPSIS</span></span>
<span data-ttu-id="40b5b-103">Questo comando elenca tutti gli endpoint del server all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="40b5b-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="40b5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40b5b-104">SYNTAX</span></span>

### <span data-ttu-id="40b5b-105">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="40b5b-105">ObjectParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b5b-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="40b5b-106">StringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b5b-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="40b5b-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40b5b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40b5b-108">DESCRIPTION</span></span>
<span data-ttu-id="40b5b-109">Questo comando elenca tutti gli endpoint del server all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="40b5b-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="40b5b-110">Può essere usato anche per elencare gli attributi di ogni endpoint server.</span><span class="sxs-lookup"><span data-stu-id="40b5b-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="40b5b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40b5b-111">EXAMPLES</span></span>

### <span data-ttu-id="40b5b-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="40b5b-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="40b5b-113">Questo comando consente di ottenere tutti gli endpoint del server contenuti nel gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="40b5b-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="40b5b-114">Specifica-ServerEndpointName per restituirne uno specifico.</span><span class="sxs-lookup"><span data-stu-id="40b5b-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="40b5b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40b5b-115">PARAMETERS</span></span>

### <span data-ttu-id="40b5b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b5b-116">-DefaultProfile</span></span>
<span data-ttu-id="40b5b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40b5b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b5b-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="40b5b-118">-Name</span></span>
<span data-ttu-id="40b5b-119">Nome dell'endpoint server.</span><span class="sxs-lookup"><span data-stu-id="40b5b-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="40b5b-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40b5b-120">-ParentObject</span></span>
<span data-ttu-id="40b5b-121">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="40b5b-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="40b5b-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="40b5b-122">-ParentResourceId</span></span>
<span data-ttu-id="40b5b-123">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="40b5b-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="40b5b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b5b-124">-ResourceGroupName</span></span>
<span data-ttu-id="40b5b-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="40b5b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="40b5b-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="40b5b-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="40b5b-127">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="40b5b-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="40b5b-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="40b5b-128">-SyncGroupName</span></span>
<span data-ttu-id="40b5b-129">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="40b5b-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="40b5b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b5b-130">CommonParameters</span></span>
<span data-ttu-id="40b5b-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40b5b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b5b-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40b5b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b5b-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40b5b-133">INPUTS</span></span>

### <span data-ttu-id="40b5b-134">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="40b5b-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="40b5b-135">System. String</span><span class="sxs-lookup"><span data-stu-id="40b5b-135">System.String</span></span>

## <span data-ttu-id="40b5b-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40b5b-136">OUTPUTS</span></span>

### <span data-ttu-id="40b5b-137">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="40b5b-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="40b5b-138">Note</span><span class="sxs-lookup"><span data-stu-id="40b5b-138">NOTES</span></span>

## <span data-ttu-id="40b5b-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40b5b-139">RELATED LINKS</span></span>
