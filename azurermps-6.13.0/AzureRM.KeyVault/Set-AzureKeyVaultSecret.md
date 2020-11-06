---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: 820406a3fe4bebfd0b2a972bb8676bbd483f7080
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510955"
---
# <span data-ttu-id="9e158-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9e158-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="9e158-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e158-102">SYNOPSIS</span></span>
<span data-ttu-id="9e158-103">Crea o aggiorna un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="9e158-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e158-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e158-104">SYNTAX</span></span>

### <span data-ttu-id="9e158-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e158-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e158-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9e158-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e158-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e158-107">DESCRIPTION</span></span>
<span data-ttu-id="9e158-108">Il cmdlet **set-AzureKeyVaultSecret** crea o aggiorna un segreto in un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9e158-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="9e158-109">Se il segreto non esiste, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="9e158-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="9e158-110">Se il segreto esiste già, questo cmdlet crea una nuova versione di tale segreto.</span><span class="sxs-lookup"><span data-stu-id="9e158-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="9e158-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e158-111">EXAMPLES</span></span>

### <span data-ttu-id="9e158-112">Esempio 1: modificare il valore di un segreto usando gli attributi predefiniti</span><span class="sxs-lookup"><span data-stu-id="9e158-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="9e158-113">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $Secret.</span><span class="sxs-lookup"><span data-stu-id="9e158-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="9e158-114">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="9e158-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="9e158-115">Il secondo comando modifica il valore del segreto denominato ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="9e158-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="9e158-116">Il valore segreto diventa il valore archiviato in $Secret.</span><span class="sxs-lookup"><span data-stu-id="9e158-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="9e158-117">Esempio 2: modificare il valore di un segreto usando attributi personalizzati</span><span class="sxs-lookup"><span data-stu-id="9e158-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="9e158-118">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $Secret.</span><span class="sxs-lookup"><span data-stu-id="9e158-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="9e158-119">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="9e158-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="9e158-120">I comandi successivi definiscono gli attributi personalizzati per la data di scadenza, i tag e il tipo di contesto e archiviano gli attributi nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="9e158-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="9e158-121">Il comando finale modifica i valori del segreto denominato ITSecret nel caveau della chiave denominato contoso, usando i valori specificati in precedenza come variabili.</span><span class="sxs-lookup"><span data-stu-id="9e158-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="9e158-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e158-122">PARAMETERS</span></span>

### <span data-ttu-id="9e158-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="9e158-123">-ContentType</span></span>
<span data-ttu-id="9e158-124">Specifica il tipo di contenuto di un segreto.</span><span class="sxs-lookup"><span data-stu-id="9e158-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="9e158-125">Per eliminare il tipo di contenuto esistente, specificare una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="9e158-125">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e158-126">-DefaultProfile</span></span>
<span data-ttu-id="9e158-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9e158-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9e158-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="9e158-128">-Disable</span></span>
<span data-ttu-id="9e158-129">Indica che questo cmdlet disabilita un segreto.</span><span class="sxs-lookup"><span data-stu-id="9e158-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="9e158-130">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="9e158-130">-Expires</span></span>
<span data-ttu-id="9e158-131">Specifica la data di scadenza, come oggetto **DateTime** , per il segreto che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="9e158-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="9e158-132">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="9e158-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="9e158-133">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="9e158-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="9e158-134">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="9e158-134">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e158-135">-InputObject</span></span>
<span data-ttu-id="9e158-136">Oggetto segreto</span><span class="sxs-lookup"><span data-stu-id="9e158-136">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e158-137">-Name</span></span>
<span data-ttu-id="9e158-138">Specifica il nome di un segreto da modificare.</span><span class="sxs-lookup"><span data-stu-id="9e158-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="9e158-139">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="9e158-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="9e158-140">-NotBefore</span></span>
<span data-ttu-id="9e158-141">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare il segreto.</span><span class="sxs-lookup"><span data-stu-id="9e158-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="9e158-142">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="9e158-142">This parameter uses UTC.</span></span> <span data-ttu-id="9e158-143">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="9e158-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="9e158-144">-SecretValue</span></span>
<span data-ttu-id="9e158-145">Specifica il valore per il segreto come oggetto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="9e158-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="9e158-146">Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="9e158-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="9e158-147">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="9e158-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="9e158-148">-Tag</span></span>
<span data-ttu-id="9e158-149">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9e158-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9e158-150">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9e158-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-151">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="9e158-151">-VaultName</span></span>
<span data-ttu-id="9e158-152">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="9e158-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="9e158-153">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="9e158-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e158-154">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e158-154">-Confirm</span></span>
<span data-ttu-id="9e158-155">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e158-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e158-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e158-156">-WhatIf</span></span>
<span data-ttu-id="9e158-157">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e158-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e158-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e158-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e158-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e158-159">CommonParameters</span></span>
<span data-ttu-id="9e158-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e158-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e158-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e158-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e158-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e158-162">INPUTS</span></span>

### <span data-ttu-id="9e158-163">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9e158-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="9e158-164">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9e158-164">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9e158-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e158-165">OUTPUTS</span></span>

### <span data-ttu-id="9e158-166">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9e158-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="9e158-167">Note</span><span class="sxs-lookup"><span data-stu-id="9e158-167">NOTES</span></span>

## <span data-ttu-id="9e158-168">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e158-168">RELATED LINKS</span></span>

[<span data-ttu-id="9e158-169">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9e158-169">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="9e158-170">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9e158-170">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
