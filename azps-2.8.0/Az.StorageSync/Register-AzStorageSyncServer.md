---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: ffcce1b3e5575099875ed15f8e76a8ca9f9c4418
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858329"
---
# <span data-ttu-id="7c9c1-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="7c9c1-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="7c9c1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="7c9c1-103">Questo comando registra un server in un servizio di sincronizzazione dello spazio di archiviazione che crea una relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="7c9c1-104">PowerShell o Azure Portal possono quindi essere usati per configurare la sincronizzazione nel server.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="7c9c1-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c9c1-105">SYNTAX</span></span>

### <span data-ttu-id="7c9c1-106">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c9c1-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c9c1-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c9c1-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c9c1-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="7c9c1-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c9c1-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c9c1-109">DESCRIPTION</span></span>
<span data-ttu-id="7c9c1-110">Questo comando registra un server in un servizio di sincronizzazione dello spazio di archiviazione, la risorsa di primo livello per la sincronizzazione dei file di Azure. Viene creata una relazione di trust tra il servizio di sincronizzazione del server e dello storage che garantisce i canali di gestione e trasferimento dati sicuri.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="7c9c1-111">PowerShell o Azure Portal possono quindi essere usati per configurare le sincronizzazioni su questo server.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="7c9c1-112">Un server può essere registrato solo in un singolo servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="7c9c1-113">Se i server devono sempre partecipare alla sincronizzazione dello stesso set di file, registrarli nello stesso servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="7c9c1-114">Il comando deve essere eseguito localmente nel server da registrare, eseguito direttamente o tramite una sessione remota di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="7c9c1-115">Non è possibile accettare un oggetto computer remoto.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="7c9c1-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c9c1-116">EXAMPLES</span></span>

### <span data-ttu-id="7c9c1-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c9c1-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="7c9c1-118">Questo comando registrerà il server locale in cui viene eseguito il comando.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="7c9c1-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c9c1-119">PARAMETERS</span></span>

### <span data-ttu-id="7c9c1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c9c1-120">-AsJob</span></span>
<span data-ttu-id="7c9c1-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7c9c1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c9c1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c9c1-122">-DefaultProfile</span></span>
<span data-ttu-id="7c9c1-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c9c1-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="7c9c1-124">-ParentObject</span></span>
<span data-ttu-id="7c9c1-125">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="7c9c1-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="7c9c1-126">-ParentResourceId</span></span>
<span data-ttu-id="7c9c1-127">ID risorsa padre di StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7c9c1-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="7c9c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c9c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="7c9c1-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="7c9c1-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="7c9c1-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="7c9c1-131">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="7c9c1-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c9c1-132">-Confirm</span></span>
<span data-ttu-id="7c9c1-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9c1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c9c1-134">-WhatIf</span></span>
<span data-ttu-id="7c9c1-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c9c1-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c9c1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c9c1-137">CommonParameters</span></span>
<span data-ttu-id="7c9c1-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c9c1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c9c1-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c9c1-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c9c1-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c9c1-140">INPUTS</span></span>

### <span data-ttu-id="7c9c1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7c9c1-141">System.String</span></span>

### <span data-ttu-id="7c9c1-142">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="7c9c1-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="7c9c1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c9c1-143">OUTPUTS</span></span>

### <span data-ttu-id="7c9c1-144">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="7c9c1-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="7c9c1-145">Note</span><span class="sxs-lookup"><span data-stu-id="7c9c1-145">NOTES</span></span>

## <span data-ttu-id="7c9c1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c9c1-146">RELATED LINKS</span></span>
