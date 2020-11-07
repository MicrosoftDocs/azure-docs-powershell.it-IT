---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676430"
---
# <span data-ttu-id="f7dae-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="f7dae-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="f7dae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7dae-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dae-103">Usare solo per la risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="f7dae-103">Use for troubleshooting only.</span></span> <span data-ttu-id="f7dae-104">Questo comando consente di eseguire il rollback del certificato del server di sincronizzazione dello storage usato per descrivere l'identità del server al servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f7dae-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="f7dae-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7dae-105">SYNTAX</span></span>

### <span data-ttu-id="f7dae-106">ObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7dae-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7dae-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7dae-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7dae-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7dae-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7dae-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7dae-109">DESCRIPTION</span></span>
<span data-ttu-id="f7dae-110">Questo comando consente di eseguire il rollback del certificato del server di sincronizzazione di archiviazione usato per descrivere l'identità del server al servizio di sincronizzazione dello storage.</span><span class="sxs-lookup"><span data-stu-id="f7dae-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="f7dae-111">Questa operazione è destinata a essere usata in scenari di risoluzione dei problemi.</span><span class="sxs-lookup"><span data-stu-id="f7dae-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="f7dae-112">Quando si chiama questo comando, il certificato del server viene sostituito, aggiornando il servizio di sincronizzazione dello spazio di archiviazione anche questo server viene registrato con l'invio della parte pubblica della chiave.</span><span class="sxs-lookup"><span data-stu-id="f7dae-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="f7dae-113">Dato che viene generato un nuovo certificato, viene aggiornata anche la data di scadenza di questo cert.</span><span class="sxs-lookup"><span data-stu-id="f7dae-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="f7dae-114">Questo comando può essere usato anche per aggiornare un certificato scaduto.</span><span class="sxs-lookup"><span data-stu-id="f7dae-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="f7dae-115">Questo problema può verificarsi se un server è offline per un periodo di tempo prolungato.</span><span class="sxs-lookup"><span data-stu-id="f7dae-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="f7dae-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7dae-116">EXAMPLES</span></span>

### <span data-ttu-id="f7dae-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7dae-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="f7dae-118">Questo comando eseguirà il rollforward del certificato del server locale e informa il servizio di sincronizzazione dello storage corrispondente della nuova identità del server, in modo sicuro.</span><span class="sxs-lookup"><span data-stu-id="f7dae-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="f7dae-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7dae-119">PARAMETERS</span></span>

### <span data-ttu-id="f7dae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dae-120">-DefaultProfile</span></span>
<span data-ttu-id="f7dae-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7dae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7dae-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f7dae-122">-ParentObject</span></span>
<span data-ttu-id="f7dae-123">Oggetto StorageSyncService, in genere passato tramite il parametro.</span><span class="sxs-lookup"><span data-stu-id="f7dae-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="f7dae-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f7dae-124">-ParentResourceId</span></span>
<span data-ttu-id="f7dae-125">ID risorsa padre di StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f7dae-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="f7dae-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7dae-126">-PassThru</span></span>
<span data-ttu-id="f7dae-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f7dae-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f7dae-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7dae-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7dae-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7dae-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="f7dae-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f7dae-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="f7dae-131">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f7dae-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="f7dae-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7dae-132">-Confirm</span></span>
<span data-ttu-id="f7dae-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7dae-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7dae-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7dae-134">-WhatIf</span></span>
<span data-ttu-id="f7dae-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7dae-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7dae-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7dae-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7dae-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dae-137">CommonParameters</span></span>
<span data-ttu-id="f7dae-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7dae-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dae-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7dae-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dae-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7dae-140">INPUTS</span></span>

### <span data-ttu-id="f7dae-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f7dae-141">System.String</span></span>

### <span data-ttu-id="f7dae-142">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="f7dae-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="f7dae-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7dae-143">OUTPUTS</span></span>

### <span data-ttu-id="f7dae-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7dae-144">System.Object</span></span>
## <span data-ttu-id="f7dae-145">Note</span><span class="sxs-lookup"><span data-stu-id="f7dae-145">NOTES</span></span>

## <span data-ttu-id="f7dae-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7dae-146">RELATED LINKS</span></span>
