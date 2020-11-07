---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: fe1422777459123120d32dd4ff0aa4b520ad59dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858362"
---
# <span data-ttu-id="39d4e-101">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d4e-101">Remove-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="39d4e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="39d4e-103">Questo comando eliminerà l'endpoint server specificato.</span><span class="sxs-lookup"><span data-stu-id="39d4e-103">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="39d4e-104">La sincronizzazione con questa posizione si arresta immediatamente.</span><span class="sxs-lookup"><span data-stu-id="39d4e-104">Sync to this location will stop immediately.</span></span>

## <span data-ttu-id="39d4e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39d4e-105">SYNTAX</span></span>

### <span data-ttu-id="39d4e-106">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39d4e-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39d4e-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d4e-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39d4e-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="39d4e-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncServerEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39d4e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39d4e-109">DESCRIPTION</span></span>
<span data-ttu-id="39d4e-110">La rimozione di un endpoint server è un'operazione distruttiva.</span><span class="sxs-lookup"><span data-stu-id="39d4e-110">Removing a server endpoint is a destructive operation.</span></span> <span data-ttu-id="39d4e-111">Il percorso del server smetterà di essere sincronizzato.</span><span class="sxs-lookup"><span data-stu-id="39d4e-111">This server location will stop syncing.</span></span> <span data-ttu-id="39d4e-112">Questa operazione non deve essere eseguita per risolvere i problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="39d4e-112">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="39d4e-113">Se il percorso del server (incl. i file) viene aggiunto di nuovo allo stesso gruppo di sincronizzazione di un endpoint del server, può portare a file di conflitto e ad altre conseguenze impreviste.</span><span class="sxs-lookup"><span data-stu-id="39d4e-113">If this server location (incl. it's files) is added again to the same sync group as a server endpoint, it can lead to conflict files and other unintended consequences.</span></span> <span data-ttu-id="39d4e-114">Questo comando è previsto solo per la disattivazione.</span><span class="sxs-lookup"><span data-stu-id="39d4e-114">This command is intended for decommissioning only.</span></span>

## <span data-ttu-id="39d4e-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39d4e-115">EXAMPLES</span></span>

### <span data-ttu-id="39d4e-116">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="39d4e-116">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncServerEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"
```

<span data-ttu-id="39d4e-117">Questo comando rimuoverà l'endpoint del server.</span><span class="sxs-lookup"><span data-stu-id="39d4e-117">This command will remove the server endpoint.</span></span>

## <span data-ttu-id="39d4e-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39d4e-118">PARAMETERS</span></span>

### <span data-ttu-id="39d4e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39d4e-119">-AsJob</span></span>
<span data-ttu-id="39d4e-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="39d4e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39d4e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39d4e-121">-DefaultProfile</span></span>
<span data-ttu-id="39d4e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39d4e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39d4e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="39d4e-123">-Force</span></span>
<span data-ttu-id="39d4e-124">Forza di fornitura per ignorare la conferma di questo comando.</span><span class="sxs-lookup"><span data-stu-id="39d4e-124">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="39d4e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39d4e-125">-InputObject</span></span>
<span data-ttu-id="39d4e-126">Oggetto di input ServerEndpoint, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="39d4e-126">ServerEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="39d4e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="39d4e-127">-Name</span></span>
<span data-ttu-id="39d4e-128">Nome della ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="39d4e-128">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d4e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39d4e-129">-PassThru</span></span>
<span data-ttu-id="39d4e-130">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="39d4e-130">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="39d4e-131">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="39d4e-131">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="39d4e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39d4e-132">-ResourceGroupName</span></span>
<span data-ttu-id="39d4e-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="39d4e-133">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d4e-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39d4e-134">-ResourceId</span></span>
<span data-ttu-id="39d4e-135">ID risorsa ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d4e-135">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39d4e-136">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="39d4e-136">-StorageSyncServiceName</span></span>
<span data-ttu-id="39d4e-137">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="39d4e-137">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d4e-138">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="39d4e-138">-SyncGroupName</span></span>
<span data-ttu-id="39d4e-139">Nome della SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="39d4e-139">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39d4e-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="39d4e-140">-Confirm</span></span>
<span data-ttu-id="39d4e-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39d4e-141">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39d4e-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39d4e-142">-WhatIf</span></span>
<span data-ttu-id="39d4e-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39d4e-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39d4e-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39d4e-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39d4e-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39d4e-145">CommonParameters</span></span>
<span data-ttu-id="39d4e-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39d4e-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39d4e-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39d4e-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39d4e-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39d4e-148">INPUTS</span></span>

### <span data-ttu-id="39d4e-149">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="39d4e-149">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

### <span data-ttu-id="39d4e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="39d4e-150">System.String</span></span>

## <span data-ttu-id="39d4e-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39d4e-151">OUTPUTS</span></span>

### <span data-ttu-id="39d4e-152">System. Object</span><span class="sxs-lookup"><span data-stu-id="39d4e-152">System.Object</span></span>
## <span data-ttu-id="39d4e-153">Note</span><span class="sxs-lookup"><span data-stu-id="39d4e-153">NOTES</span></span>

## <span data-ttu-id="39d4e-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39d4e-154">RELATED LINKS</span></span>
