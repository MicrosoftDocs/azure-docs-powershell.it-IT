---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 37ed0c0cb29e69aa2e8018bb193fa4c82b0c3bcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192399"
---
# <span data-ttu-id="3fcc3-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fcc3-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="3fcc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fcc3-102">SYNOPSIS</span></span>
<span data-ttu-id="3fcc3-103">Recupera i vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-103">Gets key vaults.</span></span>

## <span data-ttu-id="3fcc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fcc3-104">SYNTAX</span></span>

### <span data-ttu-id="3fcc3-105">GetVaultByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3fcc3-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fcc3-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="3fcc3-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3fcc3-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="3fcc3-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fcc3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3fcc3-108">DESCRIPTION</span></span>
<span data-ttu-id="3fcc3-109">Il cmdlet **Get-AzKeyVault** ottiene informazioni sui vault delle chiavi in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="3fcc3-110">È possibile visualizzare tutte le istanze di vault chiave in una sottoscrizione oppure filtrare i risultati in base a un gruppo di risorse o a un particolare vault chiave.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="3fcc3-111">Anche se è facoltativo specificare il gruppo di risorse per questo cmdlet quando si ottiene un singolo vault con chiavi, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="3fcc3-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fcc3-112">EXAMPLES</span></span>

### <span data-ttu-id="3fcc3-113">Esempio 1: Ottenere tutti i vault chiave nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="3fcc3-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="3fcc3-114">Questo comando recupera tutti i vault delle chiavi nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="3fcc3-115">Esempio 2: Ottenere un vault delle chiavi specifico</span><span class="sxs-lookup"><span data-stu-id="3fcc3-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
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

Tags                             :
```

<span data-ttu-id="3fcc3-116">Questo comando recupera la chiave vault denominata myvault nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="3fcc3-117">Esempio 3: Ottenere vault chiave in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3fcc3-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="3fcc3-118">Questo comando recupera tutti i vault delle chiavi nel gruppo di risorse denominato ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="3fcc3-119">Esempio 4: Ottenere tutti gli vault delle chiavi eliminati nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="3fcc3-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="3fcc3-120">Questo comando recupera tutti i vault delle chiavi eliminati nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="3fcc3-121">Esempio 5: Ottenere un vault delle chiavi eliminato</span><span class="sxs-lookup"><span data-stu-id="3fcc3-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="3fcc3-122">Questo comando recupera le informazioni chiave del vault eliminate denominate myvault4 nell'abbonamento corrente e nell'area ovest.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="3fcc3-123">Esempio 6: Ottenere vault delle chiavi con i filtri</span><span class="sxs-lookup"><span data-stu-id="3fcc3-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="3fcc3-124">Questo comando recupera tutti i vault chiave dell'abbonamento che iniziano con "myvault".</span><span class="sxs-lookup"><span data-stu-id="3fcc3-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="3fcc3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fcc3-125">PARAMETERS</span></span>

### <span data-ttu-id="3fcc3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fcc3-126">-DefaultProfile</span></span>
<span data-ttu-id="3fcc3-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="3fcc3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fcc3-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="3fcc3-128">-InRemovedState</span></span>
<span data-ttu-id="3fcc3-129">Specifica se visualizzare nell'output i vault eliminati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fcc3-130">-Location</span><span class="sxs-lookup"><span data-stu-id="3fcc3-130">-Location</span></span>
<span data-ttu-id="3fcc3-131">Posizione del vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fcc3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fcc3-132">-ResourceGroupName</span></span>
<span data-ttu-id="3fcc3-133">Specifica il nome del gruppo di risorse associato al vault delle chiavi o ai vault delle chiavi in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3fcc3-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="3fcc3-134">-Tag</span></span>
<span data-ttu-id="3fcc3-135">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3fcc3-136">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3fcc3-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fcc3-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3fcc3-137">-VaultName</span></span>
<span data-ttu-id="3fcc3-138">Specifica il nome del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="3fcc3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fcc3-139">CommonParameters</span></span>
<span data-ttu-id="3fcc3-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fcc3-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3fcc3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fcc3-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="3fcc3-142">INPUTS</span></span>

### <span data-ttu-id="3fcc3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3fcc3-143">System.String</span></span>

### <span data-ttu-id="3fcc3-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3fcc3-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3fcc3-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fcc3-145">OUTPUTS</span></span>

### <span data-ttu-id="3fcc3-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fcc3-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3fcc3-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3fcc3-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="3fcc3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fcc3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="3fcc3-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="3fcc3-149">NOTES</span></span>

## <span data-ttu-id="3fcc3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fcc3-150">RELATED LINKS</span></span>

[<span data-ttu-id="3fcc3-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fcc3-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="3fcc3-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fcc3-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
