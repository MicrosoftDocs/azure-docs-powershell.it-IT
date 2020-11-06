---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521915"
---
# <span data-ttu-id="86ff6-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="86ff6-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="86ff6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="86ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="86ff6-103">Ottiene i Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="86ff6-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86ff6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86ff6-104">SYNTAX</span></span>

### <span data-ttu-id="86ff6-105">ListAllVaultsInSubscription (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="86ff6-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86ff6-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="86ff6-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86ff6-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="86ff6-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86ff6-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="86ff6-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86ff6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86ff6-109">DESCRIPTION</span></span>
<span data-ttu-id="86ff6-110">Il cmdlet **Get-AzureRmKeyVault** ottiene le informazioni sui Vault chiave di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="86ff6-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="86ff6-111">È possibile visualizzare tutte le istanze delle volte chiave in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un particolare Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="86ff6-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="86ff6-112">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet quando si riceve un singolo Vault chiave, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="86ff6-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="86ff6-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86ff6-113">EXAMPLES</span></span>

### <span data-ttu-id="86ff6-114">Esempio 1: ottenere tutti i Vault chiave nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="86ff6-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="86ff6-115">Questo comando consente di ottenere tutti i Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="86ff6-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="86ff6-116">Esempio 2: ottenere un Vault chiave specifico</span><span class="sxs-lookup"><span data-stu-id="86ff6-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="86ff6-117">Questo comando ottiene il Vault chiave denominato Contoso03Vault nell'abbonamento corrente e lo archivia nella variabile $MyVault.</span><span class="sxs-lookup"><span data-stu-id="86ff6-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="86ff6-118">Puoi ispezionare le proprietà di $MyVault per ottenere informazioni dettagliate sul Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="86ff6-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="86ff6-119">Esempio 3: ottenere i Vault chiave in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="86ff6-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="86ff6-120">Questo comando consente di ottenere tutte le volte chiave nel gruppo di risorse denominato ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="86ff6-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="86ff6-121">Esempio 4: ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="86ff6-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="86ff6-122">Questo comando consente di ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="86ff6-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="86ff6-123">Esempio 5: ottenere un Vault Key eliminato</span><span class="sxs-lookup"><span data-stu-id="86ff6-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="86ff6-124">Questo comando consente di ottenere le informazioni sul Vault chiave eliminate denominate Contoso03Vault nell'abbonamento corrente e nell'area geografica di eastus2.</span><span class="sxs-lookup"><span data-stu-id="86ff6-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="86ff6-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="86ff6-125">PARAMETERS</span></span>

### <span data-ttu-id="86ff6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ff6-126">-DefaultProfile</span></span>
<span data-ttu-id="86ff6-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="86ff6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86ff6-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="86ff6-128">-InRemovedState</span></span>
<span data-ttu-id="86ff6-129">Specifica se visualizzare i Vault eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="86ff6-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ff6-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="86ff6-130">-Location</span></span>
<span data-ttu-id="86ff6-131">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="86ff6-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ff6-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ff6-132">-ResourceGroupName</span></span>
<span data-ttu-id="86ff6-133">Specifica il nome del gruppo di risorse associato alla chiave Vault o alle volte chiave in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="86ff6-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ff6-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="86ff6-134">-Tag</span></span>
<span data-ttu-id="86ff6-135">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="86ff6-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="86ff6-136">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="86ff6-136">For example:</span></span>

<span data-ttu-id="86ff6-137">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="86ff6-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ff6-138">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="86ff6-138">-VaultName</span></span>
<span data-ttu-id="86ff6-139">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="86ff6-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ff6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ff6-140">CommonParameters</span></span>
<span data-ttu-id="86ff6-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ff6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ff6-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ff6-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ff6-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="86ff6-143">INPUTS</span></span>

### <span data-ttu-id="86ff6-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="86ff6-144">None</span></span>
<span data-ttu-id="86ff6-145">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="86ff6-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86ff6-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86ff6-146">OUTPUTS</span></span>

### <span data-ttu-id="86ff6-147">Microsoft. Azure. Commands. Vault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="86ff6-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="86ff6-148">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="86ff6-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="86ff6-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="86ff6-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="86ff6-150">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="86ff6-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="86ff6-151">Note</span><span class="sxs-lookup"><span data-stu-id="86ff6-151">NOTES</span></span>

## <span data-ttu-id="86ff6-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86ff6-152">RELATED LINKS</span></span>

[<span data-ttu-id="86ff6-153">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="86ff6-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="86ff6-154">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="86ff6-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
