---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 87734d63d28785282ad3285ef8cce0a574ba30e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676426"
---
# <span data-ttu-id="b1e3e-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b1e3e-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="b1e3e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="b1e3e-103">Avviso: l'annullamento della registrazione di un server comporterà l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="b1e3e-104">Questo comando Annulla la registrazione di un server è il servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-104">This command will unregister a server it's the storage sync service.</span></span>

## <span data-ttu-id="b1e3e-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1e3e-105">SYNTAX</span></span>

### <span data-ttu-id="b1e3e-106">InputObjectParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b1e3e-106">InputObjectParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e3e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1e3e-107">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1e3e-108">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b1e3e-108">StringParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1e3e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1e3e-109">DESCRIPTION</span></span>
<span data-ttu-id="b1e3e-110">Questo comando Annulla la registrazione di un server dal servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="b1e3e-111">Avviso: l'annullamento della registrazione di un server comporterà l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="b1e3e-112">Dovrebbe essere chiamato solo quando si è certi che non è più possibile sincronizzare un percorso nel server.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="b1e3e-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1e3e-113">EXAMPLES</span></span>

### <span data-ttu-id="b1e3e-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b1e3e-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="b1e3e-115">Questo comando Annulla la registrazione del server, causando l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="b1e3e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1e3e-116">PARAMETERS</span></span>

### <span data-ttu-id="b1e3e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b1e3e-117">-AsJob</span></span>
<span data-ttu-id="b1e3e-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b1e3e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b1e3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1e3e-119">-DefaultProfile</span></span>
<span data-ttu-id="b1e3e-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1e3e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="b1e3e-121">-Force</span></span>
<span data-ttu-id="b1e3e-122">Forza di fornitura per ignorare la conferma di questo comando.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="b1e3e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1e3e-123">-InputObject</span></span>
<span data-ttu-id="b1e3e-124">Oggetto di input RegisteredServer, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="b1e3e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b1e3e-125">-PassThru</span></span>
<span data-ttu-id="b1e3e-126">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b1e3e-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b1e3e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1e3e-127">-ResourceGroupName</span></span>
<span data-ttu-id="b1e3e-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="b1e3e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b1e3e-129">-ResourceId</span></span>
<span data-ttu-id="b1e3e-130">ID risorsa RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b1e3e-130">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="b1e3e-131">-ServerId</span><span class="sxs-lookup"><span data-stu-id="b1e3e-131">-ServerId</span></span>
<span data-ttu-id="b1e3e-132">Nome della RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-132">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="b1e3e-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b1e3e-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="b1e3e-134">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b1e3e-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1e3e-135">-Confirm</span></span>
<span data-ttu-id="b1e3e-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-136">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1e3e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1e3e-137">-WhatIf</span></span>
<span data-ttu-id="b1e3e-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1e3e-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1e3e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e3e-140">CommonParameters</span></span>
<span data-ttu-id="b1e3e-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1e3e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e3e-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e3e-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e3e-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1e3e-143">INPUTS</span></span>

### <span data-ttu-id="b1e3e-144">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="b1e3e-144">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="b1e3e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="b1e3e-145">System.String</span></span>

### <span data-ttu-id="b1e3e-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b1e3e-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b1e3e-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1e3e-147">OUTPUTS</span></span>

### <span data-ttu-id="b1e3e-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="b1e3e-148">System.Object</span></span>
## <span data-ttu-id="b1e3e-149">Note</span><span class="sxs-lookup"><span data-stu-id="b1e3e-149">NOTES</span></span>

## <span data-ttu-id="b1e3e-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1e3e-150">RELATED LINKS</span></span>
