---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncGroup.md
ms.openlocfilehash: 34f4dc1933e755167333d12d4566838ea47c26b1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676446"
---
# <span data-ttu-id="ced0a-101">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ced0a-101">New-AzStorageSyncGroup</span></span>

## <span data-ttu-id="ced0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ced0a-102">SYNOPSIS</span></span>
<span data-ttu-id="ced0a-103">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ced0a-103">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ced0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ced0a-104">SYNTAX</span></span>

### <span data-ttu-id="ced0a-105">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ced0a-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncGroup [-ParentObject] <PSStorageSyncService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ced0a-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced0a-106">StringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ced0a-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="ced0a-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncGroup [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ced0a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ced0a-108">DESCRIPTION</span></span>
<span data-ttu-id="ced0a-109">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ced0a-109">This command creates a new sync group within a specified storage sync service.</span></span> <span data-ttu-id="ced0a-110">Viene usato un gruppo di sincronizzazione per descrivere una topologia di percorsi, denominati endpoint, che sincronizzano tutti i file archiviati in uno degli endpoint.</span><span class="sxs-lookup"><span data-stu-id="ced0a-110">A sync group is used to describe a topology of locations, referred to as endpoints, that will sync any files stored within any one of the endpoints.</span></span> <span data-ttu-id="ced0a-111">Un gruppo di sincronizzazione contiene endpoint di tipo cloud, che fanno riferimento a condivisioni di file Azure e contiene anche endpoint server che fanno riferimento a un percorso locale specifico in un server registrato.</span><span class="sxs-lookup"><span data-stu-id="ced0a-111">A sync group contains cloud endpoints, which reference Azure file shares, and it also contains server endpoints which reference a specific local path on a registered server.</span></span>

## <span data-ttu-id="ced0a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ced0a-112">EXAMPLES</span></span>

### <span data-ttu-id="ced0a-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ced0a-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncGroup -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="ced0a-114">Questo comando crea un nuovo gruppo di sincronizzazione all'interno di un servizio di sincronizzazione dello spazio di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="ced0a-114">This command creates a new sync group within a specified storage sync service.</span></span>

## <span data-ttu-id="ced0a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ced0a-115">PARAMETERS</span></span>

### <span data-ttu-id="ced0a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ced0a-116">-DefaultProfile</span></span>
<span data-ttu-id="ced0a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ced0a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ced0a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="ced0a-118">-Name</span></span>
<span data-ttu-id="ced0a-119">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="ced0a-119">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ced0a-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ced0a-120">-ParentObject</span></span>
<span data-ttu-id="ced0a-121">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="ced0a-121">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="ced0a-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ced0a-122">-ParentResourceId</span></span>
<span data-ttu-id="ced0a-123">ID risorsa padre di StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ced0a-123">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="ced0a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ced0a-124">-ResourceGroupName</span></span>
<span data-ttu-id="ced0a-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ced0a-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ced0a-126">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ced0a-126">-StorageSyncServiceName</span></span>
<span data-ttu-id="ced0a-127">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ced0a-127">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ced0a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ced0a-128">CommonParameters</span></span>
<span data-ttu-id="ced0a-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ced0a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ced0a-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ced0a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ced0a-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ced0a-131">INPUTS</span></span>

### <span data-ttu-id="ced0a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ced0a-132">System.String</span></span>

### <span data-ttu-id="ced0a-133">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="ced0a-133">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="ced0a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ced0a-134">OUTPUTS</span></span>

### <span data-ttu-id="ced0a-135">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ced0a-135">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

## <span data-ttu-id="ced0a-136">Note</span><span class="sxs-lookup"><span data-stu-id="ced0a-136">NOTES</span></span>

## <span data-ttu-id="ced0a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ced0a-137">RELATED LINKS</span></span>
