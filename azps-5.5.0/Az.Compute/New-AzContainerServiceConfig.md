---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: a2d55c831860f5664f0f8f3dd5312368a9e5da4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199262"
---
# <span data-ttu-id="aeb61-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="aeb61-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="aeb61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeb61-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb61-103">Crea un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="aeb61-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aeb61-104">SYNTAX</span></span>

```
New-AzContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aeb61-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aeb61-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb61-106">Il cmdlet **New-AzContainerServiceConfig crea** un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="aeb61-107">Fornire questo oggetto al cmdlet New-AzContainerService per creare un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="aeb61-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aeb61-108">EXAMPLES</span></span>

### <span data-ttu-id="aeb61-109">Esempio 1: Creare una configurazione del servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="aeb61-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="aeb61-110">Questo comando crea un contenitore e quindi lo archivia nella $Container variabile.</span><span class="sxs-lookup"><span data-stu-id="aeb61-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="aeb61-111">Il comando specifica varie impostazioni per la configurazione del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="aeb61-112">Il comando passa l'oggetto di configurazione al cmdlet Add-AzContainerServiceAgentPoolProfile tramite l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="aeb61-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="aeb61-113">Questo cmdlet aggiunge un profilo di pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="aeb61-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="aeb61-114">Specificare l'oggetto in $Container per il *parametro ContainerService* **di New-AzContainerService.**</span><span class="sxs-lookup"><span data-stu-id="aeb61-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="aeb61-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aeb61-115">PARAMETERS</span></span>

### <span data-ttu-id="aeb61-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="aeb61-116">-AdminUsername</span></span>
<span data-ttu-id="aeb61-117">Specifica il nome dell'account administrator da usare per un servizio contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="aeb61-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="aeb61-118">-AgentPoolProfile</span></span>
<span data-ttu-id="aeb61-119">Specifica una matrice di oggetti profilo del pool di agenti per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="aeb61-120">Aggiungere un profilo usando il cmdlet Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="aeb61-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="aeb61-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="aeb61-122">Specifica l'localizzatore del profilo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="aeb61-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb61-123">-DefaultProfile</span></span>
<span data-ttu-id="aeb61-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aeb61-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aeb61-125">-Location</span><span class="sxs-lookup"><span data-stu-id="aeb61-125">-Location</span></span>
<span data-ttu-id="aeb61-126">Specifica la posizione in cui creare il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="aeb61-127">-MasterCount</span></span>
<span data-ttu-id="aeb61-128">Specifica il numero di macchine virtuali master da creare.</span><span class="sxs-lookup"><span data-stu-id="aeb61-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="aeb61-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="aeb61-130">Specifica il prefisso DNS per la macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="aeb61-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-131">-TorType</span><span class="sxs-lookup"><span data-stu-id="aeb61-131">-OrchestratorType</span></span>
<span data-ttu-id="aeb61-132">Specifica il tipo di contenitore per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="aeb61-133">I valori accettabili per questo parametro sono: DCOS e Swarm.</span><span class="sxs-lookup"><span data-stu-id="aeb61-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes]
Parameter Sets: (All)
Aliases:
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="aeb61-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="aeb61-135">Specifica l'ID client del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="aeb61-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="aeb61-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="aeb61-137">Specifica il segreto del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="aeb61-137">Specifies the principal profile secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="aeb61-138">-SshPublicKey</span></span>
<span data-ttu-id="aeb61-139">Specifica la chiave pubblica SSH per un servizio di contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="aeb61-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="aeb61-140">-Tag</span></span>
<span data-ttu-id="aeb61-141">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="aeb61-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="aeb61-142">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="aeb61-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="aeb61-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="aeb61-144">Indica se questa configurazione abilita la diagnostica per la macchina virtuale del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="aeb61-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="aeb61-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="aeb61-146">Specifica la password dell'amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="aeb61-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="aeb61-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="aeb61-148">Specifica il nome utente dell'amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="aeb61-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb61-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aeb61-149">-Confirm</span></span>
<span data-ttu-id="aeb61-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aeb61-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeb61-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb61-151">-WhatIf</span></span>
<span data-ttu-id="aeb61-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aeb61-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aeb61-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aeb61-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeb61-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb61-154">CommonParameters</span></span>
<span data-ttu-id="aeb61-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aeb61-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb61-156">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aeb61-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb61-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="aeb61-157">INPUTS</span></span>

### <span data-ttu-id="aeb61-158">System.String</span><span class="sxs-lookup"><span data-stu-id="aeb61-158">System.String</span></span>

### <span data-ttu-id="aeb61-159">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aeb61-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="aeb61-160">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="aeb61-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="aeb61-161">System.Int32</span><span class="sxs-lookup"><span data-stu-id="aeb61-161">System.Int32</span></span>

### <span data-ttu-id="aeb61-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span><span class="sxs-lookup"><span data-stu-id="aeb61-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="aeb61-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aeb61-163">System.String[]</span></span>

### <span data-ttu-id="aeb61-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aeb61-164">System.Boolean</span></span>

## <span data-ttu-id="aeb61-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aeb61-165">OUTPUTS</span></span>

### <span data-ttu-id="aeb61-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="aeb61-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="aeb61-167">NOTE</span><span class="sxs-lookup"><span data-stu-id="aeb61-167">NOTES</span></span>

## <span data-ttu-id="aeb61-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aeb61-168">RELATED LINKS</span></span>

[<span data-ttu-id="aeb61-169">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="aeb61-169">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="aeb61-170">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="aeb61-170">New-AzContainerService</span></span>](./New-AzContainerService.md)
