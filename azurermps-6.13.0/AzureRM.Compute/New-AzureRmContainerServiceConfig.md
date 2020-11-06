---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmContainerServiceConfig.md
ms.openlocfilehash: 51ebdbffcb88c1d43716170b236332741d05466f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518848"
---
# <span data-ttu-id="50706-101">New-AzureRmContainerServiceConfig</span><span class="sxs-lookup"><span data-stu-id="50706-101">New-AzureRmContainerServiceConfig</span></span>

## <span data-ttu-id="50706-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50706-102">SYNOPSIS</span></span>
<span data-ttu-id="50706-103">Crea un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-103">Creates a local configuration object for a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50706-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50706-104">SYNTAX</span></span>

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

## <span data-ttu-id="50706-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50706-105">DESCRIPTION</span></span>
<span data-ttu-id="50706-106">Il cmdlet **New-AzureRmContainerServiceConfig** crea un oggetto di configurazione locale per un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-106">The **New-AzureRmContainerServiceConfig** cmdlet creates a local configuration object for a container service.</span></span>
<span data-ttu-id="50706-107">Fornisci questo oggetto al cmdlet New-AzureRmContainerService per creare un servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-107">Provide this object to the New-AzureRmContainerService cmdlet to create a container service.</span></span>

## <span data-ttu-id="50706-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50706-108">EXAMPLES</span></span>

### <span data-ttu-id="50706-109">Esempio 1: creare una configurazione del servizio contenitore</span><span class="sxs-lookup"><span data-stu-id="50706-109">Example 1: Create a container service configuration</span></span>
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

<span data-ttu-id="50706-110">Questo comando crea un contenitore e lo archivia nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="50706-110">This command creates a container, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="50706-111">Il comando specifica le varie impostazioni per la configurazione del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-111">The command specifies various settings for the container service configuration.</span></span> <span data-ttu-id="50706-112">Il comando passa l'oggetto Configuration al cmdlet Add-AzureRmContainerServiceAgentPoolProfile usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="50706-112">The command passes the configuration object to the Add-AzureRmContainerServiceAgentPoolProfile cmdlet by using the pipeline operator.</span></span> <span data-ttu-id="50706-113">Questo cmdlet aggiunge un profilo del pool di agenti.</span><span class="sxs-lookup"><span data-stu-id="50706-113">That cmdlet adds an agent pool profile.</span></span>
<span data-ttu-id="50706-114">Specifica l'oggetto in $Container per il parametro *ContainerService* di **New-AzureRmContainerService**.</span><span class="sxs-lookup"><span data-stu-id="50706-114">Specify the object in $Container for the *ContainerService* parameter of **New-AzureRmContainerService**.</span></span>

## <span data-ttu-id="50706-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50706-115">PARAMETERS</span></span>

### <span data-ttu-id="50706-116">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="50706-116">-AdminUsername</span></span>
<span data-ttu-id="50706-117">Specifica il nome dell'account di amministratore da usare per un servizio contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="50706-117">Specifies the administrator account name to use for a Linux-based container service.</span></span>

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

### <span data-ttu-id="50706-118">-AgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="50706-118">-AgentPoolProfile</span></span>
<span data-ttu-id="50706-119">Specifica una matrice di oggetti del profilo del pool di agenti per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-119">Specifies an array of agent pool profile objects for the container service.</span></span>
<span data-ttu-id="50706-120">Aggiungere un profilo usando il cmdlet Add-AzureRmContainerServiceAgentPoolProfile.</span><span class="sxs-lookup"><span data-stu-id="50706-120">Add a profile by using the Add-AzureRmContainerServiceAgentPoolProfile cmdlet.</span></span>

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

### <span data-ttu-id="50706-121">-CustomProfileOrchestrator</span><span class="sxs-lookup"><span data-stu-id="50706-121">-CustomProfileOrchestrator</span></span>
<span data-ttu-id="50706-122">Specifica l'orchestrazione del profilo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="50706-122">Specifies the custom profile orchestrator.</span></span>

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

### <span data-ttu-id="50706-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50706-123">-DefaultProfile</span></span>
<span data-ttu-id="50706-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50706-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50706-125">-Posizione</span><span class="sxs-lookup"><span data-stu-id="50706-125">-Location</span></span>
<span data-ttu-id="50706-126">Specifica la posizione in cui creare il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-126">Specifies the location in which to create the container service.</span></span>

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

### <span data-ttu-id="50706-127">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="50706-127">-MasterCount</span></span>
<span data-ttu-id="50706-128">Specifica il numero di macchine virtuali master da creare.</span><span class="sxs-lookup"><span data-stu-id="50706-128">Specifies the number of master virtual machines to create.</span></span>

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

### <span data-ttu-id="50706-129">-MasterDnsPrefix</span><span class="sxs-lookup"><span data-stu-id="50706-129">-MasterDnsPrefix</span></span>
<span data-ttu-id="50706-130">Specifica il prefisso DNS per la macchina virtuale master.</span><span class="sxs-lookup"><span data-stu-id="50706-130">Specifies the DNS prefix for the master virtual machine.</span></span>

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

