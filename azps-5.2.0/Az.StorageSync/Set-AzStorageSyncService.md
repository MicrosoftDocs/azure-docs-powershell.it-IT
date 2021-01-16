---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366519"
---
# <span data-ttu-id="33358-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="33358-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="33358-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33358-102">SYNOPSIS</span></span>
<span data-ttu-id="33358-103">Questo comando imposta il servizio di sincronizzazione dello storage in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33358-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="33358-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33358-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33358-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33358-105">DESCRIPTION</span></span>
<span data-ttu-id="33358-106">Un servizio di sincronizzazione dello spazio di archiviazione è la risorsa di primo livello per la sincronizzazione di file Azure. Questo comando imposta il servizio di sincronizzazione dello storage in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33358-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="33358-107">È consigliabile creare il numero di servizi di sincronizzazione dello spazio di archiviazione necessari per distinguere i gruppi distinti di server dell'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="33358-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="33358-108">Un servizio di sincronizzazione dello spazio di archiviazione contiene gruppi di sincronizzazione e funziona anche come destinazione per la registrazione dei server.</span><span class="sxs-lookup"><span data-stu-id="33358-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="33358-109">Un server può essere registrato solo in un singolo servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33358-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="33358-110">Se i server devono sempre partecipare alla sincronizzazione dello stesso set di file, registrarli nello stesso servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33358-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="33358-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33358-111">EXAMPLES</span></span>

### <span data-ttu-id="33358-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33358-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="33358-113">Questo comando consentirà di impostare un servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33358-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="33358-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33358-114">PARAMETERS</span></span>

### <span data-ttu-id="33358-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33358-115">-DefaultProfile</span></span>
<span data-ttu-id="33358-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33358-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="33358-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="33358-117">-Name</span></span>
<span data-ttu-id="33358-118">Nome del servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33358-118">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="33358-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33358-119">-ResourceGroupName</span></span>
<span data-ttu-id="33358-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="33358-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="33358-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="33358-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="33358-122">Servizio di sincronizzazione di archiviazione IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="33358-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="33358-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="33358-123">-Tag</span></span>
<span data-ttu-id="33358-124">Tag del servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33358-124">Storage Sync Service Tags.</span></span>

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

### <span data-ttu-id="33358-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="33358-125">-Confirm</span></span>
<span data-ttu-id="33358-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33358-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33358-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33358-127">-WhatIf</span></span>
<span data-ttu-id="33358-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33358-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33358-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33358-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33358-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33358-130">CommonParameters</span></span>
<span data-ttu-id="33358-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33358-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33358-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33358-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33358-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33358-133">INPUTS</span></span>

### <span data-ttu-id="33358-134">System. String</span><span class="sxs-lookup"><span data-stu-id="33358-134">System.String</span></span>

## <span data-ttu-id="33358-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33358-135">OUTPUTS</span></span>

### <span data-ttu-id="33358-136">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="33358-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="33358-137">Note</span><span class="sxs-lookup"><span data-stu-id="33358-137">NOTES</span></span>

## <span data-ttu-id="33358-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33358-138">RELATED LINKS</span></span>
