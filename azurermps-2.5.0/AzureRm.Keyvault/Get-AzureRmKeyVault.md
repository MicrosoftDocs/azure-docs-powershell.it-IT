---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 7cbcf722b71919096ca2c7d1dc3201ad2fe42f2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866687"
---
# <span data-ttu-id="4fb71-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="4fb71-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="4fb71-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fb71-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb71-103">Ottiene i Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="4fb71-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fb71-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fb71-104">SYNTAX</span></span>

### <span data-ttu-id="4fb71-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="4fb71-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb71-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="4fb71-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb71-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4fb71-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4fb71-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="4fb71-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4fb71-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="4fb71-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb71-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fb71-110">DESCRIPTION</span></span>
<span data-ttu-id="4fb71-111">Il cmdlet **Get-AzureRmKeyVault** ottiene le informazioni sui Vault chiave di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4fb71-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="4fb71-112">È possibile visualizzare tutte le istanze delle volte chiave in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un particolare Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="4fb71-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="4fb71-113">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet quando si riceve un singolo Vault chiave, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="4fb71-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="4fb71-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fb71-114">EXAMPLES</span></span>

### <span data-ttu-id="4fb71-115">Esempio 1: ottenere tutti i Vault chiave nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4fb71-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="4fb71-116">Questo comando consente di ottenere tutti i Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4fb71-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="4fb71-117">Esempio 2: ottenere un Vault chiave specifico</span><span class="sxs-lookup"><span data-stu-id="4fb71-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="4fb71-118">Questo comando ottiene il Vault chiave denominato Contoso03Vault nell'abbonamento corrente e lo archivia nella variabile $MyVault.</span><span class="sxs-lookup"><span data-stu-id="4fb71-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="4fb71-119">Puoi ispezionare le proprietà di $MyVault per ottenere informazioni dettagliate sul Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="4fb71-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="4fb71-120">Esempio 3: ottenere i Vault chiave in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4fb71-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="4fb71-121">Questo comando consente di ottenere tutte le volte chiave nel gruppo di risorse denominato ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="4fb71-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="4fb71-122">Esempio 4: ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="4fb71-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="4fb71-123">Questo comando consente di ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="4fb71-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="4fb71-124">Esempio 5: ottenere un Vault Key eliminato</span><span class="sxs-lookup"><span data-stu-id="4fb71-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="4fb71-125">Questo comando consente di ottenere le informazioni sul Vault chiave eliminate denominate Contoso03Vault nell'abbonamento corrente e nell'area geografica di eastus2.</span><span class="sxs-lookup"><span data-stu-id="4fb71-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="4fb71-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fb71-126">PARAMETERS</span></span>

### <span data-ttu-id="4fb71-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb71-127">-DefaultProfile</span></span>
<span data-ttu-id="4fb71-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4fb71-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4fb71-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4fb71-129">-InRemovedState</span></span>
<span data-ttu-id="4fb71-130">Specifica se visualizzare i Vault eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="4fb71-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="4fb71-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="4fb71-131">-Location</span></span>
<span data-ttu-id="4fb71-132">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="4fb71-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb71-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb71-133">-ResourceGroupName</span></span>
<span data-ttu-id="4fb71-134">Specifica il nome del gruppo di risorse associato alla chiave Vault o alle volte chiave in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="4fb71-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb71-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="4fb71-135">-Tag</span></span>
<span data-ttu-id="4fb71-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4fb71-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4fb71-137">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="4fb71-137">For example:</span></span>

<span data-ttu-id="4fb71-138">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4fb71-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4fb71-139">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="4fb71-139">-VaultName</span></span>
<span data-ttu-id="4fb71-140">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="4fb71-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb71-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb71-141">CommonParameters</span></span>
<span data-ttu-id="4fb71-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fb71-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb71-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb71-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb71-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fb71-144">INPUTS</span></span>

## <span data-ttu-id="4fb71-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fb71-145">OUTPUTS</span></span>

### <span data-ttu-id="4fb71-146">Microsoft. Azure. Commands. Vault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="4fb71-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="4fb71-147">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="4fb71-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="4fb71-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="4fb71-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="4fb71-149">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="4fb71-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="4fb71-150">Note</span><span class="sxs-lookup"><span data-stu-id="4fb71-150">NOTES</span></span>

## <span data-ttu-id="4fb71-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fb71-151">RELATED LINKS</span></span>

[<span data-ttu-id="4fb71-152">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="4fb71-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="4fb71-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="4fb71-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
