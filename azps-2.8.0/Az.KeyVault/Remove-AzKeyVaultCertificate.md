---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: 3e2da64d467d71721255afa12211530e7c0d9f08
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674133"
---
# <span data-ttu-id="c0cc8-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c0cc8-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="c0cc8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c0cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cc8-103">Rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="c0cc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c0cc8-104">SYNTAX</span></span>

### <span data-ttu-id="c0cc8-105">ByVaultNameAndName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c0cc8-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cc8-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c0cc8-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0cc8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0cc8-107">DESCRIPTION</span></span>
<span data-ttu-id="c0cc8-108">Il cmdlet **Remove-AzKeyVaultCertificate** rimuove un certificato da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="c0cc8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c0cc8-109">EXAMPLES</span></span>

### <span data-ttu-id="c0cc8-110">Esempio 1: rimuovere un certificato</span><span class="sxs-lookup"><span data-stu-id="c0cc8-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="c0cc8-111">Questo comando rimuove il certificato denominato SelfSigned01 dal Vault chiave denominato ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="c0cc8-112">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="c0cc8-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c0cc8-113">Di conseguenza, il cmdlet non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="c0cc8-114">Esempio 2: eliminare definitivamente il certificato eliminato dal caveau della chiave</span><span class="sxs-lookup"><span data-stu-id="c0cc8-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="c0cc8-115">Questo comando rimuove definitivamente il certificato denominato "CERT" dall'archivio della chiave denominato "contoso".</span><span class="sxs-lookup"><span data-stu-id="c0cc8-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="c0cc8-116">L'esecuzione di questo cmdlet richiede l'autorizzazione "Purge", che deve essere stata concessa in precedenza e esplicitamente all'utente in questo Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="c0cc8-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c0cc8-117">PARAMETERS</span></span>

### <span data-ttu-id="c0cc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cc8-118">-DefaultProfile</span></span>
<span data-ttu-id="c0cc8-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c0cc8-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0cc8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c0cc8-120">-Force</span></span>
<span data-ttu-id="c0cc8-121">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c0cc8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0cc8-122">-InputObject</span></span>
<span data-ttu-id="c0cc8-123">Oggetto certificato.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0cc8-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c0cc8-124">-InRemovedState</span></span>
<span data-ttu-id="c0cc8-125">Se presente, rimuove definitivamente il certificato eliminato in precedenza</span><span class="sxs-lookup"><span data-stu-id="c0cc8-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="c0cc8-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c0cc8-126">-Name</span></span>
<span data-ttu-id="c0cc8-127">Specifica il nome del certificato rimosso da questo cmdlet da un Vault chiave.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="c0cc8-128">Questo cmdlet costruisce il nome di dominio completo (FQDN) di un certificato basato sul nome specificato da questo parametro, il nome del Vault della chiave e l'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cc8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c0cc8-129">-PassThru</span></span>
<span data-ttu-id="c0cc8-130">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c0cc8-131">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c0cc8-132">-VAULTNAME</span><span class="sxs-lookup"><span data-stu-id="c0cc8-132">-VaultName</span></span>
<span data-ttu-id="c0cc8-133">Specifica il nome del Vault chiave da cui questo cmdlet rimuove un certificato.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="c0cc8-134">Questo cmdlet crea l'FQDN di un Vault chiave in base al nome specificato da questo parametro e all'ambiente corrente.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cc8-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c0cc8-135">-Confirm</span></span>
<span data-ttu-id="c0cc8-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cc8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0cc8-137">-WhatIf</span></span>
<span data-ttu-id="c0cc8-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cc8-139">Il cmdlet non viene eseguito. Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cc8-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0cc8-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cc8-141">CommonParameters</span></span>
<span data-ttu-id="c0cc8-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0cc8-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cc8-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0cc8-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cc8-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c0cc8-144">INPUTS</span></span>

### <span data-ttu-id="c0cc8-145">Microsoft. Azure. Commands. Vault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c0cc8-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c0cc8-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c0cc8-146">OUTPUTS</span></span>

### <span data-ttu-id="c0cc8-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c0cc8-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="c0cc8-148">Note</span><span class="sxs-lookup"><span data-stu-id="c0cc8-148">NOTES</span></span>

## <span data-ttu-id="c0cc8-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c0cc8-149">RELATED LINKS</span></span>

[<span data-ttu-id="c0cc8-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c0cc8-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="c0cc8-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c0cc8-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="c0cc8-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c0cc8-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="c0cc8-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="c0cc8-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
