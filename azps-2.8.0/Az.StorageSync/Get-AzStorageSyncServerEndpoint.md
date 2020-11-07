---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 1f6692067c48cc093e7d74d75c678374aba30f24
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857777"
---
# <span data-ttu-id="693ec-101">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="693ec-101">Get-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="693ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="693ec-102">SYNOPSIS</span></span>
<span data-ttu-id="693ec-103">Questo comando elenca tutti gli endpoint del server all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="693ec-103">This command lists all server endpoints within a given sync group.</span></span>

## <span data-ttu-id="693ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="693ec-104">SYNTAX</span></span>

### <span data-ttu-id="693ec-105">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="693ec-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="693ec-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="693ec-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="693ec-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="693ec-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServerEndpoint [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="693ec-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="693ec-108">DESCRIPTION</span></span>
<span data-ttu-id="693ec-109">Questo comando elenca tutti gli endpoint del server all'interno di un gruppo di sincronizzazione specifico.</span><span class="sxs-lookup"><span data-stu-id="693ec-109">This command lists all server endpoints within a given sync group.</span></span> <span data-ttu-id="693ec-110">Può essere usato anche per elencare gli attributi di ogni endpoint server.</span><span class="sxs-lookup"><span data-stu-id="693ec-110">It can be used to also list the attributes of each server endpoint.</span></span>

## <span data-ttu-id="693ec-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="693ec-111">EXAMPLES</span></span>

### <span data-ttu-id="693ec-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="693ec-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName"
```

<span data-ttu-id="693ec-113">Questo comando consente di ottenere tutti gli endpoint del server contenuti nel gruppo di sincronizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="693ec-113">This command gets all server endpoints contained within the specified sync group.</span></span> <span data-ttu-id="693ec-114">Specifica-ServerEndpointName per restituirne uno specifico.</span><span class="sxs-lookup"><span data-stu-id="693ec-114">Specify -ServerEndpointName to return a specific one.</span></span>

## <span data-ttu-id="693ec-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="693ec-115">PARAMETERS</span></span>

### <span data-ttu-id="693ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="693ec-116">-DefaultProfile</span></span>
<span data-ttu-id="693ec-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="693ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="693ec-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="693ec-118">-Name</span></span>
<span data-ttu-id="693ec-119">Nome dell'endpoint server.</span><span class="sxs-lookup"><span data-stu-id="693ec-119">Name of the server endpoint.</span></span>

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

### <span data-ttu-id="693ec-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="693ec-120">-ParentObject</span></span>
<span data-ttu-id="693ec-121">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="693ec-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="693ec-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="693ec-122">-ParentResourceId</span></span>
<span data-ttu-id="693ec-123">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="693ec-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="693ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="693ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="693ec-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="693ec-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="693ec-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="693ec-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="693ec-127">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="693ec-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="693ec-128">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="693ec-128">-SyncGroupName</span></span>
<span data-ttu-id="693ec-129">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="693ec-129">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="693ec-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="693ec-130">CommonParameters</span></span>
<span data-ttu-id="693ec-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="693ec-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="693ec-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="693ec-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="693ec-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="693ec-133">INPUTS</span></span>

### <span data-ttu-id="693ec-134">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="693ec-134">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="693ec-135">System. String</span><span class="sxs-lookup"><span data-stu-id="693ec-135">System.String</span></span>

## <span data-ttu-id="693ec-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="693ec-136">OUTPUTS</span></span>

### <span data-ttu-id="693ec-137">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="693ec-137">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="693ec-138">Note</span><span class="sxs-lookup"><span data-stu-id="693ec-138">NOTES</span></span>

## <span data-ttu-id="693ec-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="693ec-139">RELATED LINKS</span></span>