### <span data-ttu-id="50706-131">-OrchestratorType</span><span class="sxs-lookup"><span data-stu-id="50706-131">-OrchestratorType</span></span>
<span data-ttu-id="50706-132">Specifica il tipo di orchestratore per il servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-132">Specifies the type of orchestrator for the container service.</span></span>
<span data-ttu-id="50706-133">I valori accettabili per questo parametro sono: DCOS e Swarm.</span><span class="sxs-lookup"><span data-stu-id="50706-133">The acceptable values for this parameter are: DCOS and Swarm.</span></span>

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

### <span data-ttu-id="50706-134">-ServicePrincipalProfileClientId</span><span class="sxs-lookup"><span data-stu-id="50706-134">-ServicePrincipalProfileClientId</span></span>
<span data-ttu-id="50706-135">Specifica l'ID client del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="50706-135">Specifies the principal profile client ID.</span></span>

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

### <span data-ttu-id="50706-136">-ServicePrincipalProfileSecret</span><span class="sxs-lookup"><span data-stu-id="50706-136">-ServicePrincipalProfileSecret</span></span>
<span data-ttu-id="50706-137">Specifica il segreto del profilo principale.</span><span class="sxs-lookup"><span data-stu-id="50706-137">Specifies the principal profile secret.</span></span>

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

### <span data-ttu-id="50706-138">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="50706-138">-SshPublicKey</span></span>
<span data-ttu-id="50706-139">Specifica la chiave pubblica SSH per un servizio contenitore basato su Linux.</span><span class="sxs-lookup"><span data-stu-id="50706-139">Specifies the SSH public key for a Linux-based container service.</span></span>

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

### <span data-ttu-id="50706-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="50706-140">-Tag</span></span>
<span data-ttu-id="50706-141">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="50706-141">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="50706-142">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="50706-142">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="50706-143">-VmDiagnosticsEnabled</span><span class="sxs-lookup"><span data-stu-id="50706-143">-VmDiagnosticsEnabled</span></span>
<span data-ttu-id="50706-144">Indica se questa configurazione consente la diagnostica per la macchina virtuale del servizio contenitore.</span><span class="sxs-lookup"><span data-stu-id="50706-144">Indicates whether this configuration enables diagnostics for the container service virtual machine.</span></span>

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

### <span data-ttu-id="50706-145">-WindowsProfileAdminPassword</span><span class="sxs-lookup"><span data-stu-id="50706-145">-WindowsProfileAdminPassword</span></span>
<span data-ttu-id="50706-146">Specifica la password di amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="50706-146">Specifies the administrator password for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="50706-147">-WindowsProfileAdminUsername</span><span class="sxs-lookup"><span data-stu-id="50706-147">-WindowsProfileAdminUsername</span></span>
<span data-ttu-id="50706-148">Specifica il nome utente dell'amministratore per un servizio contenitore che usa il sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="50706-148">Specifies the administrator username for a container service that uses the Windows operating system.</span></span>

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

### <span data-ttu-id="50706-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50706-149">-Confirm</span></span>
<span data-ttu-id="50706-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50706-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50706-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50706-151">-WhatIf</span></span>
<span data-ttu-id="50706-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50706-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50706-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50706-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50706-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50706-154">CommonParameters</span></span>
<span data-ttu-id="50706-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50706-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50706-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50706-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50706-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50706-157">INPUTS</span></span>

### <span data-ttu-id="50706-158">System. String</span><span class="sxs-lookup"><span data-stu-id="50706-158">System.String</span></span>

### <span data-ttu-id="50706-159">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50706-159">System.Collections.Hashtable</span></span>

### <span data-ttu-id="50706-160">System. Nullable ' 1 [[Microsoft. Azure. Management. Compute. Models. ContainerServiceOrchestratorTypes, Microsoft. Azure. Management. Compute, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="50706-160">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.ContainerServiceOrchestratorTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="50706-161">System. Int32</span><span class="sxs-lookup"><span data-stu-id="50706-161">System.Int32</span></span>

### <span data-ttu-id="50706-162">Microsoft. Azure. Management. Compute. Models. ContainerServiceAgentPoolProfile []</span><span class="sxs-lookup"><span data-stu-id="50706-162">Microsoft.Azure.Management.Compute.Models.ContainerServiceAgentPoolProfile[]</span></span>

### <span data-ttu-id="50706-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="50706-163">System.String[]</span></span>

### <span data-ttu-id="50706-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50706-164">System.Boolean</span></span>

## <span data-ttu-id="50706-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50706-165">OUTPUTS</span></span>

### <span data-ttu-id="50706-166">Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="50706-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="50706-167">Note</span><span class="sxs-lookup"><span data-stu-id="50706-167">NOTES</span></span>

## <span data-ttu-id="50706-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50706-168">RELATED LINKS</span></span>

[<span data-ttu-id="50706-169">Add-AzureRmContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="50706-169">Add-AzureRmContainerServiceAgentPoolProfile</span></span>](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="50706-170">New-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="50706-170">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)
