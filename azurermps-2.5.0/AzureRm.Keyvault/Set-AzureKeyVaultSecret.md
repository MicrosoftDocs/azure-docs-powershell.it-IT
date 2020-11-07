---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 0c482d3fd4e2e02221799ea72e61eacc80ff9e2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866677"
---
# <span data-ttu-id="74a91-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="74a91-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="74a91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74a91-102">SYNOPSIS</span></span>
<span data-ttu-id="74a91-103">Crea o aggiorna un segreto in un caveau chiave.</span><span class="sxs-lookup"><span data-stu-id="74a91-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74a91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74a91-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74a91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74a91-105">DESCRIPTION</span></span>
<span data-ttu-id="74a91-106">Il cmdlet **set-AzureKeyVaultSecret** crea o aggiorna un segreto in un Vault chiave in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="74a91-106">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="74a91-107">Se il segreto non esiste, questo cmdlet lo crea.</span><span class="sxs-lookup"><span data-stu-id="74a91-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="74a91-108">Se il segreto esiste già, questo cmdlet crea una nuova versione di tale segreto.</span><span class="sxs-lookup"><span data-stu-id="74a91-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="74a91-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74a91-109">EXAMPLES</span></span>

### <span data-ttu-id="74a91-110">Esempio 1: modificare il valore di un segreto usando gli attributi predefiniti</span><span class="sxs-lookup"><span data-stu-id="74a91-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="74a91-111">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $Secret.</span><span class="sxs-lookup"><span data-stu-id="74a91-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="74a91-112">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="74a91-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="74a91-113">Il secondo comando modifica il valore del segreto denominato ITSecret nel caveau della chiave denominato contoso.</span><span class="sxs-lookup"><span data-stu-id="74a91-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="74a91-114">Il valore segreto diventa il valore archiviato in $Secret.</span><span class="sxs-lookup"><span data-stu-id="74a91-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="74a91-115">Esempio 2: modificare il valore di un segreto usando attributi personalizzati</span><span class="sxs-lookup"><span data-stu-id="74a91-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="74a91-116">Il primo comando converte una stringa in una stringa sicura usando il cmdlet **ConvertTo-SecureString** e quindi archivia la stringa nella variabile $Secret.</span><span class="sxs-lookup"><span data-stu-id="74a91-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="74a91-117">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="74a91-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="74a91-118">I comandi successivi definiscono gli attributi personalizzati per la data di scadenza, i tag e il tipo di contesto e archiviano gli attributi nelle variabili.</span><span class="sxs-lookup"><span data-stu-id="74a91-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="74a91-119">Il comando finale modifica i valori del segreto denominato ITSecret nel caveau della chiave denominato contoso, usando i valori specificati in precedenza come variabili.</span><span class="sxs-lookup"><span data-stu-id="74a91-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="74a91-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74a91-120">PARAMETERS</span></span>

### <span data-ttu-id="74a91-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="74a91-121">-ContentType</span></span>
<span data-ttu-id="74a91-122">Specifica il tipo di contenuto di un segreto.</span><span class="sxs-lookup"><span data-stu-id="74a91-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="74a91-123">Per eliminare il tipo di contenuto esistente, specificare una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="74a91-123">To delete the existing content type, specify an empty string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a91-124">-DefaultProfile</span></span>
<span data-ttu-id="74a91-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="74a91-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74a91-126">-Disable</span><span class="sxs-lookup"><span data-stu-id="74a91-126">-Disable</span></span>
<span data-ttu-id="74a91-127">Indica che questo cmdlet disabilita un segreto.</span><span class="sxs-lookup"><span data-stu-id="74a91-127">Indicates that this cmdlet disables a secret.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-128">-Scadenza</span><span class="sxs-lookup"><span data-stu-id="74a91-128">-Expires</span></span>
<span data-ttu-id="74a91-129">Specifica la data di scadenza, come oggetto **DateTime** , per il segreto che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="74a91-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="74a91-130">Questo parametro usa l'ora UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="74a91-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="74a91-131">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="74a91-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="74a91-132">Per altre informazioni, digitare `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="74a91-132">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="74a91-133">-Name</span></span>
<span data-ttu-id="74a91-134">Specifica il nome di un segreto da modificare.</span><span class="sxs-lookup"><span data-stu-id="74a91-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="74a91-135">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un segreto in base al nome specificato da questo parametro, al nome del Vault della chiave e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="74a91-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="74a91-136">-NotBefore</span></span>
<span data-ttu-id="74a91-137">Specifica il tempo, come oggetto **DateTime** , prima del quale non è possibile usare il segreto.</span><span class="sxs-lookup"><span data-stu-id="74a91-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="74a91-138">Questo parametro usa l'ora UTC.</span><span class="sxs-lookup"><span data-stu-id="74a91-138">This parameter uses UTC.</span></span> <span data-ttu-id="74a91-139">Per ottenere un oggetto **DateTime** , usare il cmdlet **get-date** .</span><span class="sxs-lookup"><span data-stu-id="74a91-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="74a91-140">-SecretValue</span></span>
<span data-ttu-id="74a91-141">Specifica il valore per il segreto come oggetto **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="74a91-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="74a91-142">Per ottenere un oggetto **SecureString** , usa il cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="74a91-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="74a91-143">Per altre informazioni, digitare `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="74a91-143">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="74a91-144">-Tag</span></span>
<span data-ttu-id="74a91-145">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="74a91-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="74a91-146">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="74a91-146">For example:</span></span>

<span data-ttu-id="74a91-147">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="74a91-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-148">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="74a91-148">-VaultName</span></span>
<span data-ttu-id="74a91-149">Specifica il nome del Vault chiave a cui appartiene il segreto.</span><span class="sxs-lookup"><span data-stu-id="74a91-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="74a91-150">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="74a91-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-151">-Confermare</span><span class="sxs-lookup"><span data-stu-id="74a91-151">-Confirm</span></span>
<span data-ttu-id="74a91-152">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74a91-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74a91-153">-WhatIf</span></span>
<span data-ttu-id="74a91-154">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74a91-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74a91-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74a91-155">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74a91-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a91-156">CommonParameters</span></span>
<span data-ttu-id="74a91-157">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74a91-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a91-158">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a91-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a91-159">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74a91-159">INPUTS</span></span>

## <span data-ttu-id="74a91-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74a91-160">OUTPUTS</span></span>

### <span data-ttu-id="74a91-161">Microsoft. Azure. Commands. Vault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="74a91-161">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="74a91-162">Note</span><span class="sxs-lookup"><span data-stu-id="74a91-162">NOTES</span></span>

## <span data-ttu-id="74a91-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74a91-163">RELATED LINKS</span></span>

[<span data-ttu-id="74a91-164">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="74a91-164">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="74a91-165">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="74a91-165">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
