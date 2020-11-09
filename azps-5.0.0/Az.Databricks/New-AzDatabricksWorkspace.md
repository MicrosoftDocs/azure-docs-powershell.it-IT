---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: 09f1cd27e9af0c6442afa00d5301975cae8fbdeb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297319"
---
# <span data-ttu-id="5549b-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="5549b-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="5549b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5549b-102">SYNOPSIS</span></span>
<span data-ttu-id="5549b-103">Crea una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5549b-103">Creates a new workspace.</span></span>

## <span data-ttu-id="5549b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5549b-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5549b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5549b-105">DESCRIPTION</span></span>
<span data-ttu-id="5549b-106">Crea una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5549b-106">Creates a new workspace.</span></span>

## <span data-ttu-id="5549b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5549b-107">EXAMPLES</span></span>

### <span data-ttu-id="5549b-108">Esempio 1: creare un'area di lavoro databricks</span><span class="sxs-lookup"><span data-stu-id="5549b-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="5549b-109">Questo comando crea un'area di lavoro databricks.</span><span class="sxs-lookup"><span data-stu-id="5549b-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="5549b-110">Esempio 2: creare un'area di lavoro databricks con una rete virtuale personalizzata</span><span class="sxs-lookup"><span data-stu-id="5549b-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
```powershell
PS C:\> $dlg = New-AzDelegation -Name dbrdl -ServiceName "Microsoft.Databricks/workspaces"
PS C:\> $rdpRule = New-AzNetworkSecurityRuleConfig -Name rdp-rule -Description "Allow RDP" -Access Allow -Protocol Tcp -Direction Inbound -Priority 100 -SourceAddressPrefix Internet -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $networkSecurityGroup = New-AzNetworkSecurityGroup -ResourceGroupName testgroup -Location eastus -Name nsg-test -SecurityRules $rdpRule
PS C:\> $privSubnet = New-AzVirtualNetworkSubnetConfig -Name priv-sub -AddressPrefix "10.0.1.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $pubSubnet = New-AzVirtualNetworkSubnetConfig -Name pub-sub  -AddressPrefix "10.0.2.0/24" -NetworkSecurityGroup $networkSecurityGroup -Delegation $dlg
PS C:\> $testVN = New-AzVirtualNetwork -Name testvn -ResourceGroupName testgroup -Location eastus -AddressPrefix "10.0.0.0/16" -Subnet $privSubnet,$pubSubnet
PS C:\> New-AzDatabricksWorkspace -Name databricks-test-with-custom-vn -ResourceGroupName testgroup -Location eastus -VirtualNetworkId $testVN.Id -PrivateSubnetName $privSubnet.Name -PublicSubnetName $privSubnet.Name -Sku standard

Location Name                           Type
-------- ----                           ----
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="5549b-111">Questo comando crea un'area di lavoro databricks con una rete virtuale personalizzata in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5549b-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="5549b-112">Esempio 3: creare un'area di lavoro databricks con Enable Encryption</span><span class="sxs-lookup"><span data-stu-id="5549b-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="5549b-113">Questo comando crea un'area di lavoro databricks e la imposta per prepararsi per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="5549b-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="5549b-114">Vedere gli esempi di Update-AzDatabricksWorkspace per altre impostazioni da crittografare.</span><span class="sxs-lookup"><span data-stu-id="5549b-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="5549b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5549b-115">PARAMETERS</span></span>

### <span data-ttu-id="5549b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5549b-116">-AsJob</span></span>
<span data-ttu-id="5549b-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="5549b-117">Run the command as a job</span></span>

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

### <span data-ttu-id="5549b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5549b-118">-DefaultProfile</span></span>
<span data-ttu-id="5549b-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5549b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5549b-120">-Location</span></span>
<span data-ttu-id="5549b-121">Posizione geografica in cui vive la risorsa</span><span class="sxs-lookup"><span data-stu-id="5549b-121">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-122">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5549b-122">-ManagedResourceGroupName</span></span>
<span data-ttu-id="5549b-123">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="5549b-123">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="5549b-124">-Name</span></span>
<span data-ttu-id="5549b-125">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="5549b-125">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-126">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="5549b-126">-NoWait</span></span>
<span data-ttu-id="5549b-127">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="5549b-127">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5549b-128">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="5549b-128">-PrepareEncryption</span></span>
<span data-ttu-id="5549b-129">Preparare l'area di lavoro per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="5549b-129">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="5549b-130">Abilita l'identità gestita per l'account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="5549b-130">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="5549b-131">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="5549b-131">-PrivateSubnetName</span></span>
<span data-ttu-id="5549b-132">Nome della subnet privata all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5549b-132">The name of the Private Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-133">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="5549b-133">-PublicSubnetName</span></span>
<span data-ttu-id="5549b-134">Nome di una subnet pubblica all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="5549b-134">The name of a Public Subnet within the Virtual Network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-135">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="5549b-135">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="5549b-136">Valore booleano che indica se il file system radice di DBFS verrà abilitato con il livello secondario di crittografia con le chiavi gestite della piattaforma per i dati a riposo.</span><span class="sxs-lookup"><span data-stu-id="5549b-136">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="5549b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5549b-137">-ResourceGroupName</span></span>
<span data-ttu-id="5549b-138">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5549b-138">The name of the resource group.</span></span>
<span data-ttu-id="5549b-139">Il nome è senza distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="5549b-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-140">-SKU</span><span class="sxs-lookup"><span data-stu-id="5549b-140">-Sku</span></span>
<span data-ttu-id="5549b-141">Nome Usk.</span><span class="sxs-lookup"><span data-stu-id="5549b-141">The SKU name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5549b-142">-SubscriptionId</span></span>
<span data-ttu-id="5549b-143">ID dell'abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5549b-143">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="5549b-144">-Tag</span></span>
<span data-ttu-id="5549b-145">Tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="5549b-145">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-146">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="5549b-146">-VirtualNetworkId</span></span>
<span data-ttu-id="5549b-147">ID di una rete virtuale in cui deve essere creato il cluster databricks.</span><span class="sxs-lookup"><span data-stu-id="5549b-147">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5549b-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5549b-148">-Confirm</span></span>
<span data-ttu-id="5549b-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5549b-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5549b-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5549b-150">-WhatIf</span></span>
<span data-ttu-id="5549b-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5549b-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5549b-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5549b-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5549b-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5549b-153">CommonParameters</span></span>
<span data-ttu-id="5549b-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5549b-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5549b-155">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5549b-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5549b-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5549b-156">INPUTS</span></span>

## <span data-ttu-id="5549b-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5549b-157">OUTPUTS</span></span>

### <span data-ttu-id="5549b-158">Microsoft. Azure. PowerShell. Cmdlets. databricks. Models. Api20180401. IWorkspace</span><span class="sxs-lookup"><span data-stu-id="5549b-158">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="5549b-159">Note</span><span class="sxs-lookup"><span data-stu-id="5549b-159">NOTES</span></span>

<span data-ttu-id="5549b-160">ALIAS</span><span class="sxs-lookup"><span data-stu-id="5549b-160">ALIASES</span></span>

## <span data-ttu-id="5549b-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5549b-161">RELATED LINKS</span></span>

