---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-Azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: aaace602cd50f9464021b1dcbefe39272e1621bb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861317"
---
# <span data-ttu-id="19cb0-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="19cb0-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="19cb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="19cb0-103">Ottiene i Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19cb0-103">Gets key vaults.</span></span>

## <span data-ttu-id="19cb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19cb0-104">SYNTAX</span></span>

### <span data-ttu-id="19cb0-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="19cb0-105">GetVaultByName</span></span>
```
Get-AzKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19cb0-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="19cb0-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19cb0-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="19cb0-107">ListVaultsByResourceGroup</span></span>
```
Get-AzKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="19cb0-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="19cb0-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19cb0-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="19cb0-109">ListAllVaultsInSubscription</span></span>
```
Get-AzKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19cb0-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19cb0-110">DESCRIPTION</span></span>
<span data-ttu-id="19cb0-111">Il cmdlet **Get-AzKeyVault** ottiene le informazioni sui Vault chiave di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="19cb0-111">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="19cb0-112">È possibile visualizzare tutte le istanze delle volte chiave in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un particolare Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19cb0-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="19cb0-113">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet quando si riceve un singolo Vault chiave, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="19cb0-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="19cb0-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19cb0-114">EXAMPLES</span></span>

### <span data-ttu-id="19cb0-115">Esempio 1: ottenere tutti i Vault chiave nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="19cb0-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault
```

<span data-ttu-id="19cb0-116">Questo comando consente di ottenere tutti i Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="19cb0-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="19cb0-117">Esempio 2: ottenere un Vault chiave specifico</span><span class="sxs-lookup"><span data-stu-id="19cb0-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="19cb0-118">Questo comando ottiene il Vault chiave denominato Contoso03Vault nell'abbonamento corrente e lo archivia nella variabile $MyVault.</span><span class="sxs-lookup"><span data-stu-id="19cb0-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="19cb0-119">Puoi ispezionare le proprietà di $MyVault per ottenere informazioni dettagliate sul Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19cb0-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="19cb0-120">Esempio 3: ottenere i Vault chiave in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="19cb0-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="19cb0-121">Questo comando consente di ottenere tutte le volte chiave nel gruppo di risorse denominato ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="19cb0-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="19cb0-122">Esempio 4: ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="19cb0-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzKeyVault -InRemovedState
```

<span data-ttu-id="19cb0-123">Questo comando consente di ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="19cb0-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="19cb0-124">Esempio 5: ottenere un Vault Key eliminato</span><span class="sxs-lookup"><span data-stu-id="19cb0-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="19cb0-125">Questo comando consente di ottenere le informazioni sul Vault chiave eliminate denominate Contoso03Vault nell'abbonamento corrente e nell'area geografica di eastus2.</span><span class="sxs-lookup"><span data-stu-id="19cb0-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="19cb0-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19cb0-126">PARAMETERS</span></span>

### <span data-ttu-id="19cb0-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19cb0-127">-DefaultProfile</span></span>
<span data-ttu-id="19cb0-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="19cb0-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19cb0-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="19cb0-129">-InRemovedState</span></span>
<span data-ttu-id="19cb0-130">Specifica se visualizzare i Vault eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="19cb0-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="19cb0-131">-Posizione</span><span class="sxs-lookup"><span data-stu-id="19cb0-131">-Location</span></span>
<span data-ttu-id="19cb0-132">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="19cb0-132">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="19cb0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19cb0-133">-ResourceGroupName</span></span>
<span data-ttu-id="19cb0-134">Specifica il nome del gruppo di risorse associato alla chiave Vault o alle volte chiave in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="19cb0-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="19cb0-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="19cb0-135">-Tag</span></span>
<span data-ttu-id="19cb0-136">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="19cb0-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="19cb0-137">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="19cb0-137">For example:</span></span>

<span data-ttu-id="19cb0-138">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="19cb0-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="19cb0-139">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="19cb0-139">-VaultName</span></span>
<span data-ttu-id="19cb0-140">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="19cb0-140">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="19cb0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19cb0-141">CommonParameters</span></span>
<span data-ttu-id="19cb0-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19cb0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19cb0-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19cb0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19cb0-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19cb0-144">INPUTS</span></span>

### <span data-ttu-id="19cb0-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="19cb0-145">None</span></span>
<span data-ttu-id="19cb0-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="19cb0-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19cb0-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19cb0-147">OUTPUTS</span></span>

### <span data-ttu-id="19cb0-148">Microsoft. Azure. Commands. Vault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="19cb0-148">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="19cb0-149">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="19cb0-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="19cb0-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="19cb0-150">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="19cb0-151">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="19cb0-151">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="19cb0-152">Note</span><span class="sxs-lookup"><span data-stu-id="19cb0-152">NOTES</span></span>

## <span data-ttu-id="19cb0-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19cb0-153">RELATED LINKS</span></span>

[<span data-ttu-id="19cb0-154">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="19cb0-154">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="19cb0-155">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="19cb0-155">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
