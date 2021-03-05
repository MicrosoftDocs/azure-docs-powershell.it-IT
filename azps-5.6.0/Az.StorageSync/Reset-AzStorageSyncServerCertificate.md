---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 5d93249b6bb160d2659ead144d3fabda1af8438d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974013"
---
# <span data-ttu-id="69b16-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="69b16-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="69b16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b16-102">SYNOPSIS</span></span>
<span data-ttu-id="69b16-103">Da usare solo per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="69b16-103">Use for troubleshooting only.</span></span> <span data-ttu-id="69b16-104">Questo comando esegue il roll roll del certificato del server di sincronizzazione di archiviazione usato per descrivere l'identità del server nel servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69b16-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="69b16-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69b16-105">SYNTAX</span></span>

### <span data-ttu-id="69b16-106">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="69b16-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b16-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="69b16-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b16-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="69b16-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69b16-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="69b16-109">DESCRIPTION</span></span>
<span data-ttu-id="69b16-110">Questo comando rollirà il certificato del server di sincronizzazione dello spazio di archiviazione usato per descrivere l'identità del server nel servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="69b16-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="69b16-111">Questa soluzione è pensata per essere usata negli scenari di risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="69b16-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="69b16-112">Quando si chiama questo comando, il certificato del server viene sostituito, aggiornando anche il servizio di sincronizzazione di archiviazione con cui è registrato il server inviando la parte pubblica della chiave.</span><span class="sxs-lookup"><span data-stu-id="69b16-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="69b16-113">Poiché viene generato un nuovo certificato, viene aggiornata anche la data di scadenza del certificato.</span><span class="sxs-lookup"><span data-stu-id="69b16-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="69b16-114">Questo comando può essere usato anche per aggiornare un certificato scaduto.</span><span class="sxs-lookup"><span data-stu-id="69b16-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="69b16-115">Questo problema può verificarsi se un server è offline per un periodo di tempo prolungato.</span><span class="sxs-lookup"><span data-stu-id="69b16-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="69b16-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69b16-116">EXAMPLES</span></span>

### <span data-ttu-id="69b16-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="69b16-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="69b16-118">Questo comando esegue il roll-to-roll del certificato del server locale e informa in modo sicuro il servizio di sincronizzazione di archiviazione corrispondente della nuova identità del server.</span><span class="sxs-lookup"><span data-stu-id="69b16-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="69b16-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69b16-119">PARAMETERS</span></span>

### <span data-ttu-id="69b16-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b16-120">-DefaultProfile</span></span>
<span data-ttu-id="69b16-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69b16-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69b16-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="69b16-122">-ParentObject</span></span>
<span data-ttu-id="69b16-123">Oggetto StorageSyncService, in genere passato attraverso il parametro.</span><span class="sxs-lookup"><span data-stu-id="69b16-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="69b16-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="69b16-124">-ParentResourceId</span></span>
<span data-ttu-id="69b16-125">ID risorsa padre StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="69b16-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="69b16-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69b16-126">-PassThru</span></span>
<span data-ttu-id="69b16-127">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="69b16-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="69b16-128">Se si fornisce il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="69b16-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="69b16-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b16-129">-ResourceGroupName</span></span>
<span data-ttu-id="69b16-130">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="69b16-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="69b16-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="69b16-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="69b16-132">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="69b16-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="69b16-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69b16-133">-Confirm</span></span>
<span data-ttu-id="69b16-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69b16-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b16-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b16-135">-WhatIf</span></span>
<span data-ttu-id="69b16-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69b16-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69b16-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69b16-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b16-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b16-138">CommonParameters</span></span>
<span data-ttu-id="69b16-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b16-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b16-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b16-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b16-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="69b16-141">INPUTS</span></span>

### <span data-ttu-id="69b16-142">System.String</span><span class="sxs-lookup"><span data-stu-id="69b16-142">System.String</span></span>

### <span data-ttu-id="69b16-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="69b16-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="69b16-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69b16-144">OUTPUTS</span></span>

### <span data-ttu-id="69b16-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="69b16-145">System.Object</span></span>
## <span data-ttu-id="69b16-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="69b16-146">NOTES</span></span>

## <span data-ttu-id="69b16-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69b16-147">RELATED LINKS</span></span>
