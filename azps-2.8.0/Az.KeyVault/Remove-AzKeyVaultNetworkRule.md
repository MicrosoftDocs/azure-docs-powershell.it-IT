---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: d7b5f3a7a5a4c2f28724214fb026768979fa9028
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674121"
---
# <span data-ttu-id="ce0f2-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce0f2-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="ce0f2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0f2-103">Rimuove una regola di rete da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="ce0f2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce0f2-104">SYNTAX</span></span>

### <span data-ttu-id="ce0f2-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce0f2-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0f2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ce0f2-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0f2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce0f2-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce0f2-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce0f2-108">DESCRIPTION</span></span>
<span data-ttu-id="ce0f2-109">Rimuove una regola di rete da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="ce0f2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce0f2-110">EXAMPLES</span></span>

### <span data-ttu-id="ce0f2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce0f2-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
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
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="ce0f2-112">Questo comando rimuove una regola di rete dal Vault specificato, a condizione che venga trovata una regola che corrisponda all'indirizzo IP specificato e all'identificatore delle risorse di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="ce0f2-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce0f2-113">PARAMETERS</span></span>

### <span data-ttu-id="ce0f2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0f2-114">-DefaultProfile</span></span>
<span data-ttu-id="ce0f2-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce0f2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce0f2-116">-InputObject</span></span>
<span data-ttu-id="ce0f2-117">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="ce0f2-117">KeyVault object</span></span>

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

### <span data-ttu-id="ce0f2-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="ce0f2-118">-IpAddressRange</span></span>
<span data-ttu-id="ce0f2-119">Specifica l'intervallo di indirizzi IP di rete consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="ce0f2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce0f2-120">-PassThru</span></span>
<span data-ttu-id="ce0f2-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="ce0f2-122">Se questo parametro viene specificato, restituisce l'oggetto Key Vault aggiornato.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="ce0f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="ce0f2-124">Specifica il nome del gruppo di risorse associato al Vault della chiave la cui regola di rete viene modificata.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="ce0f2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ce0f2-125">-ResourceId</span></span>
<span data-ttu-id="ce0f2-126">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="ce0f2-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="ce0f2-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ce0f2-127">-VaultName</span></span>
<span data-ttu-id="ce0f2-128">Specifica il nome di un Vault chiave di cui è in corso la modifica della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="ce0f2-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="ce0f2-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="ce0f2-130">Specifica l'identificatore delle risorse di rete virtuale consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="ce0f2-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce0f2-131">-Confirm</span></span>
<span data-ttu-id="ce0f2-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0f2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0f2-133">-WhatIf</span></span>
<span data-ttu-id="ce0f2-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0f2-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0f2-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0f2-136">CommonParameters</span></span>
<span data-ttu-id="ce0f2-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0f2-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0f2-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce0f2-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0f2-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce0f2-139">INPUTS</span></span>

### <span data-ttu-id="ce0f2-140">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce0f2-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ce0f2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ce0f2-141">System.String</span></span>

## <span data-ttu-id="ce0f2-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce0f2-142">OUTPUTS</span></span>

### <span data-ttu-id="ce0f2-143">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce0f2-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ce0f2-144">Note</span><span class="sxs-lookup"><span data-stu-id="ce0f2-144">NOTES</span></span>

## <span data-ttu-id="ce0f2-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce0f2-145">RELATED LINKS</span></span>