---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: d2d18a908b53c9a8ab077671b7e2026516d40b17
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676444"
---
# <span data-ttu-id="b041d-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b041d-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="b041d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b041d-102">SYNOPSIS</span></span>
<span data-ttu-id="b041d-103">Questo comando crea un nuovo servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b041d-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="b041d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b041d-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b041d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b041d-105">DESCRIPTION</span></span>
<span data-ttu-id="b041d-106">Un servizio di sincronizzazione dello spazio di archiviazione è la risorsa di primo livello per la sincronizzazione di file Azure. Questo comando crea un nuovo servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b041d-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="b041d-107">È consigliabile creare il numero di servizi di sincronizzazione dello spazio di archiviazione necessari per distinguere i gruppi distinti di server dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="b041d-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="b041d-108">Un servizio di sincronizzazione dello spazio di archiviazione contiene gruppi di sincronizzazione e funziona anche come destinazione per la registrazione dei server.</span><span class="sxs-lookup"><span data-stu-id="b041d-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="b041d-109">Un server può essere registrato solo in un singolo servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b041d-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="b041d-110">Se i server devono sempre partecipare alla sincronizzazione dello stesso set di file, registrarli nello stesso servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b041d-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="b041d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b041d-111">EXAMPLES</span></span>

### <span data-ttu-id="b041d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b041d-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b041d-113">Questo comando creerà un servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b041d-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="b041d-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b041d-114">PARAMETERS</span></span>

### <span data-ttu-id="b041d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b041d-115">-DefaultProfile</span></span>
<span data-ttu-id="b041d-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b041d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b041d-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b041d-117">-Location</span></span>
<span data-ttu-id="b041d-118">Posizione del servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b041d-118">Storage Sync Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b041d-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b041d-119">-Name</span></span>
<span data-ttu-id="b041d-120">Nome del servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b041d-120">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b041d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b041d-121">-ResourceGroupName</span></span>
<span data-ttu-id="b041d-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b041d-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b041d-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="b041d-123">-Tag</span></span>
<span data-ttu-id="b041d-124">Tag del servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b041d-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b041d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b041d-125">CommonParameters</span></span>
<span data-ttu-id="b041d-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b041d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b041d-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b041d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b041d-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b041d-128">INPUTS</span></span>

### <span data-ttu-id="b041d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b041d-129">System.String</span></span>

## <span data-ttu-id="b041d-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b041d-130">OUTPUTS</span></span>

### <span data-ttu-id="b041d-131">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b041d-131">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b041d-132">Note</span><span class="sxs-lookup"><span data-stu-id="b041d-132">NOTES</span></span>

## <span data-ttu-id="b041d-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b041d-133">RELATED LINKS</span></span>
