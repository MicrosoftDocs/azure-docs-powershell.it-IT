---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 795840d7580d1e7dabb15cf3211ef16d0ccfb7b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835771"
---
# <span data-ttu-id="8403b-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8403b-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="8403b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8403b-102">SYNOPSIS</span></span>
<span data-ttu-id="8403b-103">Ottiene i Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8403b-103">Gets key vaults.</span></span>

## <span data-ttu-id="8403b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8403b-104">SYNTAX</span></span>

### <span data-ttu-id="8403b-105">GetVaultByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8403b-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8403b-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="8403b-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8403b-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="8403b-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8403b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8403b-108">DESCRIPTION</span></span>
<span data-ttu-id="8403b-109">Il cmdlet **Get-AzKeyVault** ottiene le informazioni sui Vault chiave di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="8403b-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="8403b-110">È possibile visualizzare tutte le istanze delle volte chiave in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un particolare Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8403b-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="8403b-111">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet quando si riceve un singolo Vault chiave, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="8403b-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="8403b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8403b-112">EXAMPLES</span></span>

### <span data-ttu-id="8403b-113">Esempio 1: ottenere tutti i Vault chiave nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="8403b-113">Example 1: Get all key vaults in your current subscription</span></span>
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

<span data-ttu-id="8403b-114">Questo comando consente di ottenere tutti i Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8403b-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="8403b-115">Esempio 2: ottenere un Vault chiave specifico</span><span class="sxs-lookup"><span data-stu-id="8403b-115">Example 2: Get a specific key vault</span></span>
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

<span data-ttu-id="8403b-116">Questo comando consente di ottenere il Vault della chiave denominato Vault nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8403b-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="8403b-117">Esempio 3: ottenere i Vault chiave in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8403b-117">Example 3: Get key vaults in a resource group</span></span>
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

<span data-ttu-id="8403b-118">Questo comando consente di ottenere tutte le volte chiave nel gruppo di risorse denominato ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8403b-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="8403b-119">Esempio 4: ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="8403b-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
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

<span data-ttu-id="8403b-120">Questo comando consente di ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="8403b-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="8403b-121">Esempio 5: ottenere un Vault Key eliminato</span><span class="sxs-lookup"><span data-stu-id="8403b-121">Example 5: Get a deleted key vault</span></span>
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

<span data-ttu-id="8403b-122">Questo comando consente di ottenere le informazioni di archiviazione chiave eliminate denominate myvault4 nell'abbonamento corrente e nell'area di westus.</span><span class="sxs-lookup"><span data-stu-id="8403b-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="8403b-123">Esempio 6: ottenere i Vault chiave usando il filtro</span><span class="sxs-lookup"><span data-stu-id="8403b-123">Example 6: Get key vaults using filtering</span></span>
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

<span data-ttu-id="8403b-124">Questo comando consente di ottenere tutti i Vault chiave nell'abbonamento che iniziano con "Vault".</span><span class="sxs-lookup"><span data-stu-id="8403b-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="8403b-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8403b-125">PARAMETERS</span></span>

### <span data-ttu-id="8403b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8403b-126">-DefaultProfile</span></span>
<span data-ttu-id="8403b-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8403b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8403b-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8403b-128">-InRemovedState</span></span>
<span data-ttu-id="8403b-129">Specifica se visualizzare i Vault eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="8403b-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="8403b-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8403b-130">-Location</span></span>
<span data-ttu-id="8403b-131">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="8403b-131">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="8403b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8403b-132">-ResourceGroupName</span></span>
<span data-ttu-id="8403b-133">Specifica il nome del gruppo di risorse associato alla chiave Vault o alle volte chiave in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="8403b-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="8403b-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="8403b-134">-Tag</span></span>
<span data-ttu-id="8403b-135">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8403b-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8403b-136">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8403b-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8403b-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="8403b-137">-VaultName</span></span>
<span data-ttu-id="8403b-138">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="8403b-138">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="8403b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8403b-139">CommonParameters</span></span>
<span data-ttu-id="8403b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8403b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8403b-141">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8403b-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8403b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8403b-142">INPUTS</span></span>

### <span data-ttu-id="8403b-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8403b-143">System.String</span></span>

### <span data-ttu-id="8403b-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8403b-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8403b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8403b-145">OUTPUTS</span></span>

### <span data-ttu-id="8403b-146">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8403b-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8403b-147">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8403b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="8403b-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="8403b-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="8403b-149">Note</span><span class="sxs-lookup"><span data-stu-id="8403b-149">NOTES</span></span>

## <span data-ttu-id="8403b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8403b-150">RELATED LINKS</span></span>

[<span data-ttu-id="8403b-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8403b-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="8403b-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8403b-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
