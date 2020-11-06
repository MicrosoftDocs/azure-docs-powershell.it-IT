---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510588"
---
# <span data-ttu-id="678c6-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="678c6-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="678c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="678c6-102">SYNOPSIS</span></span>
<span data-ttu-id="678c6-103">Ottiene i Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="678c6-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="678c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="678c6-104">SYNTAX</span></span>

### <span data-ttu-id="678c6-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="678c6-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678c6-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="678c6-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678c6-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="678c6-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="678c6-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="678c6-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="678c6-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="678c6-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="678c6-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="678c6-110">DESCRIPTION</span></span>
<span data-ttu-id="678c6-111">Il cmdlet **Get-AzureRmKeyVault** ottiene le informazioni sui Vault chiave di un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="678c6-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="678c6-112">È possibile visualizzare tutte le istanze delle volte chiave in un abbonamento o filtrare i risultati in base a un gruppo di risorse o a un particolare Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="678c6-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="678c6-113">Tieni presente che, anche se specificando il gruppo di risorse è facoltativo per questo cmdlet quando si riceve un singolo Vault chiave, è consigliabile farlo per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="678c6-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="678c6-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="678c6-114">EXAMPLES</span></span>

### <span data-ttu-id="678c6-115">Esempio 1: ottenere tutti i Vault chiave nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="678c6-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="678c6-116">Questo comando consente di ottenere tutti i Vault chiave nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="678c6-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="678c6-117">Esempio 2: ottenere un Vault chiave specifico</span><span class="sxs-lookup"><span data-stu-id="678c6-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="678c6-118">Questo comando ottiene il Vault chiave denominato Contoso03Vault nell'abbonamento corrente e lo archivia nella variabile $MyVault.</span><span class="sxs-lookup"><span data-stu-id="678c6-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="678c6-119">Puoi ispezionare le proprietà di $MyVault per ottenere informazioni dettagliate sul Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="678c6-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="678c6-120">Esempio 3: ottenere i Vault chiave in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="678c6-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="678c6-121">Questo comando consente di ottenere tutte le volte chiave nel gruppo di risorse denominato ContosoPayRollResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="678c6-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="678c6-122">Esempio 4: ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente</span><span class="sxs-lookup"><span data-stu-id="678c6-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="678c6-123">Questo comando consente di ottenere tutti gli archivi chiave eliminati nell'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="678c6-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="678c6-124">Esempio 5: ottenere un Vault Key eliminato</span><span class="sxs-lookup"><span data-stu-id="678c6-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="678c6-125">Questo comando consente di ottenere le informazioni sul Vault chiave eliminate denominate Contoso03Vault nell'abbonamento corrente e nell'area geografica di eastus2.</span><span class="sxs-lookup"><span data-stu-id="678c6-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="678c6-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="678c6-126">PARAMETERS</span></span>

### <span data-ttu-id="678c6-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="678c6-127">-InRemovedState</span></span>
<span data-ttu-id="678c6-128">Specifica se visualizzare i Vault eliminati in precedenza nell'output.</span><span class="sxs-lookup"><span data-stu-id="678c6-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="678c6-129">-Posizione</span><span class="sxs-lookup"><span data-stu-id="678c6-129">-Location</span></span>
<span data-ttu-id="678c6-130">Posizione del Vault eliminato.</span><span class="sxs-lookup"><span data-stu-id="678c6-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678c6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="678c6-131">-ResourceGroupName</span></span>
<span data-ttu-id="678c6-132">Specifica il nome del gruppo di risorse associato alla chiave Vault o alle volte chiave in cui viene eseguita la query.</span><span class="sxs-lookup"><span data-stu-id="678c6-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678c6-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="678c6-133">-Tag</span></span>
<span data-ttu-id="678c6-134">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="678c6-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="678c6-135">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="678c6-135">For example:</span></span>

<span data-ttu-id="678c6-136">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="678c6-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678c6-137">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="678c6-137">-VaultName</span></span>
<span data-ttu-id="678c6-138">Specifica il nome del Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="678c6-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="678c6-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="678c6-139">-DefaultProfile</span></span>
<span data-ttu-id="678c6-140">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="678c6-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="678c6-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="678c6-141">CommonParameters</span></span>
<span data-ttu-id="678c6-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="678c6-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="678c6-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="678c6-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="678c6-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="678c6-144">INPUTS</span></span>

## <span data-ttu-id="678c6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="678c6-145">OUTPUTS</span></span>

### <span data-ttu-id="678c6-146">Microsoft. Azure. Commands. Vault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="678c6-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="678c6-147">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. Vault. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="678c6-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="678c6-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="678c6-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="678c6-149">System. Collections. Generic. list ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="678c6-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="678c6-150">Note</span><span class="sxs-lookup"><span data-stu-id="678c6-150">NOTES</span></span>

## <span data-ttu-id="678c6-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="678c6-151">RELATED LINKS</span></span>

[<span data-ttu-id="678c6-152">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="678c6-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="678c6-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="678c6-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
