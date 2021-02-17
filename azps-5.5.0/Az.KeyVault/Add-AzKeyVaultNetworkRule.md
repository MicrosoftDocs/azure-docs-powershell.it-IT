---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: c437611603bab6b2c4b9fff5cd0696e306182afa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180495"
---
# <span data-ttu-id="59c1d-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="59c1d-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="59c1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59c1d-102">SYNOPSIS</span></span>
<span data-ttu-id="59c1d-103">Aggiunge una regola destinata a limitare l'accesso a un vault delle chiavi in base all'indirizzo Internet del client.</span><span class="sxs-lookup"><span data-stu-id="59c1d-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="59c1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59c1d-104">SYNTAX</span></span>

### <span data-ttu-id="59c1d-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59c1d-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c1d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="59c1d-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59c1d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="59c1d-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59c1d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="59c1d-108">DESCRIPTION</span></span>
<span data-ttu-id="59c1d-109">Il cmdlet **Add-AzKeyVaultNetworkRule** concede o limita l'accesso a un vault delle chiavi a un set di chiamante designato dai relativi indirizzi IP o dalla rete virtuale a cui appartengono.</span><span class="sxs-lookup"><span data-stu-id="59c1d-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="59c1d-110">La regola potrebbe limitare l'accesso ad altri utenti, applicazioni o gruppi di sicurezza a cui sono state concesse le autorizzazioni tramite i criteri di accesso.</span><span class="sxs-lookup"><span data-stu-id="59c1d-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="59c1d-111">Tenere presente che qualsiasi intervallo IP interno (indirizzi IP privati) non può essere usato per `10.0.0.0-10.255.255.255` aggiungere regole di rete.</span><span class="sxs-lookup"><span data-stu-id="59c1d-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="59c1d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59c1d-112">EXAMPLES</span></span>

### <span data-ttu-id="59c1d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59c1d-113">Example 1</span></span>
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

<span data-ttu-id="59c1d-114">Questo comando aggiunge una regola di rete al vault specificato, consentendo l'accesso all'indirizzo IP specificato dalla rete virtuale identificata da $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="59c1d-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="59c1d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59c1d-115">PARAMETERS</span></span>

### <span data-ttu-id="59c1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59c1d-116">-DefaultProfile</span></span>
<span data-ttu-id="59c1d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59c1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59c1d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59c1d-118">-InputObject</span></span>
<span data-ttu-id="59c1d-119">Oggetto KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1d-119">KeyVault object</span></span>

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

### <span data-ttu-id="59c1d-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="59c1d-120">-IpAddressRange</span></span>
<span data-ttu-id="59c1d-121">Specifica l'intervallo di indirizzi IP di rete consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="59c1d-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="59c1d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59c1d-122">-PassThru</span></span>
<span data-ttu-id="59c1d-123">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="59c1d-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="59c1d-124">Se questa opzione è specificata, restituisce l'oggetto vault della chiave aggiornato.</span><span class="sxs-lookup"><span data-stu-id="59c1d-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="59c1d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59c1d-125">-ResourceGroupName</span></span>
<span data-ttu-id="59c1d-126">Specifica il nome del gruppo di risorse associato al vault della chiave di cui viene modificata la regola di rete.</span><span class="sxs-lookup"><span data-stu-id="59c1d-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="59c1d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59c1d-127">-ResourceId</span></span>
<span data-ttu-id="59c1d-128">ID risorsa KeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1d-128">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="59c1d-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="59c1d-129">-VaultName</span></span>
<span data-ttu-id="59c1d-130">Specifica il nome di un vault delle chiavi la cui regola di rete viene modificata.</span><span class="sxs-lookup"><span data-stu-id="59c1d-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="59c1d-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="59c1d-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="59c1d-132">Specifica l'identificatore di risorsa di rete virtuale consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="59c1d-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="59c1d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59c1d-133">-Confirm</span></span>
<span data-ttu-id="59c1d-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59c1d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59c1d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59c1d-135">-WhatIf</span></span>
<span data-ttu-id="59c1d-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59c1d-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59c1d-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59c1d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59c1d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59c1d-138">CommonParameters</span></span>
<span data-ttu-id="59c1d-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59c1d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59c1d-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="59c1d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59c1d-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="59c1d-141">INPUTS</span></span>

### <span data-ttu-id="59c1d-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1d-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="59c1d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="59c1d-143">System.String</span></span>

## <span data-ttu-id="59c1d-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59c1d-144">OUTPUTS</span></span>

### <span data-ttu-id="59c1d-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="59c1d-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="59c1d-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="59c1d-146">NOTES</span></span>

## <span data-ttu-id="59c1d-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59c1d-147">RELATED LINKS</span></span>
