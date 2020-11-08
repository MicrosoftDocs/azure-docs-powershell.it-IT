---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: 6d264ff7e2f12777845edbf2d56cae3d8b59ddb0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189651"
---
# <span data-ttu-id="be049-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="be049-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="be049-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be049-102">SYNOPSIS</span></span>
<span data-ttu-id="be049-103">Aggiorna il set di regole di rete in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="be049-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="be049-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be049-104">SYNTAX</span></span>

### <span data-ttu-id="be049-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be049-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be049-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="be049-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be049-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="be049-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be049-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be049-108">DESCRIPTION</span></span>
<span data-ttu-id="be049-109">Il comando **Update-AzKeyVaultNetworkRuleSet** aggiorna le regole di rete in vigore nell'archivio chiavi specificato.</span><span class="sxs-lookup"><span data-stu-id="be049-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="be049-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be049-110">EXAMPLES</span></span>

### <span data-ttu-id="be049-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be049-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="be049-112">Questo comando Aggiorna le regole di rete nel Vault denominato "Vault" per l'intervallo IP specificato e la rete virtuale, consentendo l'esclusione della regola di rete per i servizi Azure.</span><span class="sxs-lookup"><span data-stu-id="be049-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="be049-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="be049-113">Example 2</span></span>

<span data-ttu-id="be049-114">Aggiorna il set di regole di rete in un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="be049-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="be049-115">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="be049-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="be049-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be049-116">PARAMETERS</span></span>

### <span data-ttu-id="be049-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="be049-117">-Bypass</span></span>
<span data-ttu-id="be049-118">Specifica l'esclusione della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="be049-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be049-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="be049-119">-DefaultAction</span></span>
<span data-ttu-id="be049-120">Specifica l'azione predefinita della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="be049-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be049-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be049-121">-DefaultProfile</span></span>
<span data-ttu-id="be049-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be049-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be049-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be049-123">-InputObject</span></span>
<span data-ttu-id="be049-124">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="be049-124">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be049-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="be049-125">-IpAddressRange</span></span>
<span data-ttu-id="be049-126">Specifica l'intervallo di indirizzi IP di rete consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="be049-126">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be049-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="be049-127">-PassThru</span></span>
<span data-ttu-id="be049-128">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="be049-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="be049-129">Se questo parametro viene specificato, restituisce l'oggetto Key Vault aggiornato.</span><span class="sxs-lookup"><span data-stu-id="be049-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="be049-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be049-130">-ResourceGroupName</span></span>
<span data-ttu-id="be049-131">Specifica il nome del gruppo di risorse associato al Vault della chiave la cui regola di rete viene modificata.</span><span class="sxs-lookup"><span data-stu-id="be049-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be049-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be049-132">-ResourceId</span></span>
<span data-ttu-id="be049-133">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="be049-133">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be049-134">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="be049-134">-VaultName</span></span>
<span data-ttu-id="be049-135">Specifica il nome di un Vault chiave di cui è in corso la modifica della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="be049-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be049-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="be049-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="be049-137">Specifica l'identificatore delle risorse di rete virtuale consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="be049-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be049-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be049-138">-Confirm</span></span>
<span data-ttu-id="be049-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be049-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be049-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be049-140">-WhatIf</span></span>
<span data-ttu-id="be049-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be049-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be049-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be049-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be049-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be049-143">CommonParameters</span></span>
<span data-ttu-id="be049-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be049-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be049-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be049-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be049-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be049-146">INPUTS</span></span>

### <span data-ttu-id="be049-147">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="be049-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="be049-148">System. String</span><span class="sxs-lookup"><span data-stu-id="be049-148">System.String</span></span>

### <span data-ttu-id="be049-149">System. Nullable ' 1 [[Microsoft. Azure. Commands. DataVault. Models. PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft. Azure. PowerShell. cmdlet. tastiera, versione = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="be049-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="be049-150">System. Nullable ' 1 [[Microsoft. Azure. Commands. DataVault. Models. PSKeyVaultNetworkRuleBypassEnum, Microsoft. Azure. PowerShell. cmdlet. tastiera, versione = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="be049-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="be049-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be049-151">OUTPUTS</span></span>

### <span data-ttu-id="be049-152">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="be049-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="be049-153">Note</span><span class="sxs-lookup"><span data-stu-id="be049-153">NOTES</span></span>

## <span data-ttu-id="be049-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be049-154">RELATED LINKS</span></span>
