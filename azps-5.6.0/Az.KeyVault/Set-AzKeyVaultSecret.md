---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: a9c104bfc1935f65969e11af8de0abdb4f46c3e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980398"
---
# <span data-ttu-id="34f48-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34f48-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="34f48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f48-102">SYNOPSIS</span></span>
<span data-ttu-id="34f48-103">Crea o aggiorna un segreto in un vault delle chiavi.</span><span class="sxs-lookup"><span data-stu-id="34f48-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="34f48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="34f48-104">SYNTAX</span></span>

### <span data-ttu-id="34f48-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="34f48-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34f48-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="34f48-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34f48-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="34f48-107">DESCRIPTION</span></span>
<span data-ttu-id="34f48-108">Il cmdlet **Set-AzKeyVaultSecret** crea o aggiorna un segreto in un vault delle chiavi nel Vault delle chiavi di Azure.</span><span class="sxs-lookup"><span data-stu-id="34f48-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="34f48-109">Se il segreto non esiste, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="34f48-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="34f48-110">Se il segreto esiste già, questo cmdlet crea una nuova versione del segreto.</span><span class="sxs-lookup"><span data-stu-id="34f48-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="34f48-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="34f48-111">EXAMPLES</span></span>

### <span data-ttu-id="34f48-112">Esempio 1: Modificare il valore di un segreto usando gli attributi predefiniti</span><span class="sxs-lookup"><span data-stu-id="34f48-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

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

<span data-ttu-id="34f48-113">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella $Secret variabile.</span><span class="sxs-lookup"><span data-stu-id="34f48-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="34f48-114">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="34f48-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="34f48-115">Il secondo comando modifica il valore del segreto denominato ITSecret nella chiave vault denominata Contoso.</span><span class="sxs-lookup"><span data-stu-id="34f48-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="34f48-116">Il valore segreto diventa il valore archiviato nella $Secret.</span><span class="sxs-lookup"><span data-stu-id="34f48-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="34f48-117">Esempio 2: Modificare il valore di un segreto usando attributi personalizzati</span><span class="sxs-lookup"><span data-stu-id="34f48-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

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

<span data-ttu-id="34f48-118">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella $Secret variabile.</span><span class="sxs-lookup"><span data-stu-id="34f48-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="34f48-119">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="34f48-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="34f48-120">I comandi seguenti definiscono gli attributi personalizzati per la data di scadenza, i tag e il tipo di contesto e archiviano gli attributi in variabili.</span><span class="sxs-lookup"><span data-stu-id="34f48-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="34f48-121">Il comando finale modifica i valori del segreto denominato ITSecret nella chiave vault denominata Contoso, usando i valori specificati in precedenza come variabili.</span><span class="sxs-lookup"><span data-stu-id="34f48-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="34f48-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34f48-122">PARAMETERS</span></span>

### <span data-ttu-id="34f48-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="34f48-123">-ContentType</span></span>
<span data-ttu-id="34f48-124">Specifica il tipo di contenuto di un segreto.</span><span class="sxs-lookup"><span data-stu-id="34f48-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="34f48-125">Per eliminare il tipo di contenuto esistente, specificare una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="34f48-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="34f48-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f48-126">-DefaultProfile</span></span>
<span data-ttu-id="34f48-127">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="34f48-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="34f48-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="34f48-128">-Disable</span></span>
<span data-ttu-id="34f48-129">Indica che questo cmdlet disabilita un segreto.</span><span class="sxs-lookup"><span data-stu-id="34f48-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="34f48-130">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="34f48-130">-Expires</span></span>
<span data-ttu-id="34f48-131">Specifica la scadenza, come oggetto **DateTime,** per il segreto che viene aggiornato dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f48-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="34f48-132">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="34f48-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="34f48-133">Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="34f48-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="34f48-134">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="34f48-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="34f48-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34f48-135">-InputObject</span></span>
<span data-ttu-id="34f48-136">Oggetto segreto</span><span class="sxs-lookup"><span data-stu-id="34f48-136">Secret object</span></span>

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

### <span data-ttu-id="34f48-137">-Name</span><span class="sxs-lookup"><span data-stu-id="34f48-137">-Name</span></span>
<span data-ttu-id="34f48-138">Specifica il nome di un segreto da modificare.</span><span class="sxs-lookup"><span data-stu-id="34f48-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="34f48-139">Questo cmdlet crea il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del vault delle chiavi e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="34f48-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="34f48-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="34f48-140">-NotBefore</span></span>
<span data-ttu-id="34f48-141">Specifica l'ora, come oggetto **DateTime,** prima della quale non è possibile usare il segreto.</span><span class="sxs-lookup"><span data-stu-id="34f48-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="34f48-142">Questo parametro usa utc.</span><span class="sxs-lookup"><span data-stu-id="34f48-142">This parameter uses UTC.</span></span> <span data-ttu-id="34f48-143">Per ottenere un **oggetto DateTime,** usare il cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="34f48-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="34f48-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="34f48-144">-SecretValue</span></span>
<span data-ttu-id="34f48-145">Specifica il valore per il segreto come **oggetto SecureString.**</span><span class="sxs-lookup"><span data-stu-id="34f48-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="34f48-146">Per ottenere un **oggetto SecureString,** usare il cmdlet **ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="34f48-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="34f48-147">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="34f48-147">For more information, type `Get-Help
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

### <span data-ttu-id="34f48-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="34f48-148">-Tag</span></span>
<span data-ttu-id="34f48-149">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="34f48-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="34f48-150">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="34f48-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="34f48-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="34f48-151">-VaultName</span></span>
<span data-ttu-id="34f48-152">Specifica il nome del vault della chiave a cui appartiene questo segreto.</span><span class="sxs-lookup"><span data-stu-id="34f48-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="34f48-153">Questo cmdlet crea l'FQDN di un vault delle chiavi in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="34f48-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="34f48-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34f48-154">-Confirm</span></span>
<span data-ttu-id="34f48-155">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34f48-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34f48-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34f48-156">-WhatIf</span></span>
<span data-ttu-id="34f48-157">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34f48-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34f48-158">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="34f48-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34f48-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f48-159">CommonParameters</span></span>
<span data-ttu-id="34f48-160">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34f48-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f48-161">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34f48-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f48-162">INPUT</span><span class="sxs-lookup"><span data-stu-id="34f48-162">INPUTS</span></span>

### <span data-ttu-id="34f48-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="34f48-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="34f48-164">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="34f48-164">OUTPUTS</span></span>

### <span data-ttu-id="34f48-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34f48-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="34f48-166">NOTE</span><span class="sxs-lookup"><span data-stu-id="34f48-166">NOTES</span></span>

## <span data-ttu-id="34f48-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="34f48-167">RELATED LINKS</span></span>

[<span data-ttu-id="34f48-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34f48-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="34f48-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="34f48-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
