---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncService.md
ms.openlocfilehash: c24bf60171e152985fb13204f23082f94f8c7ff0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011358"
---
# <span data-ttu-id="2e40d-101">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2e40d-101">New-AzStorageSyncService</span></span>

## <span data-ttu-id="2e40d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e40d-102">SYNOPSIS</span></span>
<span data-ttu-id="2e40d-103">Questo comando crea un nuovo servizio di sincronizzazione di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e40d-103">This command creates a new storage sync service in a resource group.</span></span>

## <span data-ttu-id="2e40d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2e40d-104">SYNTAX</span></span>

```
New-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-IncomingTrafficPolicy] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e40d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2e40d-105">DESCRIPTION</span></span>
<span data-ttu-id="2e40d-106">Un servizio di sincronizzazione dello spazio di archiviazione è la risorsa principale per Azure File Sync. Questo comando crea un nuovo servizio di sincronizzazione di archiviazione in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e40d-106">A storage sync service is the top level resource for Azure File Sync. This command creates a new storage sync service in a resource group.</span></span> <span data-ttu-id="2e40d-107">È consigliabile creare tutti i servizi di sincronizzazione di archiviazione assolutamente necessari per distinguere diversi gruppi di server nell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="2e40d-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="2e40d-108">Un servizio di sincronizzazione di archiviazione contiene gruppi di sincronizzazione e funziona anche come destinazione per registrare i server.</span><span class="sxs-lookup"><span data-stu-id="2e40d-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="2e40d-109">Un server può essere registrato solo con un singolo servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e40d-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="2e40d-110">Se i server devono partecipare alla sincronizzazione dello stesso set di file, registrarli nello stesso servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e40d-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="2e40d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2e40d-111">EXAMPLES</span></span>

### <span data-ttu-id="2e40d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2e40d-112">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncService -ResourceGroupName "myResourceGroup" -Location "myLocation" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="2e40d-113">Questo comando crea un servizio di sincronizzazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e40d-113">This command will create a storage sync service.</span></span>

## <span data-ttu-id="2e40d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e40d-114">PARAMETERS</span></span>

### <span data-ttu-id="2e40d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e40d-115">-DefaultProfile</span></span>
<span data-ttu-id="2e40d-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2e40d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e40d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="2e40d-117">-Location</span></span>
<span data-ttu-id="2e40d-118">Posizione del servizio di sincronizzazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e40d-118">Storage Sync Service location.</span></span>

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

### <span data-ttu-id="2e40d-119">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="2e40d-119">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="2e40d-120">IncomingTrafficPolicy del servizio di sincronizzazione di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2e40d-120">Storage Sync Service IncomingTrafficPolicy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e40d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2e40d-121">-Name</span></span>
<span data-ttu-id="2e40d-122">Nome del servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e40d-122">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="2e40d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e40d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e40d-124">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2e40d-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="2e40d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e40d-125">-Tag</span></span>
<span data-ttu-id="2e40d-126">Tag del servizio di sincronizzazione dell'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2e40d-126">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="2e40d-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e40d-127">-Confirm</span></span>
<span data-ttu-id="2e40d-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e40d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e40d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e40d-129">-WhatIf</span></span>
<span data-ttu-id="2e40d-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e40d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2e40d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2e40d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e40d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e40d-132">CommonParameters</span></span>
<span data-ttu-id="2e40d-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e40d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e40d-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e40d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e40d-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="2e40d-135">INPUTS</span></span>

### <span data-ttu-id="2e40d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2e40d-136">System.String</span></span>

## <span data-ttu-id="2e40d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2e40d-137">OUTPUTS</span></span>

### <span data-ttu-id="2e40d-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="2e40d-138">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="2e40d-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="2e40d-139">NOTES</span></span>

## <span data-ttu-id="2e40d-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2e40d-140">RELATED LINKS</span></span>
