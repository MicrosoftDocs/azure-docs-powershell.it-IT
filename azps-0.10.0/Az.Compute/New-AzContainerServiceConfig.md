---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerServiceConfig.md
ms.openlocfilehash: 4352edac7342bd421fb907295581aaa6bee8e8ef
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863657"
---
# <span data-ttu-id="d49ee-101">New-AzContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="d49ee-101">New-AzContainerServiceConfig</span></span>

## <span data-ttu-id="d49ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d49ee-102">SYNOPSIS</span></span>
<span data-ttu-id="d49ee-103">Crea un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-103">Creates a local configuration object for a container service.</span></span>

## <span data-ttu-id="d49ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d49ee-104">SYNTAX</span></span>

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

## <span data-ttu-id="d49ee-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d49ee-105">DESCRIPTION</span></span>
<span data-ttu-id="d49ee-106">Il cmdlet **New-AzContainerServiceConfig** crea un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-106">The **New-AzContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="d49ee-107">Fornisci questo oggetto al cmdlet New-AzContainerService per creare un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-107">Provide this object to the New-AzContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="d49ee-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d49ee-108">EXAMPLES</span></span>

### <span data-ttu-id="d49ee-109">Esempio 1: creare una configurazione del servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="d49ee-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="d49ee-110">Questo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="d49ee-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d49ee-111">Il comando specifica le varie impostazioni per la configurazione del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="d49ee-112">Il comando passa l'oggetto Configuration al cmdlet Add-AzContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d49ee-112">The command passes the configuration object to the Add-AzContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="d49ee-113">Questo cmdlet aggiunge un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="d49ee-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="d49ee-114">Specifica l'oggetto in $Container per il parametro *ContainerService* di **New-AzContainerService**.</span><span class="sxs-lookup"><span data-stu-id="d49ee-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzContainerService**.</span></span>

## <span data-ttu-id="d49ee-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d49ee-115">PARAMETERS</span></span>

### <span data-ttu-id="d49ee-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="d49ee-116">-AdminUsername</span></span>
<span data-ttu-id="d49ee-117">Specifica il nome dell'account di amministratore da usare per un servizio contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="d49ee-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d49ee-118">-AgentPoolProfile</span></span>
<span data-ttu-id="d49ee-119">Specifica una matrice di oggetti del profilo del pool di agenti per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="d49ee-120">Aggiungere un profilo usando il cmdlet Add-AzContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="d49ee-120">Add a profile by using the Add-AzContainerServiceAgentPoolProfile cmdlet.</span></span>

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="d49ee-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="d49ee-122">Specifica l'orchestrazione del profilo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d49ee-122">Specifies the custom profile orchestrator.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49ee-123">-DefaultProfile</span></span>
<span data-ttu-id="d49ee-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d49ee-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d49ee-125">-Location</span></span>
<span data-ttu-id="d49ee-126">Specifica la posizione in cui creare il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-126">Specifies the location in which to create the container service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="d49ee-127">-MasterCount</span></span>
<span data-ttu-id="d49ee-128">Specifica il numero di macchine virtuali master da creare.</span><span class="sxs-lookup"><span data-stu-id="d49ee-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="d49ee-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="d49ee-130">Specifica il prefisso DNS per la macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="d49ee-130">Specifies the DNS prefix for the master virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="d49ee-131">-OrchestratorType</span></span>
<span data-ttu-id="d49ee-132">Specifica il tipo di orchestratore per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="d49ee-133">I valori accettabili per questo parametro sono: DCOS e Swarm.</span><span class="sxs-lookup"><span data-stu-id="d49ee-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="d49ee-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="d49ee-135">Specifica l'ID client del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="d49ee-135">Specifies the principal profile client ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="d49ee-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="d49ee-137">Specifica il segreto del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="d49ee-137">Specifies the principal profile secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d49ee-138">-SshPublicKey</span></span>
<span data-ttu-id="d49ee-139">Specifica la chiave pubblica SSH per un servizio contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="d49ee-139">Specifies the SSH public key for a Linux-based container service.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="d49ee-140">-Tag</span></span>
<span data-ttu-id="d49ee-141">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d49ee-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d49ee-142">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="d49ee-142">For example:</span></span>

<span data-ttu-id="d49ee-143">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d49ee-143">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-144">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="d49ee-144">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="d49ee-145">Indica se questa configurazione consente la diagnostica per la macchina virtuale del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d49ee-145">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-146">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="d49ee-146">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="d49ee-147">Specifica la password di amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d49ee-147">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-148">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="d49ee-148">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="d49ee-149">Specifica il nome utente dell'amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d49ee-149">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d49ee-150">-Confirm</span></span>
<span data-ttu-id="d49ee-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d49ee-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d49ee-152">-WhatIf</span></span>
<span data-ttu-id="d49ee-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d49ee-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d49ee-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d49ee-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49ee-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49ee-155">CommonParameters</span></span>
<span data-ttu-id="d49ee-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d49ee-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49ee-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49ee-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49ee-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d49ee-158">INPUTS</span></span>

### <span data-ttu-id="d49ee-159">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d49ee-159">None</span></span>
<span data-ttu-id="d49ee-160">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d49ee-160">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d49ee-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d49ee-161">OUTPUTS</span></span>

### <span data-ttu-id="d49ee-162">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="d49ee-162">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="d49ee-163">Note</span><span class="sxs-lookup"><span data-stu-id="d49ee-163">NOTES</span></span>

## <span data-ttu-id="d49ee-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d49ee-164">RELATED LINKS</span></span>

[<span data-ttu-id="d49ee-165">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d49ee-165">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d49ee-166">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="d49ee-166">New-AzContainerService</span></span>](./New-AzContainerService.md)
