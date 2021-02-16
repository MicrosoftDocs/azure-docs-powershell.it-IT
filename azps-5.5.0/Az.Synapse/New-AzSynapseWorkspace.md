---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseWorkspace.md
ms.openlocfilehash: fb3613555e65b0d13650e5c15189edd865ab2b89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195591"
---
# <span data-ttu-id="5128b-101">New-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5128b-101">New-AzSynapseWorkspace</span></span>

## <span data-ttu-id="5128b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5128b-102">SYNOPSIS</span></span>
<span data-ttu-id="5128b-103">Crea un'area di lavoro Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5128b-103">Creates a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5128b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5128b-104">SYNTAX</span></span>

```
New-AzSynapseWorkspace -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 -DefaultDataLakeStorageAccountName <String> -DefaultDataLakeStorageFilesystem <String>
 -SqlAdministratorLoginCredential <PSCredential> [-ManagedVirtualNetwork <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5128b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5128b-105">DESCRIPTION</span></span>
<span data-ttu-id="5128b-106">Il cmdlet **New-AzSynapseWorkspace** crea un'area di lavoro di Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5128b-106">The **New-AzSynapseWorkspace** cmdlet creates an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="5128b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5128b-107">EXAMPLES</span></span>

### <span data-ttu-id="5128b-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5128b-108">Example 1</span></span>
```powershell
PS C:\> $password = ConvertTo-SecureString "Password123!" -AsPlainText -Force
PS C:\> $creds = New-Object System.Management.Automation.PSCredential ("ContosoUser", $password)
PS C:\> New-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -Name ContosoWorkspace -Location northeurope -DefaultDataLakeStorageAccountName ContosoAdlGen2Storage -DefaultDataLakeStorageFilesystem ContosoFileSystem -SqlAdministratorLoginCredential $creds -AsJob
```

<span data-ttu-id="5128b-109">Questo comando crea un'area di lavoro Synapse Analytics denominata ContosoWorkspace che usa l'archivio dati ContosoAdlGenStorage nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5128b-109">This command creates a Synapse Analytics workspace named ContosoWorkspace that uses the ContosoAdlGenStorage Data Store, in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="5128b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5128b-110">PARAMETERS</span></span>

### <span data-ttu-id="5128b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5128b-111">-AsJob</span></span>
<span data-ttu-id="5128b-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5128b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5128b-113">-DefaultDataLakeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5128b-113">-DefaultDataLakeStorageAccountName</span></span>
<span data-ttu-id="5128b-114">Nome predefinito dell'account di archiviazione ADLS Gen2.</span><span class="sxs-lookup"><span data-stu-id="5128b-114">The default ADLS Gen2 storage account name.</span></span>

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

### <span data-ttu-id="5128b-115">-DefaultDataLakeStorageFilesystem</span><span class="sxs-lookup"><span data-stu-id="5128b-115">-DefaultDataLakeStorageFilesystem</span></span>
<span data-ttu-id="5128b-116">File system ADLS Gen2 predefinito.</span><span class="sxs-lookup"><span data-stu-id="5128b-116">The default ADLS Gen2 file system.</span></span>

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

### <span data-ttu-id="5128b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5128b-117">-DefaultProfile</span></span>
<span data-ttu-id="5128b-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5128b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5128b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5128b-119">-Location</span></span>
<span data-ttu-id="5128b-120">Area geografica di Azure in cui deve essere creata la risorsa.</span><span class="sxs-lookup"><span data-stu-id="5128b-120">Azure region where the resource should be created.</span></span>

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

### <span data-ttu-id="5128b-121">-ManagedVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5128b-121">-ManagedVirtualNetwork</span></span>
<span data-ttu-id="5128b-122">Nome di una rete virtuale gestita da Synapse dedicata per l'area di lavoro Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="5128b-122">Name of a Synapse-managed virtual network dedicated for the Azure Synapse workspace.</span></span>

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

### <span data-ttu-id="5128b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5128b-123">-Name</span></span>
<span data-ttu-id="5128b-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="5128b-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5128b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5128b-125">-ResourceGroupName</span></span>
<span data-ttu-id="5128b-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5128b-126">Resource group name.</span></span>

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

### <span data-ttu-id="5128b-127">-SqlAdministratorLoginCredential</span><span class="sxs-lookup"><span data-stu-id="5128b-127">-SqlAdministratorLoginCredential</span></span>
<span data-ttu-id="5128b-128">SQL credenziali di amministratore.</span><span class="sxs-lookup"><span data-stu-id="5128b-128">SQL administrator credentials.</span></span>

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

### <span data-ttu-id="5128b-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="5128b-129">-Tag</span></span>
<span data-ttu-id="5128b-130">Stringa, dizionario stringa di tag associati alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="5128b-130">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="5128b-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5128b-131">-Confirm</span></span>
<span data-ttu-id="5128b-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5128b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5128b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5128b-133">-WhatIf</span></span>
<span data-ttu-id="5128b-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5128b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5128b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5128b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5128b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5128b-136">CommonParameters</span></span>
<span data-ttu-id="5128b-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5128b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5128b-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5128b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5128b-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="5128b-139">INPUTS</span></span>

### <span data-ttu-id="5128b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5128b-140">System.String</span></span>

### <span data-ttu-id="5128b-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5128b-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="5128b-142">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="5128b-142">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="5128b-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5128b-143">OUTPUTS</span></span>

### <span data-ttu-id="5128b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5128b-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="5128b-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="5128b-145">NOTES</span></span>

## <span data-ttu-id="5128b-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5128b-146">RELATED LINKS</span></span>
