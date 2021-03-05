---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 84148d675b5c6bc43a883ecd5c419b5019de49d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013005"
---
# <span data-ttu-id="4f93d-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4f93d-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="4f93d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f93d-102">SYNOPSIS</span></span>
<span data-ttu-id="4f93d-103">Recupera i vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="4f93d-103">Gets key vaults.</span></span>

## <span data-ttu-id="4f93d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f93d-104">SYNTAX</span></span>

### <span data-ttu-id="4f93d-105">GetVaultByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f93d-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f93d-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="4f93d-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f93d-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="4f93d-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f93d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4f93d-108">DESCRIPTION</span></span>
<span data-ttu-id="4f93d-109">Il cmdlet **Get-AzKeyVault** ottiene informazioni sui vault delle chiavi in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4f93d-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="4f93d-110">È possibile visualizzare tutte le istanze di vault chiave in una sottoscrizione oppure filtrare i risultati in base a un gruppo di risorse o a un particolare vault chiave.</span><span class="sxs-lookup"><span data-stu-id="4f93d-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="4f93d-111">Anche se è facoltativo specificare il gruppo di risorse per questo cmdlet quando si ottiene un singolo vault con chiavi, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="4f93d-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="4f93d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f93d-112">EXAMPLES</span></span>

### <span data-ttu-id="4f93d-113">Esempio 1: Ottenere tutti i vault delle chiavi nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4f93d-113">Example 1: Get all key vaults in your current subscription</span></span>
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

<span data-ttu-id="4f93d-114">Questo comando recupera tutti i vault delle chiavi nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4f93d-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="4f93d-115">Esempio 2: Ottenere un vault delle chiavi specifico</span><span class="sxs-lookup"><span data-stu-id="4f93d-115">Example 2: Get a specific key vault</span></span>
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

<span data-ttu-id="4f93d-116">Questo comando recupera la chiave vault denominata myvault nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4f93d-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="4f93d-117">Esempio 3: Ottenere vault chiave in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4f93d-117">Example 3: Get key vaults in a resource group</span></span>
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

<span data-ttu-id="4f93d-118">Questo comando recupera tutti i vault delle chiavi nel gruppo di risorse denominato ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4f93d-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="4f93d-119">Esempio 4: Ottenere tutti gli vault delle chiavi eliminati nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4f93d-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
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

<span data-ttu-id="4f93d-120">Questo comando recupera tutti i vault delle chiavi eliminati nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4f93d-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="4f93d-121">Esempio 5: Ottenere un vault delle chiavi eliminato</span><span class="sxs-lookup"><span data-stu-id="4f93d-121">Example 5: Get a deleted key vault</span></span>
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

<span data-ttu-id="4f93d-122">Questo comando recupera le informazioni chiave del vault eliminate denominate myvault4 nell'abbonamento corrente e nell'area ovest.</span><span class="sxs-lookup"><span data-stu-id="4f93d-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="4f93d-123">Esempio 6: Ottenere vault delle chiavi con i filtri</span><span class="sxs-lookup"><span data-stu-id="4f93d-123">Example 6: Get key vaults using filtering</span></span>
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

<span data-ttu-id="4f93d-124">Questo comando recupera tutti i vault chiave dell'abbonamento che iniziano con "miovaultato".</span><span class="sxs-lookup"><span data-stu-id="4f93d-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="4f93d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f93d-125">PARAMETERS</span></span>

### <span data-ttu-id="4f93d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f93d-126">-DefaultProfile</span></span>
<span data-ttu-id="4f93d-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4f93d-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f93d-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4f93d-128">-InRemovedState</span></span>
<span data-ttu-id="4f93d-129">Specifica se visualizzare nell'output i vault eliminati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="4f93d-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="4f93d-130">-Location</span><span class="sxs-lookup"><span data-stu-id="4f93d-130">-Location</span></span>
<span data-ttu-id="4f93d-131">Posizione del vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="4f93d-131">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="4f93d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f93d-132">-ResourceGroupName</span></span>
<span data-ttu-id="4f93d-133">Specifica il nome del gruppo di risorse associato al vault delle chiavi o ai vault delle chiavi in cui eseguire la query.</span><span class="sxs-lookup"><span data-stu-id="4f93d-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="4f93d-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f93d-134">-Tag</span></span>
<span data-ttu-id="4f93d-135">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4f93d-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4f93d-136">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4f93d-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4f93d-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4f93d-137">-VaultName</span></span>
<span data-ttu-id="4f93d-138">Specifica il nome del vault della chiave.</span><span class="sxs-lookup"><span data-stu-id="4f93d-138">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="4f93d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f93d-139">CommonParameters</span></span>
<span data-ttu-id="4f93d-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f93d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f93d-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f93d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f93d-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="4f93d-142">INPUTS</span></span>

### <span data-ttu-id="4f93d-143">System.String</span><span class="sxs-lookup"><span data-stu-id="4f93d-143">System.String</span></span>

### <span data-ttu-id="4f93d-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f93d-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f93d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f93d-145">OUTPUTS</span></span>

### <span data-ttu-id="4f93d-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4f93d-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="4f93d-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4f93d-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="4f93d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="4f93d-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="4f93d-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="4f93d-149">NOTES</span></span>

## <span data-ttu-id="4f93d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f93d-150">RELATED LINKS</span></span>

[<span data-ttu-id="4f93d-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4f93d-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="4f93d-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4f93d-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
