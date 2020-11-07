---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676442"
---
# <span data-ttu-id="c836e-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="c836e-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="c836e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c836e-102">SYNOPSIS</span></span>
<span data-ttu-id="c836e-103">Questo comando registra un server in un servizio di sincronizzazione dello spazio di archiviazione che crea una relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="c836e-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="c836e-104">PowerShell o Azure Portal possono quindi essere usati per configurare la sincronizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="c836e-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="c836e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c836e-105">SYNTAX</span></span>

### <span data-ttu-id="c836e-106">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c836e-106">ObjectParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c836e-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c836e-107">StringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c836e-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c836e-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c836e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c836e-109">DESCRIPTION</span></span>
<span data-ttu-id="c836e-110">Questo comando registra un server in un servizio di sincronizzazione dello spazio di archiviazione, la risorsa di primo livello per la sincronizzazione dei file di Azure. Viene creata una relazione di trust tra il servizio di sincronizzazione del server e dello storage che garantisce i canali di gestione e trasferimento dati sicuri.</span><span class="sxs-lookup"><span data-stu-id="c836e-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="c836e-111">PowerShell o Azure Portal possono quindi essere usati per configurare le sincronizzazioni su questo server.</span><span class="sxs-lookup"><span data-stu-id="c836e-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="c836e-112">Un server può essere registrato solo in un singolo servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c836e-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="c836e-113">Se i server devono sempre partecipare alla sincronizzazione dello stesso set di file, registrarli nello stesso servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c836e-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="c836e-114">Il comando deve essere eseguito localmente nel server da registrare, eseguito direttamente o tramite una sessione remota di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c836e-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="c836e-115">Non è possibile accettare un oggetto computer remoto.</span><span class="sxs-lookup"><span data-stu-id="c836e-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="c836e-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c836e-116">EXAMPLES</span></span>

### <span data-ttu-id="c836e-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c836e-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="c836e-118">Questo comando registrerà il server locale in cui viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="c836e-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="c836e-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c836e-119">PARAMETERS</span></span>

### <span data-ttu-id="c836e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c836e-120">-AsJob</span></span>
<span data-ttu-id="c836e-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c836e-121">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c836e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c836e-122">-DefaultProfile</span></span>
<span data-ttu-id="c836e-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c836e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c836e-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c836e-124">-ParentObject</span></span>
<span data-ttu-id="c836e-125">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="c836e-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="c836e-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c836e-126">-ParentResourceId</span></span>
<span data-ttu-id="c836e-127">ID risorsa padre di StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c836e-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="c836e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c836e-128">-ResourceGroupName</span></span>
<span data-ttu-id="c836e-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c836e-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="c836e-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="c836e-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="c836e-131">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="c836e-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="c836e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c836e-132">CommonParameters</span></span>
<span data-ttu-id="c836e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c836e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c836e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c836e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c836e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c836e-135">INPUTS</span></span>

### <span data-ttu-id="c836e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c836e-136">System.String</span></span>

### <span data-ttu-id="c836e-137">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="c836e-137">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="c836e-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c836e-138">OUTPUTS</span></span>

### <span data-ttu-id="c836e-139">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="c836e-139">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="c836e-140">Note</span><span class="sxs-lookup"><span data-stu-id="c836e-140">NOTES</span></span>

## <span data-ttu-id="c836e-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c836e-141">RELATED LINKS</span></span>
