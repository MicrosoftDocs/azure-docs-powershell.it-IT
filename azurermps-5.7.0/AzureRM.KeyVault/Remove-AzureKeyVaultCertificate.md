---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 6c8fcc5476ea2defda78ea03cc1acce7b7e3dea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520444"
---
# <span data-ttu-id="cccc3-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cccc3-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="cccc3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cccc3-102">SYNOPSIS</span></span>
<span data-ttu-id="cccc3-103">Rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cccc3-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cccc3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cccc3-104">SYNTAX</span></span>

### <span data-ttu-id="cccc3-105">ByVaultNameAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cccc3-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cccc3-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cccc3-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cccc3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cccc3-107">DESCRIPTION</span></span>
<span data-ttu-id="cccc3-108">Il cmdlet **Remove-AzureKeyVaultCertificate** rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cccc3-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="cccc3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cccc3-109">EXAMPLES</span></span>

### <span data-ttu-id="cccc3-110">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="cccc3-110">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="cccc3-111">Questo comando rimuove il certificato denominato SelfSigned01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="cccc3-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="cccc3-112">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="cccc3-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="cccc3-113">Di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="cccc3-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="cccc3-114">Esempio 3: eliminare definitivamente il certificato eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="cccc3-114">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="cccc3-115">Questo comando rimuove definitivamente il certificato denominato "CERT" dall'archivio della chiave denominato "contoso".</span><span class="sxs-lookup"><span data-stu-id="cccc3-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="cccc3-116">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente in questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cccc3-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="cccc3-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cccc3-117">PARAMETERS</span></span>

### <span data-ttu-id="cccc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cccc3-118">-DefaultProfile</span></span>
<span data-ttu-id="cccc3-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cccc3-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cccc3-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cccc3-120">-Force</span></span>
<span data-ttu-id="cccc3-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cccc3-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cccc3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cccc3-122">-InputObject</span></span>
<span data-ttu-id="cccc3-123">Oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="cccc3-123">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cccc3-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="cccc3-124">-InRemovedState</span></span>
<span data-ttu-id="cccc3-125">Se presente, rimuove definitivamente il certificato eliminato in precedenza</span><span class="sxs-lookup"><span data-stu-id="cccc3-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="cccc3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="cccc3-126">-Name</span></span>
<span data-ttu-id="cccc3-127">Specifica il nome del certificato rimosso da questo cmdlet da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="cccc3-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="cccc3-128">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato basato sul nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="cccc3-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cccc3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cccc3-129">-PassThru</span></span>
<span data-ttu-id="cccc3-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cccc3-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cccc3-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cccc3-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cccc3-132">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="cccc3-132">-VaultName</span></span>
<span data-ttu-id="cccc3-133">Specifica il nome del Vault chiave da cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="cccc3-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="cccc3-134">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="cccc3-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cccc3-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cccc3-135">-Confirm</span></span>
<span data-ttu-id="cccc3-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cccc3-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccc3-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cccc3-137">-WhatIf</span></span>
<span data-ttu-id="cccc3-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cccc3-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cccc3-139">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cccc3-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cccc3-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cccc3-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cccc3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cccc3-141">CommonParameters</span></span>
<span data-ttu-id="cccc3-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cccc3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cccc3-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cccc3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cccc3-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cccc3-144">INPUTS</span></span>

### <span data-ttu-id="cccc3-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cccc3-145">None</span></span>
<span data-ttu-id="cccc3-146">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="cccc3-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cccc3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cccc3-147">OUTPUTS</span></span>

### <span data-ttu-id="cccc3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cccc3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="cccc3-149">Note</span><span class="sxs-lookup"><span data-stu-id="cccc3-149">NOTES</span></span>

## <span data-ttu-id="cccc3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cccc3-150">RELATED LINKS</span></span>

[<span data-ttu-id="cccc3-151">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cccc3-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cccc3-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cccc3-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cccc3-153">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="cccc3-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="cccc3-154">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="cccc3-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
