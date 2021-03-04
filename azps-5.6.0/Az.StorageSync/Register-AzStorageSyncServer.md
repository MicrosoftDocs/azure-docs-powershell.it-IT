---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: 62dcefcf48e1d4c685b2a4f4855af41da7d8db75
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011325"
---
# <span data-ttu-id="b4d4d-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b4d4d-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="b4d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="b4d4d-103">Questo comando registra un server in un servizio di sincronizzazione di archiviazione che crea una relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="b4d4d-104">PowerShell o il portale di Azure possono quindi essere usati per configurare la sincronizzazione in questo server.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="b4d4d-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b4d4d-105">SYNTAX</span></span>

### <span data-ttu-id="b4d4d-106">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="b4d4d-106">StringParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d4d-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d4d-107">ObjectParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4d4d-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4d4d-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4d4d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b4d4d-109">DESCRIPTION</span></span>
<span data-ttu-id="b4d4d-110">Questo comando registra un server in un servizio di sincronizzazione di archiviazione, la risorsa principale per Azure File Sync. Viene creata una relazione di trust tra il server e il servizio di sincronizzazione di archiviazione che assicura canali sicuri di trasferimento e gestione dei dati.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="b4d4d-111">PowerShell o il portale di Azure possono quindi essere usati per configurare le sincronizzazioni in questo server.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="b4d4d-112">Un server può essere registrato solo con un singolo servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="b4d4d-113">Se i server devono partecipare alla sincronizzazione dello stesso set di file, registrarli nello stesso servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="b4d4d-114">Il comando deve essere eseguito in locale nel server che deve essere registrato: viene eseguito direttamente o tramite una sessione remota di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="b4d4d-115">Un oggetto computer remoto non può essere accettato.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="b4d4d-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b4d4d-116">EXAMPLES</span></span>

### <span data-ttu-id="b4d4d-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b4d4d-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b4d4d-118">Questo comando registrerà il server locale su cui viene eseguito questo comando.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="b4d4d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4d4d-119">PARAMETERS</span></span>

### <span data-ttu-id="b4d4d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b4d4d-120">-AsJob</span></span>
<span data-ttu-id="b4d4d-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b4d4d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b4d4d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4d4d-122">-DefaultProfile</span></span>
<span data-ttu-id="b4d4d-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4d4d-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4d4d-124">-ParentObject</span></span>
<span data-ttu-id="b4d4d-125">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b4d4d-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b4d4d-126">-ParentResourceId</span></span>
<span data-ttu-id="b4d4d-127">ID risorsa padre StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b4d4d-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="b4d4d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4d4d-128">-ResourceGroupName</span></span>
<span data-ttu-id="b4d4d-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b4d4d-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b4d4d-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="b4d4d-131">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b4d4d-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4d4d-132">-Confirm</span></span>
<span data-ttu-id="b4d4d-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4d4d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4d4d-134">-WhatIf</span></span>
<span data-ttu-id="b4d4d-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4d4d-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4d4d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4d4d-137">CommonParameters</span></span>
<span data-ttu-id="b4d4d-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4d4d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4d4d-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4d4d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4d4d-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="b4d4d-140">INPUTS</span></span>

### <span data-ttu-id="b4d4d-141">System.String</span><span class="sxs-lookup"><span data-stu-id="b4d4d-141">System.String</span></span>

### <span data-ttu-id="b4d4d-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="b4d4d-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b4d4d-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b4d4d-143">OUTPUTS</span></span>

### <span data-ttu-id="b4d4d-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b4d4d-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="b4d4d-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="b4d4d-145">NOTES</span></span>

## <span data-ttu-id="b4d4d-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b4d4d-146">RELATED LINKS</span></span>
