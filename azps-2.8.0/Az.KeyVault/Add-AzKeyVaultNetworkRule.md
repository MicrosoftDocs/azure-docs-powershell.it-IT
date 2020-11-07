---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: fd93a933b394fc8729186c7ea78c737123149bf2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674179"
---
# <span data-ttu-id="9e802-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9e802-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="9e802-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e802-102">SYNOPSIS</span></span>
<span data-ttu-id="9e802-103">Aggiunge una regola che consente di limitare l'accesso a un Vault chiave in base all'indirizzo Internet del client.</span><span class="sxs-lookup"><span data-stu-id="9e802-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="9e802-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e802-104">SYNTAX</span></span>

### <span data-ttu-id="9e802-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e802-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e802-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9e802-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e802-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9e802-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e802-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e802-108">DESCRIPTION</span></span>
<span data-ttu-id="9e802-109">Il cmdlet **Add-AzKeyVaultNetworkRule** concede o limita l'accesso a un Vault chiave a un set di chiamante designato dagli indirizzi IP o dalla rete virtuale a cui appartengono.</span><span class="sxs-lookup"><span data-stu-id="9e802-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="9e802-110">La regola offre la possibilità di limitare l'accesso ad altri utenti, applicazioni o gruppi di sicurezza a cui sono state concesse le autorizzazioni tramite i criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="9e802-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="9e802-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e802-111">EXAMPLES</span></span>

### <span data-ttu-id="9e802-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9e802-112">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="9e802-113">Questo comando aggiunge una regola di rete al Vault specificato, consentendo l'accesso all'indirizzo IP specificato dalla rete virtuale identificata da $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="9e802-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="9e802-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e802-114">PARAMETERS</span></span>

### <span data-ttu-id="9e802-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e802-115">-DefaultProfile</span></span>
<span data-ttu-id="9e802-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e802-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e802-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e802-117">-InputObject</span></span>
<span data-ttu-id="9e802-118">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="9e802-118">KeyVault object</span></span>

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

### <span data-ttu-id="9e802-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="9e802-119">-IpAddressRange</span></span>
<span data-ttu-id="9e802-120">Specifica l'intervallo di indirizzi IP di rete consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="9e802-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="9e802-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e802-121">-PassThru</span></span>
<span data-ttu-id="9e802-122">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="9e802-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="9e802-123">Se questo parametro viene specificato, restituisce l'oggetto Key Vault aggiornato.</span><span class="sxs-lookup"><span data-stu-id="9e802-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="9e802-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e802-124">-ResourceGroupName</span></span>
<span data-ttu-id="9e802-125">Specifica il nome del gruppo di risorse associato al Vault della chiave la cui regola di rete viene modificata.</span><span class="sxs-lookup"><span data-stu-id="9e802-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="9e802-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e802-126">-ResourceId</span></span>
<span data-ttu-id="9e802-127">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="9e802-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="9e802-128">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="9e802-128">-VaultName</span></span>
<span data-ttu-id="9e802-129">Specifica il nome di un Vault chiave di cui è in corso la modifica della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="9e802-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="9e802-130">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9e802-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9e802-131">Specifica l'identificatore delle risorse di rete virtuale consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="9e802-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="9e802-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e802-132">-Confirm</span></span>
<span data-ttu-id="9e802-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e802-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e802-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e802-134">-WhatIf</span></span>
<span data-ttu-id="9e802-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e802-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e802-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e802-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e802-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e802-137">CommonParameters</span></span>
<span data-ttu-id="9e802-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e802-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e802-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e802-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e802-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e802-140">INPUTS</span></span>

### <span data-ttu-id="9e802-141">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9e802-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9e802-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9e802-142">System.String</span></span>

## <span data-ttu-id="9e802-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e802-143">OUTPUTS</span></span>

### <span data-ttu-id="9e802-144">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9e802-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9e802-145">Note</span><span class="sxs-lookup"><span data-stu-id="9e802-145">NOTES</span></span>

## <span data-ttu-id="9e802-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e802-146">RELATED LINKS</span></span>
