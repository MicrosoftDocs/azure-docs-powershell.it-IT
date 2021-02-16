---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183071"
---
# <span data-ttu-id="58174-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="58174-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="58174-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58174-102">SYNOPSIS</span></span>
<span data-ttu-id="58174-103">Questo comando imposta il servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58174-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="58174-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58174-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58174-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="58174-105">DESCRIPTION</span></span>
<span data-ttu-id="58174-106">Un servizio di sincronizzazione dell'archiviazione è la risorsa principale per Sincronizzazione file di Azure. Questo comando imposta il servizio di sincronizzazione dello spazio di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58174-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="58174-107">È consigliabile creare tutti i servizi di sincronizzazione di archiviazione assolutamente necessari per distinguere diversi gruppi di server nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="58174-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="58174-108">Un servizio di sincronizzazione di archiviazione contiene gruppi di sincronizzazione e funziona anche come destinazione per la registrazione dei server.</span><span class="sxs-lookup"><span data-stu-id="58174-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="58174-109">Un server può essere registrato solo con un singolo servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="58174-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="58174-110">Se i server devono partecipare alla sincronizzazione dello stesso set di file, registrarli nello stesso servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="58174-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="58174-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58174-111">EXAMPLES</span></span>

### <span data-ttu-id="58174-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58174-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="58174-113">Questo comando imposta un servizio di sincronizzazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="58174-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="58174-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58174-114">PARAMETERS</span></span>

### <span data-ttu-id="58174-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58174-115">-DefaultProfile</span></span>
<span data-ttu-id="58174-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58174-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="58174-117">-Name</span><span class="sxs-lookup"><span data-stu-id="58174-117">-Name</span></span>
<span data-ttu-id="58174-118">Nome del servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="58174-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="58174-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58174-119">-ResourceGroupName</span></span>
<span data-ttu-id="58174-120">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58174-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="58174-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="58174-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="58174-122">IncomingTrafficPolicy del servizio di sincronizzazione di archiviazione</span><span class="sxs-lookup"><span data-stu-id="58174-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="58174-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="58174-123">-Tag</span></span>
<span data-ttu-id="58174-124">Tag del servizio di sincronizzazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="58174-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58174-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58174-125">-Confirm</span></span>
<span data-ttu-id="58174-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58174-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58174-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58174-127">-WhatIf</span></span>
<span data-ttu-id="58174-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58174-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58174-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58174-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58174-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58174-130">CommonParameters</span></span>
<span data-ttu-id="58174-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58174-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58174-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58174-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58174-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="58174-133">INPUTS</span></span>

### <span data-ttu-id="58174-134">System.String</span><span class="sxs-lookup"><span data-stu-id="58174-134">System.String</span></span>

## <span data-ttu-id="58174-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58174-135">OUTPUTS</span></span>

### <span data-ttu-id="58174-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="58174-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="58174-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="58174-137">NOTES</span></span>

## <span data-ttu-id="58174-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58174-138">RELATED LINKS</span></span>
