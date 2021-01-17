---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383557"
---
# <span data-ttu-id="cd647-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd647-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="cd647-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd647-102">SYNOPSIS</span></span>
<span data-ttu-id="cd647-103">Crea un'area di lavoro di analisi sinapsi.</span><span class="sxs-lookup"><span data-stu-id="cd647-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cd647-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd647-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd647-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd647-105">DESCRIPTION</span></span>
<span data-ttu-id="cd647-106">Il cmdlet **New-AzSynapseWorkspace** crea un'area di lavoro di Azure sinapsi Analytics.</span><span class="sxs-lookup"><span data-stu-id="cd647-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="cd647-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd647-107">EXAMPLES</span></span>

### <span data-ttu-id="cd647-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd647-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="cd647-109">Questo comando crea un'area di lavoro di analisi sinapsi denominata ContosoWorkspace che usa l'archivio dati ContosoAdlGenStorage, nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cd647-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="cd647-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd647-110">PARAMETERS</span></span>

### <span data-ttu-id="cd647-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd647-111">-AsJob</span></span>
<span data-ttu-id="cd647-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cd647-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd647-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cd647-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="cd647-114">Nome dell'account di archiviazione predefinito di ADL Gen2.</span><span class="sxs-lookup"><span data-stu-id="cd647-114">The default ADLS Gen2 storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="cd647-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="cd647-116">Il file System ADL Gen2 predefinito.</span><span class="sxs-lookup"><span data-stu-id="cd647-116">The default ADLS Gen2 file system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd647-117">-DefaultProfile</span></span>
<span data-ttu-id="cd647-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd647-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd647-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cd647-119">-Location</span></span>
<span data-ttu-id="cd647-120">Area di Azure in cui deve essere creata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd647-120">Azure region where the resource should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cd647-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="cd647-122">Nome di una rete virtuale gestita da sinapsi dedicata per l'area di lavoro di Azure sinapsi.</span><span class="sxs-lookup"><span data-stu-id="cd647-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: default

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd647-123">-Name</span></span>
<span data-ttu-id="cd647-124">Nome dell'area di lavoro sinapsi.</span><span class="sxs-lookup"><span data-stu-id="cd647-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd647-125">-ResourceGroupName</span></span>
<span data-ttu-id="cd647-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cd647-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="cd647-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="cd647-128">Credenziali di amministratore SQL.</span><span class="sxs-lookup"><span data-stu-id="cd647-128">SQL administrator credentials.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="cd647-129">-Tag</span></span>
<span data-ttu-id="cd647-130">Una stringa, un dizionario di stringhe di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd647-130">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd647-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd647-131">-Confirm</span></span>
<span data-ttu-id="cd647-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd647-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd647-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd647-133">-WhatIf</span></span>
<span data-ttu-id="cd647-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd647-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd647-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd647-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd647-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd647-136">CommonParameters</span></span>
<span data-ttu-id="cd647-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd647-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd647-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd647-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd647-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd647-139">INPUTS</span></span>

### <span data-ttu-id="cd647-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cd647-140">System.String</span></span>

### <span data-ttu-id="cd647-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cd647-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="cd647-142">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="cd647-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="cd647-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd647-143">OUTPUTS</span></span>

### <span data-ttu-id="cd647-144">Microsoft. Azure. Commands. sinapsi. Models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cd647-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cd647-145">Note</span><span class="sxs-lookup"><span data-stu-id="cd647-145">NOTES</span></span>

## <span data-ttu-id="cd647-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd647-146">RELATED LINKS</span></span>
