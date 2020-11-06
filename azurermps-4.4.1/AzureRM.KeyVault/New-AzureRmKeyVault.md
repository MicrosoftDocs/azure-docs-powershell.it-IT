---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://go.microsoft.com/fwlink/?LinkId=690160
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureRmKeyVault.md
ms.openlocfilehash: 28cd93fe9de14365e4de626729ec45a7aaa88cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521623"
---
# <span data-ttu-id="ba76b-101">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ba76b-101">New-AzureRmKeyVault</span></span>

## <span data-ttu-id="ba76b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba76b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba76b-103">Crea un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ba76b-103">Creates a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba76b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba76b-104">SYNTAX</span></span>

```
New-AzureRmKeyVault [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnableSoftDelete]
 [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ba76b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba76b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba76b-106">Il cmdlet **New-AzureRmKeyVault** crea un Vault Key nel gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="ba76b-106">The **New-AzureRmKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="ba76b-107">Questo cmdlet concede anche le autorizzazioni per l'utente attualmente connesso per aggiungere, rimuovere o elencare chiavi e segreti nel caveau della chiave.</span><span class="sxs-lookup"><span data-stu-id="ba76b-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>

<span data-ttu-id="ba76b-108">Nota: se viene visualizzato l'errore **l'abbonamento non è registrato per l'uso dello spazio dei nomi "Microsoft. Key Vault"** quando si tenta di creare il nuovo Vault chiave, eseguire **Register-AzureRmResourceProvider-ProviderNamespace "Microsoft. Key Vault"** e quindi eseguire di nuovo il comando **New-AzureRmKeyVault** .</span><span class="sxs-lookup"><span data-stu-id="ba76b-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzureRmResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzureRmKeyVault** command.</span></span> <span data-ttu-id="ba76b-109">Per altre informazioni, vedere Register-AzureRmResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="ba76b-109">For more information, see Register-AzureRmResourceProvider.</span></span>

## <span data-ttu-id="ba76b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba76b-110">EXAMPLES</span></span>

### <span data-ttu-id="ba76b-111">Esempio 1: creare un Vault chiave standard</span><span class="sxs-lookup"><span data-stu-id="ba76b-111">Example 1: Create a Standard key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

<span data-ttu-id="ba76b-112">Questo comando crea un Vault chiave denominato Contoso03Vault, nell'area di Azure est US.</span><span class="sxs-lookup"><span data-stu-id="ba76b-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="ba76b-113">Il comando aggiunge il Vault chiave al gruppo di risorse denominato Group14.</span><span class="sxs-lookup"><span data-stu-id="ba76b-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="ba76b-114">Poiché il comando non specifica un valore per il parametro *SKU* , crea un Vault chiave standard.</span><span class="sxs-lookup"><span data-stu-id="ba76b-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="ba76b-115">Esempio 2: creare un Vault Key Premium</span><span class="sxs-lookup"><span data-stu-id="ba76b-115">Example 2: Create a Premium key vault</span></span>
```
PS C:\>New-AzureRmKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'
```

<span data-ttu-id="ba76b-116">Questo comando crea un Vault chiave, proprio come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="ba76b-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="ba76b-117">Tuttavia, specifica un valore Premium per il parametro *SKU* per creare un Vault Key Premium.</span><span class="sxs-lookup"><span data-stu-id="ba76b-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

## <span data-ttu-id="ba76b-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba76b-118">PARAMETERS</span></span>

### <span data-ttu-id="ba76b-119">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="ba76b-119">-EnabledForDeployment</span></span>
<span data-ttu-id="ba76b-120">Consente al provider di risorse Microsoft. Compute di recuperare i segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave nella creazione di risorse, ad esempio quando si crea una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="ba76b-120">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-121">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ba76b-121">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="ba76b-122">Abilita il servizio di crittografia di Azure disk per ottenere segreti e scartare le chiavi da questo caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="ba76b-122">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-123">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="ba76b-123">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="ba76b-124">Consente a Azure Resource Manager di ottenere segreti da questo Vault chiave quando si fa riferimento a questo Vault chiave in una distribuzione di modelli.</span><span class="sxs-lookup"><span data-stu-id="ba76b-124">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="ba76b-125">-EnableSoftDelete</span></span>
<span data-ttu-id="ba76b-126">Se specificato, la funzionalità' Elimina soft ' è abilitata per il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ba76b-126">If specified, 'soft delete' functionality is enabled for this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ba76b-127">-Location</span></span>
<span data-ttu-id="ba76b-128">Specifica l'area di Azure in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ba76b-128">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="ba76b-129">Usa il comando Get-AzureLocation ( https://msdn.microsoft.com/ Library/Azure/mt589064. aspx) per vedere le tue scelte.</span><span class="sxs-lookup"><span data-stu-id="ba76b-129">Use the command Get-AzureLocation (https://msdn.microsoft.com/ library/azure/mt589064.aspx) to see your choices.</span></span> <span data-ttu-id="ba76b-130">Per altre informazioni, digitare `Get-Help Get-AzureLocation` .</span><span class="sxs-lookup"><span data-stu-id="ba76b-130">For more information, type `Get-Help Get-AzureLocation`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba76b-131">-ResourceGroupName</span></span>
<span data-ttu-id="ba76b-132">Specifica il nome di un gruppo di risorse esistente in cui creare il Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="ba76b-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="ba76b-133">-Sku</span></span>
<span data-ttu-id="ba76b-134">Specifica l'USK dell'istanza Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ba76b-134">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="ba76b-135">Per informazioni sulle caratteristiche disponibili per ogni Usk, vedere il sito Web relativo ai prezzi di Azure Key Vault ( https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="ba76b-135">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: Microsoft.Azure.Management.KeyVault.Models.SkuName
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="ba76b-136">-Tag</span></span>
<span data-ttu-id="ba76b-137">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ba76b-137">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ba76b-138">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="ba76b-138">For example:</span></span>

<span data-ttu-id="ba76b-139">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ba76b-139">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-140">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="ba76b-140">-VaultName</span></span>
<span data-ttu-id="ba76b-141">Specifica il nome del Vault della chiave da creare.</span><span class="sxs-lookup"><span data-stu-id="ba76b-141">Specifies the name of the key vault to create.</span></span> <span data-ttu-id="ba76b-142">Il nome può essere costituito da qualsiasi combinazione di lettere, cifre o trattini.</span><span class="sxs-lookup"><span data-stu-id="ba76b-142">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="ba76b-143">Il nome deve iniziare e terminare con una lettera o una cifra.</span><span class="sxs-lookup"><span data-stu-id="ba76b-143">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="ba76b-144">Il nome deve essere universalmente univoco.</span><span class="sxs-lookup"><span data-stu-id="ba76b-144">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba76b-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ba76b-145">-Confirm</span></span>
<span data-ttu-id="ba76b-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba76b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba76b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba76b-147">-WhatIf</span></span>
<span data-ttu-id="ba76b-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba76b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba76b-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ba76b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba76b-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba76b-150">-DefaultProfile</span></span>
<span data-ttu-id="ba76b-151">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba76b-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba76b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba76b-152">CommonParameters</span></span>
<span data-ttu-id="ba76b-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba76b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba76b-154">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba76b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba76b-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba76b-155">INPUTS</span></span>

## <span data-ttu-id="ba76b-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba76b-156">OUTPUTS</span></span>

### <span data-ttu-id="ba76b-157">Microsoft. Azure. Commands. Vault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="ba76b-157">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="ba76b-158">Note</span><span class="sxs-lookup"><span data-stu-id="ba76b-158">NOTES</span></span>

## <span data-ttu-id="ba76b-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba76b-159">RELATED LINKS</span></span>

[<span data-ttu-id="ba76b-160">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ba76b-160">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)

[<span data-ttu-id="ba76b-161">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="ba76b-161">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
