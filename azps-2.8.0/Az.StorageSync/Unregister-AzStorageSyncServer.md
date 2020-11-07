---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/unregister-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Unregister-AzStorageSyncServer.md
ms.openlocfilehash: 3752e520c3637ffa1e08bfd89d03c6caeebd4e18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855033"
---
# <span data-ttu-id="62701-101">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="62701-101">Unregister-AzStorageSyncServer</span></span>

## <span data-ttu-id="62701-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62701-102">SYNOPSIS</span></span>
<span data-ttu-id="62701-103">Avviso: l'annullamento della registrazione di un server comporterà l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="62701-103">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="62701-104">Questo comando Annulla la registrazione di un server dal servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="62701-104">This command will unregister a server from it's storage sync service.</span></span>

## <span data-ttu-id="62701-105">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62701-105">SYNTAX</span></span>

### <span data-ttu-id="62701-106">StringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="62701-106">StringParameterSet (Default)</span></span>
```
Unregister-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-ServerId] <Guid> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62701-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="62701-107">InputObjectParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-InputObject] <PSRegisteredServer> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62701-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62701-108">ResourceIdParameterSet</span></span>
```
Unregister-AzStorageSyncServer [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62701-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62701-109">DESCRIPTION</span></span>
<span data-ttu-id="62701-110">Questo comando Annulla la registrazione di un server dal servizio di sincronizzazione dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="62701-110">This command will unregister a server from the storage sync service.</span></span> <span data-ttu-id="62701-111">Avviso: l'annullamento della registrazione di un server comporterà l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="62701-111">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="62701-112">Dovrebbe essere chiamato solo quando si è certi che non è più possibile sincronizzare un percorso nel server.</span><span class="sxs-lookup"><span data-stu-id="62701-112">It should only be called when you are certain that no path on this server is to be synced anymore.</span></span>

## <span data-ttu-id="62701-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62701-113">EXAMPLES</span></span>

### <span data-ttu-id="62701-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62701-114">Example 1</span></span>
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> Unregister-AzStorageSyncServer -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -ServerId $RegisteredServer.ServerId
```

<span data-ttu-id="62701-115">Questo comando Annulla la registrazione del server, causando l'eliminazione a cascata di tutti gli endpoint server nel server.</span><span class="sxs-lookup"><span data-stu-id="62701-115">This command will unregister the server, causing cascading deletes of all server endpoints on this server.</span></span>

## <span data-ttu-id="62701-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62701-116">PARAMETERS</span></span>

### <span data-ttu-id="62701-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62701-117">-AsJob</span></span>
<span data-ttu-id="62701-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="62701-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62701-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62701-119">-DefaultProfile</span></span>
<span data-ttu-id="62701-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62701-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62701-121">-Force</span><span class="sxs-lookup"><span data-stu-id="62701-121">-Force</span></span>
<span data-ttu-id="62701-122">Forza di fornitura per ignorare la conferma di questo comando.</span><span class="sxs-lookup"><span data-stu-id="62701-122">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="62701-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62701-123">-InputObject</span></span>
<span data-ttu-id="62701-124">Oggetto di input RegisteredServer, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="62701-124">RegisteredServer Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="62701-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62701-125">-PassThru</span></span>
<span data-ttu-id="62701-126">In esecuzione normale, questo cmdlet non restituisce alcun valore per l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="62701-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="62701-127">Se fornisci il parametro PassThru, il cmdlet scriverà un valore nella pipeline dopo l'esecuzione corretta.</span><span class="sxs-lookup"><span data-stu-id="62701-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="62701-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62701-128">-ResourceGroupName</span></span>
<span data-ttu-id="62701-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="62701-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="62701-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62701-130">-ResourceId</span></span>
<span data-ttu-id="62701-131">ID risorsa RegisteredServer</span><span class="sxs-lookup"><span data-stu-id="62701-131">RegisteredServer Resource Id</span></span>

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

### <span data-ttu-id="62701-132">-ServerId</span><span class="sxs-lookup"><span data-stu-id="62701-132">-ServerId</span></span>
<span data-ttu-id="62701-133">Nome della RegisteredServer.</span><span class="sxs-lookup"><span data-stu-id="62701-133">Name of the RegisteredServer.</span></span>

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

### <span data-ttu-id="62701-134">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="62701-134">-StorageSyncServiceName</span></span>
<span data-ttu-id="62701-135">Nome della StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="62701-135">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="62701-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="62701-136">-Confirm</span></span>
<span data-ttu-id="62701-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62701-137">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62701-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62701-138">-WhatIf</span></span>
<span data-ttu-id="62701-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62701-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62701-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="62701-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62701-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62701-141">CommonParameters</span></span>
<span data-ttu-id="62701-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62701-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62701-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62701-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62701-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62701-144">INPUTS</span></span>

### <span data-ttu-id="62701-145">Microsoft. Azure. Commands. StorageSync. Models. PSRegisteredServer</span><span class="sxs-lookup"><span data-stu-id="62701-145">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

### <span data-ttu-id="62701-146">System. String</span><span class="sxs-lookup"><span data-stu-id="62701-146">System.String</span></span>

### <span data-ttu-id="62701-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62701-147">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="62701-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62701-148">OUTPUTS</span></span>

### <span data-ttu-id="62701-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="62701-149">System.Object</span></span>
## <span data-ttu-id="62701-150">Note</span><span class="sxs-lookup"><span data-stu-id="62701-150">NOTES</span></span>

## <span data-ttu-id="62701-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62701-151">RELATED LINKS</span></span>
