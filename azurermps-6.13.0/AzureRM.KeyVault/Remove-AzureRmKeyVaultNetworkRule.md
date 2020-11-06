---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: f1ff73a753c794ce7528c9af2b480f75d1460815
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515195"
---
# <span data-ttu-id="8697b-101">Remove-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8697b-101">Remove-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="8697b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8697b-102">SYNOPSIS</span></span>
<span data-ttu-id="8697b-103">Rimuove una regola di rete da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8697b-103">Removes a network rule from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8697b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8697b-104">SYNTAX</span></span>

### <span data-ttu-id="8697b-105">ByVaultName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8697b-105">ByVaultName (Default)</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8697b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8697b-106">ByInputObject</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8697b-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8697b-107">ByResourceId</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8697b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8697b-108">DESCRIPTION</span></span>
<span data-ttu-id="8697b-109">Rimuove una regola di rete da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8697b-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="8697b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8697b-110">EXAMPLES</span></span>

### <span data-ttu-id="8697b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8697b-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzureRmKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="8697b-112">Questo comando rimuove una regola di rete dal Vault specificato, a condizione che venga trovata una regola che corrisponda all'indirizzo IP specificato e all'identificatore delle risorse di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="8697b-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="8697b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8697b-113">PARAMETERS</span></span>

### <span data-ttu-id="8697b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8697b-114">-DefaultProfile</span></span>
<span data-ttu-id="8697b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8697b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8697b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8697b-116">-InputObject</span></span>
<span data-ttu-id="8697b-117">Oggetto Vault</span><span class="sxs-lookup"><span data-stu-id="8697b-117">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8697b-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8697b-118">-IpAddressRange</span></span>
<span data-ttu-id="8697b-119">Specifica l'intervallo di indirizzi IP di rete consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="8697b-119">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8697b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8697b-120">-PassThru</span></span>
<span data-ttu-id="8697b-121">Questo cmdlet non restituisce un oggetto per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="8697b-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="8697b-122">Se questo parametro viene specificato, restituisce l'oggetto Key Vault aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8697b-122">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8697b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8697b-123">-ResourceGroupName</span></span>
<span data-ttu-id="8697b-124">Specifica il nome del gruppo di risorse associato al Vault della chiave la cui regola di rete viene modificata.</span><span class="sxs-lookup"><span data-stu-id="8697b-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8697b-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8697b-125">-ResourceId</span></span>
<span data-ttu-id="8697b-126">ID risorsa di un Vault</span><span class="sxs-lookup"><span data-stu-id="8697b-126">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8697b-127">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8697b-127">-VaultName</span></span>
<span data-ttu-id="8697b-128">Specifica il nome di un Vault chiave di cui è in corso la modifica della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="8697b-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8697b-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8697b-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="8697b-130">Specifica l'identificatore delle risorse di rete virtuale consentito della regola di rete.</span><span class="sxs-lookup"><span data-stu-id="8697b-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8697b-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8697b-131">-Confirm</span></span>
<span data-ttu-id="8697b-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8697b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8697b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8697b-133">-WhatIf</span></span>
<span data-ttu-id="8697b-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8697b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8697b-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8697b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8697b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8697b-136">CommonParameters</span></span>
<span data-ttu-id="8697b-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8697b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8697b-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8697b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8697b-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8697b-139">INPUTS</span></span>

### <span data-ttu-id="8697b-140">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8697b-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8697b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8697b-141">OUTPUTS</span></span>

### <span data-ttu-id="8697b-142">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8697b-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8697b-143">Note</span><span class="sxs-lookup"><span data-stu-id="8697b-143">NOTES</span></span>

## <span data-ttu-id="8697b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8697b-144">RELATED LINKS</span></span>