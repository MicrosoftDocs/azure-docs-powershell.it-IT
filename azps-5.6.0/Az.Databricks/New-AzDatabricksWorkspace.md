---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/new-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksWorkspace.md
ms.openlocfilehash: c49056da040e7259c1cbc0964335f157e00cbecd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962238"
---
# <span data-ttu-id="dfef1-101">New-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="dfef1-101">New-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="dfef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfef1-102">SYNOPSIS</span></span>
<span data-ttu-id="dfef1-103">Crea una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="dfef1-103">Creates a new workspace.</span></span>

## <span data-ttu-id="dfef1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dfef1-104">SYNTAX</span></span>

```
New-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-EnableNoPublicIP] [-ManagedResourceGroupName <String>] [-PrepareEncryption]
 [-PrivateSubnetName <String>] [-PublicSubnetName <String>] [-RequireInfrastructureEncryption] [-Sku <String>]
 [-Tag <Hashtable>] [-VirtualNetworkId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfef1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dfef1-105">DESCRIPTION</span></span>
<span data-ttu-id="dfef1-106">Crea una nuova area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="dfef1-106">Creates a new workspace.</span></span>

## <span data-ttu-id="dfef1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dfef1-107">EXAMPLES</span></span>

### <span data-ttu-id="dfef1-108">Esempio 1: Creare un'area di lavoro Databricks</span><span class="sxs-lookup"><span data-stu-id="dfef1-108">Example 1: Create a Databricks workspace</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup -Location eastus -ManagedResourceGroupName databricks-group -Sku standard

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="dfef1-109">Questo comando crea un'area di lavoro Databricks.</span><span class="sxs-lookup"><span data-stu-id="dfef1-109">This command creates a Databricks workspace.</span></span>

### <span data-ttu-id="dfef1-110">Esempio 2: Creare un'area di lavoro Databricks con una rete virtuale personalizzata</span><span class="sxs-lookup"><span data-stu-id="dfef1-110">Example 2: Create a Databricks workspace with a customized virtual network</span></span>
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

<span data-ttu-id="dfef1-111">Questo comando crea un'area di lavoro Databricks con una rete virtuale personalizzata in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dfef1-111">This command creates a Databricks workspace with customized virtual network in a resource group.</span></span>

### <span data-ttu-id="dfef1-112">Esempio 3: Creare un'area di lavoro Databricks con l'abilitazione della crittografia</span><span class="sxs-lookup"><span data-stu-id="dfef1-112">Example 3: Create a Databricks workspace with enable encryption</span></span>
```powershell
PS C:\> New-AzDatabricksWorkspace -Name databricks-test02 -ResourceGroupName testgroup -PrepareEncryption -Location "East US 2 EUAP" -Sku premium

