---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 5ebcdee62997ed678b9696264a40076a40c36342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973981"
---
# <span data-ttu-id="ceeec-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="ceeec-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="ceeec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceeec-102">SYNOPSIS</span></span>
<span data-ttu-id="ceeec-103">Avviso: l'annullamento della registrazione di un server comporterà eliminazioni a catena di tutti gli endpoint server su questo server.</span><span class="sxs-lookup"><span data-stu-id="ceeec-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="ceeec-104">Questo comando anregistrerà un server del servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ceeec-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="ceeec-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ceeec-105">SYNTAX</span></span>

### <span data-ttu-id="ceeec-106">StringParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="ceeec-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceeec-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ceeec-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceeec-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ceeec-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceeec-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ceeec-109">DESCRIPTION</span></span>
<span data-ttu-id="ceeec-110">Questo comando anregistrerà un server dal servizio di sincronizzazione di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ceeec-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="ceeec-111">Avviso: l'annullamento della registrazione di un server comporterà eliminazioni a catena di tutti gli endpoint server su questo server.</span><span class="sxs-lookup"><span data-stu-id="ceeec-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="ceeec-112">Deve essere chiamato solo quando si è certi che non deve più essere sincronizzato alcun percorso in questo server.</span><span class="sxs-lookup"><span data-stu-id="ceeec-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="ceeec-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ceeec-113">EXAMPLES</span></span>

### <span data-ttu-id="ceeec-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ceeec-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="ceeec-115">Questo comando annulla la registrazione del server, causando eliminazioni a catena di tutti gli endpoint server su questo server.</span><span class="sxs-lookup"><span data-stu-id="ceeec-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="ceeec-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceeec-116">PARAMETERS</span></span>

### <span data-ttu-id="ceeec-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ceeec-117">-AsJob</span></span>
<span data-ttu-id="ceeec-118">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ceeec-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ceeec-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceeec-119">-DefaultProfile</span></span>
<span data-ttu-id="ceeec-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ceeec-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ceeec-121">-Force</span><span class="sxs-lookup"><span data-stu-id="ceeec-121">-Force</span></span>
<span data-ttu-id="ceeec-122">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="ceeec-122">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceeec-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceeec-123">-InputObject</span></span>
<span data-ttu-id="ceeec-124">RegisteredServer Input Object, in genere passato attraverso la pipeline.</span><span class="sxs-lookup"><span data-stu-id="ceeec-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceeec-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ceeec-125">-PassThru</span></span>
<span data-ttu-id="ceeec-126">Nella normale esecuzione, questo cmdlet non restituisce alcun valore in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="ceeec-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="ceeec-127">Se si specifica il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="ceeec-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="ceeec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ceeec-128">-ResourceGroupName</span></span>
<span data-ttu-id="ceeec-129">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ceeec-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="ceeec-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ceeec-130">-ResourceId</span></span>
<span data-ttu-id="ceeec-131">RegisteredServer Resource Id</span><span class="sxs-lookup"><span data-stu-id="ceeec-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="ceeec-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="ceeec-132">-ServerId</span></span>
<span data-ttu-id="ceeec-133">Nome del server registrato.</span><span class="sxs-lookup"><span data-stu-id="ceeec-133">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: StringParameterSet
Aliases: RegisteredServerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeec-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ceeec-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="ceeec-135">Nome di StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ceeec-135">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ceeec-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ceeec-136">-Confirm</span></span>
<span data-ttu-id="ceeec-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceeec-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceeec-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceeec-138">-WhatIf</span></span>
<span data-ttu-id="ceeec-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ceeec-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ceeec-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ceeec-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceeec-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceeec-141">CommonParameters</span></span>
<span data-ttu-id="ceeec-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceeec-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceeec-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceeec-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceeec-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="ceeec-144">INPUTS</span></span>

### <span data-ttu-id="ceeec-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="ceeec-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="ceeec-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ceeec-146">System.String</span></span>

### <span data-ttu-id="ceeec-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ceeec-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ceeec-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ceeec-148">OUTPUTS</span></span>

### <span data-ttu-id="ceeec-149">System.Object</span><span class="sxs-lookup"><span data-stu-id="ceeec-149">System.Object</span></span>
## <span data-ttu-id="ceeec-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="ceeec-150">NOTES</span></span>

## <span data-ttu-id="ceeec-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ceeec-151">RELATED LINKS</span></span>
