---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: e88f1d3ce684881d839574fe0b73f36b83e275f9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688524"
---
# <span data-ttu-id="d568e-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="d568e-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="d568e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d568e-102">SYNOPSIS</span></span>
<span data-ttu-id="d568e-103">Crea un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d568e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d568e-104">SYNTAX</span></span>

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d568e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d568e-105">DESCRIPTION</span></span>
<span data-ttu-id="d568e-106">Il cmdlet **New-AzureRmContainerServiceConfig** crea un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="d568e-107">Fornisci questo oggetto al cmdlet New-AzureRmContainerService per creare un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="d568e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d568e-108">EXAMPLES</span></span>

### <span data-ttu-id="d568e-109">Esempio 1: creare una configurazione del servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="d568e-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="d568e-110">Questo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="d568e-110">This command creates a container, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="d568e-111">Il comando specifica le varie impostazioni per la configurazione del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-111">The command specifies various settings for the container service configuration.</span></span>
<span data-ttu-id="d568e-112">Il comando passa l'oggetto Configuration al cmdlet Add-AzureRmContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="d568e-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d568e-113">Questo cmdlet aggiunge un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="d568e-113">That cmdlet adds an agent pool profile.</span></span>

<span data-ttu-id="d568e-114">Specifica l'oggetto in $Container per il parametro *ContainerService* di **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="d568e-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="d568e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d568e-115">PARAMETERS</span></span>

### <span data-ttu-id="d568e-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="d568e-116">-AdminUsername</span></span>
<span data-ttu-id="d568e-117">Specifica il nome dell'account di amministratore da usare per un servizio contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="d568e-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="d568e-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d568e-118">-AgentPoolProfile</span></span>
<span data-ttu-id="d568e-119">Specifica una matrice di oggetti del profilo del pool di agenti per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="d568e-120">Aggiungere un profilo usando il cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="d568e-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="d568e-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="d568e-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="d568e-122">Specifica l'orchestrazione del profilo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="d568e-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="d568e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d568e-123">-DefaultProfile</span></span>
<span data-ttu-id="d568e-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d568e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d568e-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d568e-125">-Location</span></span>
<span data-ttu-id="d568e-126">Specifica la posizione in cui creare il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="d568e-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="d568e-127">-MasterCount</span></span>
<span data-ttu-id="d568e-128">Specifica il numero di macchine virtuali master da creare.</span><span class="sxs-lookup"><span data-stu-id="d568e-128">Specifies the number of master virtual machines to create.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d568e-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="d568e-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="d568e-130">Specifica il prefisso DNS per la macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="d568e-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="d568e-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="d568e-131">-OrchestratorType</span></span>
<span data-ttu-id="d568e-132">Specifica il tipo di orchestratore per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="d568e-133">I valori accettabili per questo parametro sono: DCOS e Swarm.</span><span class="sxs-lookup"><span data-stu-id="d568e-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="d568e-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="d568e-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="d568e-135">Specifica l'ID client del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="d568e-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="d568e-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="d568e-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="d568e-137">Specifica il segreto del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="d568e-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="d568e-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d568e-138">-SshPublicKey</span></span>
<span data-ttu-id="d568e-139">Specifica la chiave pubblica SSH per un servizio contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="d568e-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="d568e-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="d568e-140">-Tag</span></span>
<span data-ttu-id="d568e-141">Specifica i tag per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-141">Specifies tags for the container service.</span></span>

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

### <span data-ttu-id="d568e-142">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="d568e-142">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="d568e-143">Indica se questa configurazione consente la diagnostica per la macchina virtuale del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="d568e-143">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="d568e-144">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="d568e-144">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="d568e-145">Specifica la password di amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d568e-145">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="d568e-146">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="d568e-146">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="d568e-147">Specifica il nome utente dell'amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="d568e-147">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="d568e-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d568e-148">-Confirm</span></span>
<span data-ttu-id="d568e-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d568e-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d568e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d568e-150">-WhatIf</span></span>
<span data-ttu-id="d568e-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d568e-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d568e-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d568e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d568e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d568e-153">CommonParameters</span></span>
<span data-ttu-id="d568e-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d568e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d568e-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d568e-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d568e-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d568e-156">INPUTS</span></span>

## <span data-ttu-id="d568e-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d568e-157">OUTPUTS</span></span>

## <span data-ttu-id="d568e-158">Note</span><span class="sxs-lookup"><span data-stu-id="d568e-158">NOTES</span></span>

## <span data-ttu-id="d568e-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d568e-159">RELATED LINKS</span></span>

[<span data-ttu-id="d568e-160">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="d568e-160">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="d568e-161">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="d568e-161">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)