Location Name            Type
-------- ----            ----
eastus   databricks-test02 Microsoft.Databricks/workspaces
```

<span data-ttu-id="dfef1-113">Questo comando crea un'area di lavoro Databricks e la imposta in modo da preparare la crittografia.</span><span class="sxs-lookup"><span data-stu-id="dfef1-113">This command creates a Databricks workspace and sets it to prepare for encryption.</span></span>
<span data-ttu-id="dfef1-114">Per altre impostazioni per la crittografia, Update-AzDatabricksWorkspace esempi di crittografia.</span><span class="sxs-lookup"><span data-stu-id="dfef1-114">Please refer to the examples of Update-AzDatabricksWorkspace for more settings to encryption.</span></span>

## <span data-ttu-id="dfef1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfef1-115">PARAMETERS</span></span>

### <span data-ttu-id="dfef1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfef1-116">-AsJob</span></span>
<span data-ttu-id="dfef1-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="dfef1-117">Run the command as a job</span></span>

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

### <span data-ttu-id="dfef1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfef1-118">-DefaultProfile</span></span>
<span data-ttu-id="dfef1-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dfef1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfef1-120">-EnableNoPublicIP</span><span class="sxs-lookup"><span data-stu-id="dfef1-120">-EnableNoPublicIP</span></span>
<span data-ttu-id="dfef1-121">Valore da usare per il campo.</span><span class="sxs-lookup"><span data-stu-id="dfef1-121">The value which should be used for this field.</span></span>

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

### <span data-ttu-id="dfef1-122">-Location</span><span class="sxs-lookup"><span data-stu-id="dfef1-122">-Location</span></span>
<span data-ttu-id="dfef1-123">Posizione geografica in cui si trova la risorsa</span><span class="sxs-lookup"><span data-stu-id="dfef1-123">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="dfef1-124">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfef1-124">-ManagedResourceGroupName</span></span>
<span data-ttu-id="dfef1-125">Nome del gruppo di risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="dfef1-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="dfef1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="dfef1-126">-Name</span></span>
<span data-ttu-id="dfef1-127">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="dfef1-127">The name of the workspace.</span></span>

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

### <span data-ttu-id="dfef1-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dfef1-128">-NoWait</span></span>
<span data-ttu-id="dfef1-129">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="dfef1-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dfef1-130">-PrepareEncryption</span><span class="sxs-lookup"><span data-stu-id="dfef1-130">-PrepareEncryption</span></span>
<span data-ttu-id="dfef1-131">Preparare l'area di lavoro per la crittografia.</span><span class="sxs-lookup"><span data-stu-id="dfef1-131">Prepare the workspace for encryption.</span></span>
<span data-ttu-id="dfef1-132">Abilita l'identità gestita per l'account di archiviazione gestita.</span><span class="sxs-lookup"><span data-stu-id="dfef1-132">Enables the Managed Identity for managed storage account.</span></span>

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

### <span data-ttu-id="dfef1-133">-PrivateSubnetName</span><span class="sxs-lookup"><span data-stu-id="dfef1-133">-PrivateSubnetName</span></span>
<span data-ttu-id="dfef1-134">Nome della subnet privata all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfef1-134">The name of the Private Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="dfef1-135">-PublicSubnetName</span><span class="sxs-lookup"><span data-stu-id="dfef1-135">-PublicSubnetName</span></span>
<span data-ttu-id="dfef1-136">Nome di una subnet pubblica all'interno della rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="dfef1-136">The name of a Public Subnet within the Virtual Network.</span></span>

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

### <span data-ttu-id="dfef1-137">-RequireInfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="dfef1-137">-RequireInfrastructureEncryption</span></span>
<span data-ttu-id="dfef1-138">Valore booleano che indica se il file system radice DBFS verrà abilitato o meno con un livello secondario di crittografia con chiavi gestite dalla piattaforma per i dati in archivio.</span><span class="sxs-lookup"><span data-stu-id="dfef1-138">A boolean indicating whether or not the DBFS root file system will be enabled with secondary layer of encryption with platform managed keys for data at rest.</span></span>

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

### <span data-ttu-id="dfef1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfef1-139">-ResourceGroupName</span></span>
<span data-ttu-id="dfef1-140">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dfef1-140">The name of the resource group.</span></span>
<span data-ttu-id="dfef1-141">Per il nome non viene distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="dfef1-141">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dfef1-142">-SKU</span><span class="sxs-lookup"><span data-stu-id="dfef1-142">-Sku</span></span>
<span data-ttu-id="dfef1-143">Nome SKU.</span><span class="sxs-lookup"><span data-stu-id="dfef1-143">The SKU name.</span></span>

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

### <span data-ttu-id="dfef1-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfef1-144">-SubscriptionId</span></span>
<span data-ttu-id="dfef1-145">ID della sottoscrizione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="dfef1-145">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dfef1-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="dfef1-146">-Tag</span></span>
<span data-ttu-id="dfef1-147">Tag di risorse.</span><span class="sxs-lookup"><span data-stu-id="dfef1-147">Resource tags.</span></span>

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

### <span data-ttu-id="dfef1-148">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="dfef1-148">-VirtualNetworkId</span></span>
<span data-ttu-id="dfef1-149">ID di una rete virtuale in cui deve essere creato il cluster di databricks.</span><span class="sxs-lookup"><span data-stu-id="dfef1-149">The ID of a Virtual Network where this Databricks Cluster should be created.</span></span>

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

### <span data-ttu-id="dfef1-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfef1-150">-Confirm</span></span>
<span data-ttu-id="dfef1-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfef1-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfef1-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfef1-152">-WhatIf</span></span>
<span data-ttu-id="dfef1-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfef1-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfef1-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dfef1-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfef1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfef1-155">CommonParameters</span></span>
<span data-ttu-id="dfef1-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfef1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfef1-157">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dfef1-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfef1-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="dfef1-158">INPUTS</span></span>

## <span data-ttu-id="dfef1-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dfef1-159">OUTPUTS</span></span>

### <span data-ttu-id="dfef1-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="dfef1-160">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="dfef1-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="dfef1-161">NOTES</span></span>

<span data-ttu-id="dfef1-162">ALIAS</span><span class="sxs-lookup"><span data-stu-id="dfef1-162">ALIASES</span></span>

## <span data-ttu-id="dfef1-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dfef1-163">RELATED LINKS</span></span>

